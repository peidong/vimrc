# Installation
## Ubuntu Installation

    sudo apt-get install pylint
    sudo apt-get install aptitude
    sudo aptitude install exuberant-ctags ack-grep git build-essential cmake python-dev
    cd ~
    git clone https://github.com/peidong/vimrc.git
    mv vimrc .vim
    ln -s ~/.vim/vimrc ~/.vimrc
    ln -s ~/.vim/ycm_extra_conf.py ~/.ycm_extra_conf.py
    mkdir -p ~/.vim/bundle
    git clone https://github.com/Shougo/neobundle.vim ~/.vim/bundle/neobundle.vim

Then vim, and `:NeoBundleInstall`

    cd ~/.vim/bundle/YouCompleteMe
    ./install.py --clang-completer --omnisharp-completer --gocode-completer
    mkdir ~/.undodir/

## Mac OSX Installation
#### How to install [MacVim](https://github.com/macvim-dev/macvim/releases/tag/snapshot-80)

    ./configure --with-features=huge --enable-cscope --enable-largefile --enable-luainterp=yes --enable-multibyte --enable-mzschemeinterp --enable-perlinterp=yes --enable-pythoninterp=yes --with-python-config-dir=/usr/lib/python2.7/config --enable-rubyinterp=yes --enable-tclinterp

install [pip](https://pip.pypa.io/en/stable/installing/)

#### Install vimrc

    ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    brew install ack cmake
    sudo pip install pylint
    cd ~
    git clone https://github.com/peidong/vimrc.git
    mv vimrc .vim
    ln -s ~/.vim/vimrc ~/.vimrc
    ln -s ~/.vim/ycm_extra_conf.py ~/.ycm_extra_conf.py
    mkdir -p ~/.vim/bundle
    git clone https://github.com/Shougo/neobundle.vim ~/.vim/bundle/neobundle.vim

Then vim, and `:NeoBundleInstall`

    cd ~/.vim/bundle/YouCompleteMe
    ./install.py --clang-completer --omnisharp-completer --gocode-completer
    mkdir ~/.undodir/

## Installing on Windows
Not done

# Keymap
#### Normal Mode
##### Pure vimscript plugins
###### Plugin 'mattn/emmet-vim'
Keybinding         | Description
-------------------|------------------------------------------------------------
<kbd>C-y ,</kbd>   | Emmet-vim
###### Plugin 'scrooloose/nerdtree'
Keybinding         | Description
-------------------|------------------------------------------------------------
<kbd>`<leader>` b f</kbd>   | Open file list.`<CR>`:open,`r`:refresh,`I`:show or show off hidden files,`m`:show functions list
<kbd>x</kbd>   | close the tree
<kbd>X</kbd>   | close the tree(recursive)
<kbd>r</kbd>   | refresh the tree
<kbd>R</kbd>   | refresh the tree(recursive)
<kbd>p</kbd>   | jump to the parent
<kbd>P</kbd>   | jump to the parent(root)
<kbd>j(k)</kbd>   | down(up)
<kbd>K(J)</kbd>   | big down(up)
<kbd>o</kbd>   | open
<kbd>i(s)</kbd>   | split up/down(left/right)
<kbd>c</kbd>   | change to root
<kbd>q</kbd>   | close
###### Plugin 'mbbill/undotree'
Keybinding         | Description
-------------------|------------------------------------------------------------
<kbd>`<leader>` b u</kbd>   | show undo list
###### Plugin 'xuhdev/vim-latex-live-preview'
Keybinding         | Description
-------------------|------------------------------------------------------------
<kbd>:LLPStartPreview</kbd>| Using pdf to preview Latex
###### Plugin 'lervag/vimtex'
Keybinding         | Description
-------------------|------------------------------------------------------------
<kbd>] ]</kbd>| Create close envelope
###### Plugin 'tpope/vim-surround'
Keybinding         | Description
-------------------|------------------------------------------------------------
<kbd>ds</kbd>| delete a surrounding
<kbd>cs</kbd>| change a surrounding
<kbd>ys`<motion>`</kbd>| add a surrounding
<kbd>yS</kbd>| add a surrounding and place the surrounded text on a new line + indent it
<kbd>yss</kbd>| add a surrounding to the whole line
<kbd>ySs</kbd>| add a surrounding to the whole line, place it on a new line + indent it
<kbd>ySS</kbd>| same as ySs
###### Plugin 'kien/ctrlp.vim'
Keybinding         | Description
-------------------|------------------------------------------------------------
<kbd>C-p</kbd>| invoke CtrlP in find file mode
<kbd>C-j(k)</kbd>| navigate the result list
<kbd>`Enter`</kbd>| open the file
###### Plugin 'gcmt/wildfire.vim'
Keybinding         | Description
-------------------|------------------------------------------------------------
<kbd>`Enter`</kbd>| select the area
<kbd>`Backspace`</kbd>| backward
###### Plugin 'tpope/vim-fugitive'
Keybinding         | Description
-------------------|------------------------------------------------------------
<kbd>`:Gcommit`</kbd>| git commit
<kbd>`:Gpush`</kbd>| git push
<kbd>`:Gdiff`</kbd>| git diff
<kbd>`:Gstatus`</kbd>| git status
<kbd>`D`</kbd>| git diff
<kbd>C-n(p)</kbd>| next(previous) file
<kbd>-</kbd>| add file
<kbd>cc</kbd>| git commit
<kbd>q</kbd>| quit
###### Plugin 'tomtom/tcomment_vim'
Keybinding         | Description
-------------------|------------------------------------------------------------
<kbd>gc`<motion>`</kbd>   | Comment/uncomment the context
<kbd>gcc</kbd>   | Comment/uncomment the line
<kbd>g\>`<motion>`</kbd>   | Comment the context
<kbd>g\>c</kbd>   | Comment the line
<kbd>g\<`<motion>`</kbd>   | Comment the context
<kbd>g\<c</kbd>   | Comment the line
###### Plugin 'easymotion/vim-easymotion'
Keybinding         | Description
-------------------|------------------------------------------------------------
<kbd>`<leader>` `<leader>` f ?</kbd> | Jump to the ? word
<kbd>`<leader>` `<leader>` j(k)</kbd> | Jump to the next(below) lines
<kbd>`<leader>` `<leader>` w(e)</kbd> | Jump to the words begining(end)
<kbd>`<leader>` `<leader>` .</kbd> | repeat jump
<kbd>v `<leader>` `<leader>` f ?</kbd>| Select to the ? word
<kbd>d `<leader>` `<leader>` f ?</kbd>| Delete to the ? word
<kbd>y `<leader>` `<leader>` f ?</kbd>| Copy to the ? word
###### Plugin 'terryma/vim-multiple-cursors'
Keybinding         | Description
-------------------|------------------------------------------------------------
<kbd>C-n</kbd>| search the next word
<kbd>C-p</kbd>| search the previous word
<kbd>C-x</kbd>| search skip
###### Plugin 'vim-ctrlspace'
Keybinding         | Description
-------------------|------------------------------------------------------------
<kbd>C-`<space>`</kbd>| show tab buffers
<kbd>j(k)</kbd>| down(up)
<kbd>`<return>`</kbd>| open file
<kbd>v(V)</kbd>| vertical split open (cursor in ctrlspace)
<kbd>s(S)</kbd>| split open (cursor in ctrlspace)
<kbd>`<ESC>`/q</kbd>| close
##### Other plugins
###### Plugin 'Valloric/YouCompleteMe'
Keybinding         | Description
-------------------|------------------------------------------------------------
<kbd>`<leader>` c j d</kbd>   | `:YcmCompleter GoToDeclaration<CR>`
<kbd>`<leader>` c j e</kbd>   | `:YcmCompleter GoToDefinition<CR>`
###### Plugin 'dyng/ctrlsf.vim'
Keybinding         | Description
-------------------|------------------------------------------------------------
<kbd>`<leader>` r t</kbd>   | `:CtrlSF<CR>`:search the cursor word,`q`:quit,`p`:see details
<kbd>p</kbd>| Preview
<kbd>q</kbd>| Quit search mode
###### Plugin 'MikeCoder/markdown-preview.vim'
Keybinding         | Description
-------------------|------------------------------------------------------------
<kbd>`<leader>` b m</kbd>| Markdown Preview in Github format

#### Insert Mode

Keybinding         | Description
-------------------|------------------------------------------------------------
<kbd>jj</kbd>      | `<ESC>` : return to Normal Mode

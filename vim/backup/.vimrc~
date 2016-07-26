" filetype plugin on
" filetype indent on
" Pathogen load
filetype off

call pathogen#infect()
call pathogen#helptags()

filetype plugin indent on
syntax on

"colorscheme slate
colorscheme elflord
set background=dark
set colorcolumn=80
set encoding=utf-8
set fileencoding=utf-8

highlight OverLength ctermbg=red ctermfg=white guibg=#592929
match OverLength /\%81v.\+/
highlight ExtraWhitespace ctermbg=darkgreen guibg=darkgreen
match ExtraWhitespace /\t/

" Highlight tabs at beginning of line and trailing whitespace
highlight BadWhiteSpace ctermbg=red  guibg=red
au BufRead,BufNewFile *.py,*.pyw,*.rst match BadWhiteSpace /^\t\+/
au BufRead,BufNewFile *.py,*.pyw,*.rst match BadWhiteSpace /\s\+$/

" " Strip spaces from end of lines
autocmd BufWritePre *.py,*.rst,*.php :%s/\s\+$//e

set backup " make backup files
set backupdir=~/.vim/backup " where to put backup files
set directory=~/.vim/tmp " directory to place swap files in
set fileformats=unix,dos,mac " support all three, in this order
set noerrorbells " don't make noise
set novisualbell " don't blink
set report=0 " tell us when anything is changed via :...
set ruler " Always show current positions along the bottom
set scrolloff=10 " Keep 10 lines (top/bottom) for scope
set showcmd " show the command being typed
set showmatch " show matching brackets
set expandtab " no real tabs please!
set nowrap " do not wrap line
set smartcase " if there are caps, go case-sensitive
set shiftwidth=4 " auto-indent amount when using cindent, 
                 " &gt;&gt;, &lt;&lt; and stuff like that
set softtabstop=4 " when hitting tab or backspace, how many spaces 
                  "should a tab be (see expandtab)
set tabstop=4 " real tabs should be 8, and they will show with 
              " set list on
set backspace=indent,eol,start " make backspace a more flexible
set iskeyword+=_,$,@,%,# " none of these are word dividers               
set wildmenu " turn on command line completion wild style
             " ignore these list file extensions
set wildignore=*.dll,*.o,*.obj,*.bak,*.exe,*.pyc,
                \*.jpg,*.gif,*.png
set wildmode=list:longest " turn on wild mode huge list

set cursorline " highlight the current line
set cursorcolumn " highlight the current column
hi ColorColumn ctermbg=lightblue guibg=lightblue
:nnoremap &lt;Leader&gt;c :set cursorline! cursorcolumn!&lt;CR&gt;
set linespace=0 " don't insert any extra pixel lines
                " between rows
set list " we do what to show tabs, to ensure we get them 
         " out of my files
set listchars=tab:>-,trail:- " show tabs and trailing 
set nohlsearch " do not highlight searched for phrases
set nostartofline " leave my cursor where it was
set nonumber
set numberwidth=5 "We are good up to 99999 lines
set statusline=%F%m%r%h%w[%L][%{&ff}]%y[0x%B][%p%%][%04l,%04v]
"              | | | | |  |   |      |   |     |     |    | 
"              | | | | |  |   |      |   |     |     |    |
"              | | | | |  |   |      |   |     |     |    + current 
"              | | | | |  |   |      |   |     |     |       column
"              | | | | |  |   |      |   |     |     +-- current line
"              | | | | |  |   |      |   |     +-- current % into file
"              | | | | |  |   |      |   +--hex code for chr
"              | | | | |  |   |      +-- current syntax in 
"              | | | | |  |   |          square brackets
"              | | | | |  |   +-- current fileformat
"              | | | | |  +-- number of lines
"              | | | | +-- preview flag in square brackets
"              | | | +-- help flag in square brackets
"              | | +-- readonly flag in square brackets
"              | +-- rodified flag in square brackets
"              +-- full path to file in the buffer
"
"
set laststatus=2

" Enable python folding
let g:pymode_folding = 0

" let g:pymode_lint_checker = "pep8"
set completeopt-=preview

" Ignore line length
let g:pymode_lint_ignore = "E501,W"

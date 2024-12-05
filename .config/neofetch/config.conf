" ---------------------
" 1. CONFIGURACIÓN PRINCIPAL
" ---------------------
set number              " Mostrar números de línea
set tabstop=4            " Definir el tamaño de tabulador
set shiftwidth=4         " Establecer el desplazamiento para la indentación
set expandtab            " Usar espacios en lugar de tabuladores
set clipboard=unnamedplus " Habilitar el portapapeles del sistema
set mouse=a              " Habilitar soporte de ratón
set cursorline           " Resaltar la línea del cursor

" ---------------------
" 2. CONFIGURACIÓN DE PLUGINS
" ---------------------
call plug#begin()

" Instalar y configurar el tema gruvbox
Plug 'morhetz/gruvbox'

" Instalar NERDTree para explorar archivos
Plug 'scrooloose/nerdtree'

" Instalar el complemento para autocompletar código
Plug 'neoclide/coc.nvim', {'branch': 'release'}

" Finaliza la configuración de plugins
call plug#end()

" ---------------------
" 3. CONFIGURACIÓN PERSONALIZADA
" ---------------------
let mapleader=" "       " Establecer la tecla líder a espacio

" Mapeo para guardar archivo
nmap <C-s> :w<CR>

" Mapeo para buscar archivos con Telescope
nmap <leader>ff <cmd>Telescope find_files<cr>

" Mapeo para abrir NERDTree
nmap <leader>nt :NERDTreeToggle<CR>

" ---------------------
" 4. TRANSPARENCIA DE FONDO
" ---------------------
function! TransparentBackground()
    highlight Normal guibg=NONE ctermbg=NONE
    highlight LineNr guibg=NONE ctermbg=NONE
    set fillchars+=vert:\│
    highlight WinSeparator gui=NONE guibg=NONE guifg=#444444 cterm=NONE ctermbg=NONE ctermfg=gray
    highlight VertSplit gui=NONE guibg=NONE guifg=#444444 cterm=NONE ctermbg=NONE ctermfg=gray
endfunction

" Activar el fondo transparente
augroup MyColors
    autocmd!
    autocmd ColorScheme * call TransparentBackground() 
augroup END

" Usar el tema OneDark

" Recargar automáticamente al guardar el archivo init.vim
autocmd BufWritePost $MYVIMRC source $MYVIMRC

call plug#begin('~/.local/share/nvim/plugged')
" Instalar nvim-tree.lua
Plug 'kyazdani42/nvim-tree.lua'
call plug#end()

" Configuración para nvim-tree
let g:nvim_tree_auto_open = 1 " Abrir automáticamente cuando abres Neovim
let g:nvim_tree_auto_close = 1 " Cerrar cuando no hay más archivos abiertos
let g:nvim_tree_quit_on_open = 1 " Cerrar el árbol al abrir un archivo

" Mapear una tecla para abrir el árbol de archivos
nmap <Leader>e :NvimTreeToggle<CR>  " Abre y cierra el árbol de archivos con <Leader> + e



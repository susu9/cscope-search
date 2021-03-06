# cscope-search
Search a word through cscope egrep (It's fast!!)

![cscope-search-demo-small](https://user-images.githubusercontent.com/6793352/90325216-ac921a80-df2d-11ea-9954-f4a32f3e0baf.gif)

## Installation
### Manually download
Copy the autoload and plugin folder to ~/.vim

### Use vim-plug
Add Plug 'susu9/cscope-search' to .vimrc

```vim
call plug#begin('~/.vim/plugged')
Plug 'susu9/cscope-search'
call plug#end()
```

## Commands

| Command                             | Description                                                        |
| ----------------------------------- | ------------------------------------------------------------------ |
| `CscopeSearch`                      | Input and seach a word                                             |
| `CscopeSearchHistory`               | Select and repeat a search by history                            |
| `CscopeSearchLast`                  | Repeat the latest search |

## Global options

| Flag                              | Default                           | Description                                            |
| --------------------------------- | --------------------------------- | ------------------------------------------------------ |
| `g:cscope_search_history_size`    | 15                                | How many search commands you want to keep              |
| `g:cscope_search_prevent_jump`    | 1                                 | Prevent automatically jump to the first search result when quickfix is enable |

## vimrc configuration
Example
```vim
set cscopequickfix=s-,f-,g-,c-,d-,i-,t-,e-
nnoremap <C-f> :CscopeSearch<CR>
nnoremap <C-h> :CscopeSearchHistory<CR>
nnoremap <C-l> :CscopeSearchLast<CR>
autocmd QuickFixCmdPost [^l]* nested botright cwindow 6
```

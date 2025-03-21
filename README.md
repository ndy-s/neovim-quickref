# Neovim Cheat Sheet
A personalized quick-reference guide for mastering Neovim’s essential commands and workflows.

## Navigation
- `Ctrl-]`: Jump to definition or references
- `Ctrl-o`: Return to previous location after a jump
- `<Enter>`: Open link (in help section)
- `K`: Look up documentation or information for word under cursor
- `gg`: Go to first line in document
- `G`: Go to last line in document
- `<number>G`: Go to specific line number (e.g., `5G` for line 5)
- `0`: Move to start of the line
- `$`: Move to end of the line
- `^`: Move to start of the sentence (first non-whitespace character)
- `%`: Jump to matching parenthesis, bracket, or brace
- `h`: Move cursor left
- `j`: Move cursor down
- `k`: Move cursor up
- `l`: Move cursor right
- `Ctrl+g`: Show file location and status
- `Ctrl+w`: Window navigation (e.g., `Ctrl+w h/j/k/l` to move between splits)

## Editing
- `i`: Insert text before cursor
- `a`: Append text after cursor
- `A`: Append text at end of line
- `o`: Open new line below cursor and enter insert mode
- `O`: Open new line above cursor and enter insert mode
- `x`: Delete character under cursor
- `dw`: Delete from cursor to start of next word
- `de`: Delete from cursor to end of current word
- `d$`: Delete from cursor to end of line
- `dd`: Delete entire current line
- `r`: Replace character under cursor with another character
- `R`: Replace multiple characters (enter replace mode)
- `ce`: Change from cursor to end of current word
- `c$`: Change from cursor to end of line
- `cw`: Change from cursor to start of next word
- `u`: Undo last change
- `U`: Undo all changes on current line
- `Ctrl+r`: Redo undone change

### Motion Formula
```
operator + [count/number] + motion
```
Examples: `d2w` (delete 2 words), `c3e` (change 3 words to end)

## Copy & Pasting
- `y`: Yank (copy) selected text or motion (e.g., `yw` to yank a word)
- `p`: Paste after cursor
- `P`: Paste before cursor

## Visual Mode
- `v`: Enter visual mode (character-wise selection)
- `V`: Enter visual mode (line-wise selection) *Note: Added as a common companion to `v`*

## Search
- `/<search>`: Search forward for `<search>`
- `?<search>`: Search backward for `<search>`
- `/<search>\c`: Search forward, case-insensitive
- `n`: Go to next search result
- `N`: Go to previous search result (reverse direction)

## Find & Replace
- `:s/<old>/<new>`: Replace first occurrence of `<old>` with `<new>` in current line
- `:s/<old>/<new>/g`: Replace all occurrences in current line
- `:<start>,<end>s/<old>/<new>/g`: Replace all occurrences between lines `<start>` and `<end>` (e.g., `:1,5s/old/new/g`)
- `:%s/<old>/<new>/g`: Replace all occurrences in entire file
- `:%s/<old>/<new>/gc`: Replace all occurrences in file with confirmation prompt

## File Operations
- `:r <file>`: Read and insert contents of `<file>` below cursor
- `:e`: Edit a file (e.g., `:e filename`) + `Ctrl+d` or `Tab` for completion

## External Commands
- `:!<command>`: Execute external shell command (e.g., `:!ls` or `:!git status`)
- `:r !<command>`: Insert output of external command below cursor (e.g., `:r !ls`)

## Options
- `:set ic`: Enable case-insensitive search
- `:set hls is`: Enable search highlighting and incremental search
- `:set noic`: Disable case-insensitive search
- `:set invic`: Toggle case-insensitive search
- `:nohlsearch`: Clear search highlighting

## Help
- `:help`: Open help window
- `:help w`: Open help for the `w` command (or any topic)

## Saving Selection
- `v<select>` + `:'<,'>w TEST`: Save selected text to a new file named `TEST`

## Configuration
- `init.vim`: Neovim configuration file (typically at `~/.config/nvim/init.vim`)

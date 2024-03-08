# vim-cheat

# Sway and VIM
key | desc
---|---
`meta`-`1`,`2`,`3` 	|	switch workspaces
`meta`-`shift`-`1`,`2`,`3` |	move window to workspace
meta-shift-c |	reload sway (ctrl-o in nano to save config)
meta-enter	|	open terminal
meta-d	|	open launcher (esc to dismiss)
meta-f	|	window to full screen
meta-minus	|	scratchpad stuff
meta-shift-minus	|
meta-shift-arrow	| move window /tiling
meta-r	|	resize




# VIM
## Normal Mode
key | desc
---|---
`h`,`j`,`k`,`l` |move
`gj`,`gjk` |move one display line
`.`| repeat
`w`| move forward to start of word
`b`| move back to start of word
`e` |move forward to end of word
`ge` |backward to end of previous word
`ea`| append to current word
`gea`| append prev word
`W`,`B`,`E`,`gE`| as above but WORD (only whitespace)
0 | - 
`u`| undo
`<C-r>`| redo
g;/u<C-r>| move to last change
|
f{char}| find forward in line (curson on match)
t{char} |til find forward in line (cursor before match)
;| repeat last char find
, back up
dt{char} delete until {char}
D delete to end of line (=== d$)
cc delete line and insert

<C-u> page up (or shift-up)
<C-d> page down (or shift-down)
{,} jump to start of next/previous paragraph
% jump to matching block (parenthesis, if/endif etc)
$ end of line
_ start of text
0 start of line
:76 go line 76
G go end of file
gg go start of file
ciw replace in word insert
ci" replace in quote insert
dw delete to end of word
daw delete a word (inside)
db delete back a word
d$ delete to end of line
d0 delete to start of line
dd delete line (cut into register 0)
y yank (copy to register 0)
yy yank line
yt, yank to character (,)
p paste
"0p paste from yank register
"+p paste from system clipboard
"+P
"+Y yank to sys clipboard
i insert mode
I insert at start of line
a append to insert mode
A append end of line into insert mode
o add line and insert mode (can be anywhere in line)
O insert line above
zz recenter screen at cursor

xp transpose next two characters (delete paste)
ddp transpose this line and next
yyp duplicate line

## Searching
/text<CR> search text
* search word under cursor
n next match
cw change word (then n to find next then . to change again)
N previous match
gn select next match in visual mode
gnc change next match

<C-r><C-w> expand search term to whole word
<C-r>" paste buffer into search term
<C-r>+ paste sys clip into search term
<C-l> clear search highlights
:%s/replace/Replace/g  global search and replace
:%s/replace/Replace/gc prompt global search and replace (y,n,q,a)


## Miscellaneous
<C-a>, <C-x> jump to next number add/subtract
180<C-a> jump to next number add 180
list of numbers 0), select in visual mode then g<C-a> to increment all

:6t. copy line 6 to below current line
:t6 copy current line to below line 6
:6m. move line 6 to below current line
:m6 move current line to below line 6
:read !{cmd} Execute {cmd} in the shell and insert its standard output below the cursor
:edit index.html open file
:edit %:h<tab> open file in current file dir
:set ignorecase
:set noignorecase
:set ignorecase! toggle
:set ignorecase? status
:set ignorecase& set default
:abbr @@ dferguson@gmail.com (autocomplete)

=ip auto indent paragraph
== auto indent current line
>> indent line
<< unindent line

mm mark
`m return to mark
mM/`M global mark (file) mark before file diving eg :vimgrep
`H goto editing homer config on unraid

<C-i>, <C-o> forward/back in jump list

gf goto file under cursor
:set path? check path
<C-]> goto definition (setup?)

## Window/buffer management
:ls list buffers
:e! revert changes (reread file)
<C-6> switch between open buffers/files
<C-w><C-w> switch focus between windows
<C-w><C-hjkl> switch focus in direction
<C-w><C-s> split horiz
<C-w><C-v> split vert
:sp file horiz split load file
:vsp file vert split load file
:clo close current window
:on close all except current window

## Tab management
<C-w>T Move the current window into its own tab
:tabc Close the current tab page and all of its windows
2gt Switch to tab page number 2
gt Switch to the next tab page
gT Switch to the previous tab page

## Netrw file management
vim .
:edit ./path
:E dir of active buffer
:e. dir of current working

<-> cd ..
/match<CR> move to search

## Command line
nvim -d file1 file2


## Visual Mode
<C-[> esc
v visual mode
V visual line mode
o move to front/end of visual block
c change selection (delete then insert)
d cut
y copy
"+y copy to sys clipboard 
<,> indent (. to repeat, u to undo)
gv select last visual block
: pre-populate selection
:m0 move selection to front of file
:m$ move selection to end of file
:normal i// comment all selected lines
:normal i# comment all selected lines
:!sort
{,} jump to start of next/previous paragraph
vip select current paragraph
= autoindent

Insert Mode (also command mode :)
<C-[> esc
<C-r>0 paste
<C-o>zz one-shot command
<C-w> delete back one word
<C-u> delete back to start of line
<C-t> indent tab
<C-d> unindent 
<C-n> autocomplete
<C-x><C-k> dictionary lookup
<C-x><C-l> whole line lookup
<C-x><C-p> partial lookup
<C-x><C-f> filename completion
:cd /mnt cd to directory for completion
<C-x><C-o> omni completion
:set spell
:set nospell
<C-x><C-s> spell fix

 https://quickref.me/vim


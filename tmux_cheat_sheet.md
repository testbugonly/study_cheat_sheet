## tmux cheatsheet


### start:
`tmux`

start with session name:

`tmux new -s session_name`

list sessions:

`tmux ls`

kill session:

`tmux kill-session -t session_name`

kill all:

`tmux kill-server`

detach from session:

`tmux detach`

attach to sessions:

`tmux attach`

`tmux attach -t your_session_name`

`tmux switch -t your_session_name`


>>>Tmux has three layers of concept: session, windows, and pane.
>>>Each tmux command will open a session, each session can open multiple windows, each window can open multiple panes.

### The prefix (press **`ctrl+b`**),then press shortcuts:

Sessions:

create a new session:

`:new-session`

switch to the previous session:

`(`

switch to the next session:

`)`

Display sessions list:

`s`

rename session:

`$`

background:

`d`

### tmux windows

help:

`?`

create a new window:

`c`

switch previos session:

`p`

switch next session:

`n`

switch to a window using a number(0-9):

`2`

choose a window from an interactive list:

`w`

close a window:

`exit`

rename the window:

`,`

delete window:

`&`

search in multiple windows:

`f`

switch between two adjacent windows:

`l`

Enable scroll (`q` to exit scrollig):

`[`

### tmux panes

Split the active pane horizontally:

`"`

Split the active pane vertically:

`%`

Switch to another pane:

`the_arrow_key`

Resize the active pane:

`ALT+the_arrow_key`

Zoom in,or exit zoom mode:

`z`

close pane:

`x`

Display panes number:

`q`

Select the next panel in the current window:

`o`

### Config file

`vi ~/.tmux.conf`

You can change the prefix shortcuts,like:

```
set-option -g prefix C-a
unbind-key C-b
bind-key C-a send-prefix

set -g history-limit 10000
```

set VI mode in tmux:

`set-window-option -g mode-keys vi`

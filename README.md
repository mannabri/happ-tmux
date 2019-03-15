# happy-tmux

> tmux is a terminal multiplexer: it enables a number of terminals to be created,
accessed, and controlled from a single screen. tmux may be detached from a
screen and continue running in the background, then later reattached.
[~ github.com/tmux](https://github.com/tmux/tmux/wiki)

tmux is customizable in every way, so I decided to change a couple of things. 
Apply this configuration and you will experience happy tmux sessions. Or just 
take a bit and leave the rest ;) 

### Features

* Prefix key is set to `C-Space`. 
You don't need the space key for any other shortcut and it's huge, you won't miss.
* Toggle mouse mode (on/off) with `C-Space m`. 
By default it's off which means you can mark and copy text with your mouse.
When it's is on it allows you to scroll, resize panes and change windows with your mouse.
* Splitting panes with `C-Space |` for vertical and `C-Space -` for horizontal splits. 
* Theme color is set to `blue`. 
I don't like the default green, don't ask me why. 
* Reload the config file with `C-Space r`. 
If you try out new things in your config, you don't want to miss this.
* Don't rename windows automatically. 


### Cheatsheet

Start a new session

```sh
$ tmux
$ tmux new -s <session_name>
```

Show active sessions

```sh
$ tmux ls
```

Attach to a session

```sh
$ tmux attach -t <session_name>
$ tmux attach -t <session_id>
```

Rename a session

```sh
$ tmux rename-session -t <session_name> <new_session_name>
$ tmux rename-session -t <session_id> <new_session_name>
```

Kill a session

```sh
$ tmux kill-session -t 
```

Operate a session

command | key
--- | ---
detach from session | `C-Space d`
new window | `C-Space c`
rename window | `C-Space ,`
jump to window | `C-Space <window_id>`
split vertical | `C-Space \|`
split horizontal | `C-Space -`

### Installation
Copy the config file to your home directory: `~/.tmux.conf`

Then, reload the configuration by running 
`$ tmux source-file ~/.tmux.conf`

Open a new tmux session and enjoy :)

# tmux Session Manager

This script allows you to manage tmux sessions with ease by selecting a working
directory interactively using `fzf`. It checks if a tmux session exists for the
selected directory and attaches to it, or it creates a new session if it doesn't
exist.

## Features

- Interactive selection of a directory within `$HOME/Developer` using `fzf`.
- Attaches to an existing tmux session or creates a new one.
- Supports attaching to tmux sessions both inside or outside of tmux.
- Automatically sets the tmux working directory to the selected directory.

## Requirements

- [tmux](https://github.com/tmux/tmux) - A terminal multiplexer.
- [fzf](https://github.com/junegunn/fzf) - A command-line fuzzy finder.
- Bash shell.

## Installation

1. Clone this repository:

```bash

git clone https://github.com/akshikrm/tmux-session-manager.git cd tmux-session-manager

```

2. Make the script executable:

```bash

chmod +x sessy

```

3. (Optional) Add it to your `PATH` for global access:

## Usage

Run the script with the following command:

```bash

bash ./sessy

```

This will prompt you to choose a directory within `$HOME/Developer` and will
either attach to the corresponding tmux session or create a new one if it
doesn't exist.

### Inside tmux

If you're already inside a tmux session, the script will switch to the selected
session using `tmux switch-client`.

### Outside tmux

If you're outside of tmux, the script will attach to the selected tmux session
using `tmux attach-session`.

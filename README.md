# tmux-start

Start tmux with a sesson and windows.

Syntax:

    tmux-start <session-name> [window-name [window-keys]] ...

Example:

    tmux-start mysession mywindow1 ls mywindow2 date

The example does this:

  * If the session name "mysession" exists, then attach and exit.

  * Create a new session with name "mysesssion".

  * Create a window name "mywindow1".

  * Send the keys "ls" followed by a return;
    this command lists the files in the directory.

  * Create a window name "mywindow2".

  * Send the keys "date" followed by a return;
    this command shows the current date and time.


## What this does

If the session name already exists, then attach and exit.

Create a new session with a session name by using the first arg,
and create each window and its keys by using the rest of the args.

Finally, select the first window, because its our preference.


## Install

Option 1: download the file to wherever you want, then make it executable.

    cd /usr/local/bin/
    sudo curl -O https://raw.githubusercontent.com/SixArm/tmux-start/master/tmux-start
    sudo chmod +x tmux-start

Option 2: clone the repo to anywhere you want, then add it to your path.

    cd /anywhere/you/want
    git clone https://github.com/SixArm/tmux-start.git   
    export PATH="$PATH:/anywhere/you/want/tmux-start"

If you would like to help us by writing a package for any popular package manager, such as apt, yum, brew, etc., we wecome help.


## Comparisons

The [tmuxinator](https://github.com/tmuxinator/tmuxinator) program
can manage complex tmux sessions easily, such as by using YAML files,
and providing split screen, project hooks, completions, and more.


## Project goals

Short and simple-- easy to understand.

Free open source-- easy to modify.

POSIX shell usability-- easy to run anywhere.


## Tracking

* Program: tmux-start
* Version: 5.0.0
* Created: 2013-08-02T00:00:00Z
* Updated: 2021-10-28T16:40:50Z
* License: GPL-2.0-or-greater or contact us for custom license
* Contact: Joel Parker Henderson (joel@joelparkerhenderson.com)

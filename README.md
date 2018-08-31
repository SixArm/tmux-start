# tmux-start

Start tmux with a sesson and windows.

Syntax:

    tmux-start <session-name> [window-name] ...

Example:

    tmux-start mysession mywindow1 hello mywindow2 world

The example does this:

  * Create a session name "mysession",
    or if the session name already exists,
    then attach to the existing session.

  * Create a window name "mywindow1" and send the
    keys "hello" and a return character.

  * Create a window name "mywindow2" and send the
    keys "world" and a return character.


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


## What this script does

The script creates the session "session-name".

If the session name already exists, then the
script attaches to it i.e. to the existing session.

The script creates windows, starting at window 1.

The script sets a window's name as per the command args,
then sends the window the keys as per the command args.

When the session is running and all the windows are ready,
then the script selects window 1, and window 2 as the previous.
This is because we typically want the first window active,
and we want the second window to be available by one key.


## Comparisons

The [tmuxinator](https://github.com/tmuxinator/tmuxinator) program
can manage complex tmux sessions easily, such as by using YAML files,
and providing split screen, project hooks, completions, and more.
The program is implemented via a Ruby gem.


## Tracking

* Program: tmux-start
* Version: 4.0.2
* Created: 2013-08-02
* Updated: 2018-08-29
* License: GPL
* Contact: Joel Parker Henderson (joel@joelparkerhenderson.com)

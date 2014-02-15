bpython-blessings - A fancy blessings interface to the Python interactive interpreter
=====================================================================================

Dependencies
------------

Pygments

```
apt-get install python-pygments
```

Sphinx != 1.1.2 (for the documentation only)

```
apt-get install python-sphinx
```

Introduction
------------

This project is a fork of [bpython](http://bpython-interpreter.org/).

The goal is to get something with most of bpython's features which doesn't run in fullscreen mode.

Features
--------

*   Blessings!
    
    Instead of going fullscreen using curses and flushing everything to stdout on exit, bpython-blessings uses blessings. This means it can do the fancy things mentioned below without disrupting your terminal's UI.

*   In-line syntax highlighting.
    
    This uses Pygments for lexing the code as you type, and colours
    appropriately. Pygments does a great job of doing all of the tricky stuff
    and really leaving me with very little to do except format the tokens in
    all my favourite colours.

*   zsh-like autocomplete.
    
    With the fullscreen gone, the “suggestions displayed as you type” feature has to go as well. Instead, you can hit tab to get menu completion.

*   Expected parameter list.
    
    This will be integrated into the zsh-style menu completion.

*   Rewind.
    
    The sky is the limit, or in this case the screen. You can only rewind until you hit the upper edge of the screen, because anything else looks weird in scrollback.

*   Pastebin code/write to file.
    
    I don't really use the save thing much, but the pastebin thing's great. Hit
    a key and what you see on the screen will be sent to a pastebin and a URL
    is returned for you to do what you like with. I've hardcoded
    paste.pocoo.org in for now, that needs to be fixed so it's configurable.
    Next release, I promise.

Configuration
-------------

See the sample-config file for a list of available options.  You should save
your config file as ~/.config/bpython/config (i.e
$XDG_CONFIG_HOME/bpython/config) or specify at the command line::

```
bpython --config /path/to/bpython/config
```

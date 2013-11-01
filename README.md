todotxt-machine
===============

todotxt-machine is an interactive terminal based [todo.txt](http://todotxt.com/) file editor with an interface similar to [mutt](http://www.mutt.org/). It follows [the todo.txt
format](https://github.com/ginatrapani/todo.txt-cli/wiki/The-Todo.txt-Format) and stores todo items in plain text.

Screenshots
-----------

View your todos in a list with helpful syntax highlighting:

[![screenshot1.png](https://raw.github.com/AnthonyDiGirolamo/todotxt-machine/master/screenshots/screenshot1.png)](https://raw.github.com/AnthonyDiGirolamo/todotxt-machine/master/screenshots/screenshot1.png)

Sort in ascending or descending order, or keep things unsorted:

[![screenshot3.png](https://raw.github.com/AnthonyDiGirolamo/todotxt-machine/master/screenshots/screenshot3.png)](https://raw.github.com/AnthonyDiGirolamo/todotxt-machine/master/screenshots/screenshot3.png)

Filter contexts and projects:

[![screenshot2.png](https://raw.github.com/AnthonyDiGirolamo/todotxt-machine/master/screenshots/screenshot2.png)](https://raw.github.com/AnthonyDiGirolamo/todotxt-machine/master/screenshots/screenshot2.png)

And some quotes for when you have nothing left to do:

[![screenshot_quote1.png](https://raw.github.com/AnthonyDiGirolamo/todotxt-machine/master/screenshots/screenshot_quote1.png)](https://raw.github.com/AnthonyDiGirolamo/todotxt-machine/master/screenshots/screenshot_quote1.png)

[![screenshot_quote2.png](https://raw.github.com/AnthonyDiGirolamo/todotxt-machine/master/screenshots/screenshot_quote2.png)](https://raw.github.com/AnthonyDiGirolamo/todotxt-machine/master/screenshots/screenshot_quote2.png)

Requirements
------------

Python 2.7.5 or Python 3.3.2 with readline support on Linux or Mac OS X.
todotxt-machine outputs raw [terminal control
sequences](http://invisible-island.net/xterm/ctlseqs/ctlseqs.html) to draw its
interface and does not rely on modules like
[curses](http://docs.python.org/3.3/library/curses.html) or
[urwid](http://excess.org/urwid/).

Installation
------------

    pip install todotxt-machine

Command Line Options
--------------------

    usage: todotxt-machine.py [-h] [-f FILE] [--readline-editing-mode {emacs,vi}]

    Interactive terminal interface for todo.txt files.

    optional arguments:
      -h, --help            show this help message and exit
      -f FILE, --file FILE  path to your todo.txt file
                            default:~/Dropbox/todo/todo.txt
      --readline-editing-mode {emacs,vi}
                            set readline editing-mode

Key Bindings
------------

### General

    ?            - display this help message
    q, ctrl-c    - quit

### Movement

    j, down      - move selection down
    k, up        - move selection up
    g, page up   - move selection to the top item
    G, page down - move selection to the bottom item

### Filtering & Sorting

    p            - select the next project
    P            - select the previous project
    c            - select the next context
    C            - select the previous context
    s            - switch sorting method

### Manipulating Todo Items

    x            - complete / un-complete selected todo item
    n            - add a new todo to the end of the list
    o            - add a todo after the selected todo
    O            - add a todo before the selected todo
    enter, A, e  - edit the selected todo
    D            - delete the selected todo

### While Editing a Todo

    ctrl-c       - cancel editing a todo
    tab          - tab complete @contexts and +Projects

Planned Features
----------------

- User defined color themes
- Manual reordering of todo items
- Searching with fuzzy matching


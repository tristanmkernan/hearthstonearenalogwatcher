=============================
Hearthstone Arena Log Watcher
=============================
To use (with caution), simply do::

    >>> from hearthstonearenalogwatcher import HearthstoneArenaLogWatcher
    >>> halw = HearthstoneArenaLogLocation(log_folder="log folder")
    >>> for event in halw.event_generator(speed=1):  # get events at most once per second (rate = 1 / speed)
    >>> if event.type == HearthstoneArenaLogWatcher.Event.ENTERED_ARENA:
    >>>     # event.date is an ArenaDraft object, containing hero, drafted cards, and whether the draft is over.
    >>>     arena_state = event.data
    >>>     # do something interesting
    >>> elif event.type == HearthstoneArenaLogWatcher.Event.EXITED_ARENA:
    >>>     pass

And so on for the following events:
- ENTERED_ARENA
- EXITED_ARENA
- HERO_SELECTED
- CARD_DRAFTED
- DRAFT_ENDED

It's that simple!

Errors
^^^^^^
FileNotFoundError
*****************
Raised when the passed parameter ``log_location`` is invalid and a log file is attempted to be accessed.

Tests and Examples
^^^^^^^^^^^^^^^^^^
Todo: make some tests and examples!

License
^^^^^^^
The MIT License (MIT)

Copyright (c) 2016 Tristan Kernan

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and
associated documentation files (the "Software"), to deal in the Software without restriction, including without
limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the
Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial
portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT
LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE
OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
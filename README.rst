=============================
BinaryOrNot
=============================

.. image:: https://badge.fury.io/py/binaryornot.png
    :target: http://badge.fury.io/py/binaryornot
    
.. image:: https://travis-ci.org/audreyr/binaryornot.png?branch=master
        :target: https://travis-ci.org/audreyr/binaryornot

.. image:: https://readthedocs.org/projects/binaryornot/badge/?version=latest
        :target: https://readthedocs.org/projects/binaryornot/?badge=latest
        :alt: Documentation Status


Ultra-lightweight pure Python package to guess whether a file is binary or text,
using a heuristic similar to Perl's `pp_fttext` and its analysis by @eliben.

* Free software: BSD license
* Documentation: http://binaryornot.readthedocs.org

Status
------

It works, and people are using this package in various places. But it doesn't cover all edge cases yet.

The code could be improved. Pull requests welcome! As of now, it is based on these snippets, but that may change:

* http://stackoverflow.com/questions/898669/how-can-i-detect-if-a-file-is-binary-non-text-in-python
* http://stackoverflow.com/questions/1446549/how-to-identify-binary-and-text-files-using-python
* http://code.activestate.com/recipes/173220/
* http://eli.thegreenplace.net/2011/10/19/perls-guess-if-file-is-text-or-binary-implemented-in-python/

Features
--------

Has tests for these file types:

* Text: .txt, .css, .json, .svg, .js, .lua, .pl, .rst
* Binary: .png, .gif, .jpg, .tiff, .bmp, .DS_Store, .eot, .otf, .ttf, .woff, .rgb

Has tests for numerous encodings.

Why?
----

You may be thinking, "I can write this in 2 lines of code?!"

It's actually not that easy. Here's a great article about how *perldoc*'s
heuristic to guess file types works: http://eli.thegreenplace.net/2011/10/19/perls-guess-if-file-is-text-or-binary-implemented-in-python/

And that's just where we started. Over time, we've found more edge cases and
our heuristic has gotten more complex.

Also, this package saves you from having to write and thoroughly test
your code with all sorts of weird file types and encodings, cross-platform.

Credits
-------

* Special thanks to Eli Bendersky (@eliben) for his writeup explaining the heuristic and his implementation, which this is largely based on.
* Source code from the portion of Perl's `pp_fttext` that checks for textiness: https://github.com/Perl/perl5/blob/v5.23.1/pp_sys.c#L3527-L3587

Laxative - Debian packaging helper
==================================

Building laxative
-----------------

Clone this repository, then:

    sudo apt-get install $(grep Build-Depends debian/control | sed -r -e 's/.*: //;s/,//g;s/\s*\([^)]+\)//g')
    dpkg-buildpackage -b

Installing laxative
-------------------

After building with the instructions above:

    sudo debi
    sudo apt-get install -yf

Note: the first command may produce errors if you don't have the appropriate
dependencies available. The second command should automatically install any
that are missing.

Using laxative
--------------

Laxative comes with a set of man pages. Run `man lax' after you have
installed it to get started.

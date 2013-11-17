gtmsu_servicemenu
=================

A GUI application that allows you to tag your files to organize them.

![alt text](http://mooos.org/scr/111723.png "gtmsu_servicemenu")

Includes [tmsu][3].

Includes KDE service menus.

Depends on: zenity, go-sqlite3, go-fuse, kdebase-dolphin

Install with
------------

    $ makepkg -sfi PKGBUILD

example:
    
     $ rm -r ~/abs/gtmsu_servicemenu && mkdir -p ~/abs/gtmsu_servicemenu && cd ~/abs/gtmsu_servicemenu && wget https://raw.github.com/idk/gtmsu_servicemenu/master/PKGBUILD && makepkg -sfi

Remove with
-----------

    # pacman -R gtmsu_servicemenu

Run with
--------

In dolphin right click context menu adds 'Tag file(s)' and 'Tagging Options'

In other file managers add these to context menu: 
gtmsu tag %U
gtmsu edit
gtmsu mount
gtmsu db


TMSU
----

    $ tmsu help


SUPPORT
-------

[The Linux Distro Community][1]

[pdq][2]


HISTORY
-------
* 2013-11-16: Version 0.2.2

Contributing
------------

1. Fork it.
2. Create a branch (`git checkout -b my_gtmsu_servicemenu`)
3. Commit your changes (`git commit -am "Added foo and bar"`)
4. Push to the branch (`git push origin my_gtmsu_servicemenu`)
5. Create an [Issue][2] with a link to your branch
6. Join the Linux Distro Community IRC! :D

SHARE AND ENJOY!
----------------

[1]: http://www.linuxdistrocommunity.com
[2]: https://github.com/idk/gtmsu_servicemenu/issues
[3]: http://tmsu.org

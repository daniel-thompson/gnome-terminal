Terminal - with tmux
====================

Introduction
------------

This is tiny hack on top of gnome-terminal that automatically enables support
for tmux (default) keybindings whenever the terminal is running in a window
without tabs. The changes feel great under the fingers but, unfortunately,
so far I haven't really come up with a way to reconcile this with the GNOME
preferences ethos. For that reason it will remain a hack for the time being.

Currently the following tab shortcuts are implemented:

 * Switch to Previous Terminal
 * Switch to Next Terminal
 * Switch to Tab 1
 * Switch to Tab 2
 * ...
 * Switch to Tab 9
 * Switch to Tab 10

Quickstart
----------

This approach it not actually very good practice because it will potentially
clobber the version provided by the package manager (and be clobbered whenever
the package manager installs an update). However it has the advantage the
autoconf easily find the gnome-shell search provider...

    ./autogen.sh --prefix=/usr
    make
    sudo make install

On F21 the build requires (at least) the following packages:

    appdata-tools dconf-devel nautilus-devel vte291-devel

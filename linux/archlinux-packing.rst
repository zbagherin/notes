Packing
=======

REF
---

-  https://wiki.archlinux.org/index.php/DeveloperWiki:Building\_in\_a\_Clean\_Chroot

pacman
------

yaourt
------

PKGBUILD
--------

::

    # Set up chroot envirnment
    pacman -S devtools
    mkdir ~/chroot
    CHROOT=$HOME/chroot
    mkarchroot $CHROOT/root base base-devel

    # Update packages in chroot
    arch-nspawn $CHROOT/root pacman -Syu

    # Run from the dir containing the PKGBUILD: 
    makechrootpkg -c -r $CHROOT

Build in Chroot
---------------

devtools
--------

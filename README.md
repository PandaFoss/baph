# baph - Basic AUR Package Helper


#### Features

- minimal requirements.
- search for packages matching a query.
- optionally view and confirm the PKGBUILD for each package.
- handles complex dependency chains including other AUR packages.
- import and locally trust PGP keys required for signed AUR packages


#### Installation

A makefile is provided to make install and removal easy
run `make install` *(as root if needed)*, `make uninstall` to remove.

#### What is it

baph provides a simple way to search, install, and update AUR packages.
It is not a package manager, beyond simple operations you should still use `pacman`

---

This program follows the package build process described
[here](https://wiki.archlinux.org/index.php/Arch_User_Repository#Installing_packages)
and [here](https://wiki.archlinux.org/index.php/Makepkg)


See `man baph` for usage and more details

NOTE: This is a fork of [this](https://bitbucket.org/natemaia/baph) repository.

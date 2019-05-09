# baph - Basic AUR Package Helper

A simple AUR package helper for Arch Linux written in bash.


#### Features

- Minimal requirements.
- Search for packages matching a query.
- Optionally view and confirm the PKGBUILD for each package.
- Handles complex dependency chains including other AUR packages.
- Import and locally trust PGP keys required for signed AUR packages


#### Installation

Clone this repo and copy `baph` to somewhere on your `$PATH`, usually `/usr/bin/`

```
git clone https://bitbucket.org/natemaia/baph.git

sudo cp baph/baph /usr/bin/baph
```

---


#### What is it

A way to search, install, and update AUR packages. It is not a replacement for `pacman`, beyond simple operations you should use `pacman`

---

This program follows the local package build process for Arch Linux described
[here](https://wiki.archlinux.org/index.php/Arch_User_Repository#Installing_packages)
and [here](https://wiki.archlinux.org/index.php/Makepkg)


---

#### Usage

Argument types are as follows: `{}` basic, `[]` optional, `<>` required.


```

 baph - Simple helper to search, install, and update AUR packages

 usage: baph <operation> [options] [package(s)]

 operations:
     baph {-h --help}
     baph {-v --version}
     baph {-s --search}  <query>
     baph {-u --update}  [options] [package(s)]
     baph {-i --install} [options] <package(s)>

 options:
     --noview, -n       Skip viewing PKGBUILD files
     --auronly, -a      Only operate on AUR packages
     --noconfirm, -N    Skip confirmation dialogs

 examples:
     install 'google-chrome' and 'yay' from the AUR
         baph -i google-chrome yay

     search for AUR packages matching 'cmus'
         baph -s cmus

     update only the AUR packages on the system, skip view/confirm dialogs
         baph -uanN

```

---

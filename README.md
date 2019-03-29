phidget22networkserver
===
> network server for Phidget devices

This repository containes sources of an Arch Linux (pacman) package, see [PKGBUILD](https://wiki.archlinux.org/index.php/PKGBUILD) for details. Being opinionated and special-purpose, it is not published on the AUR (Arch User Repository), but instead is part of a [collection of atomic configuration snippets](https://github.com/regaur) I use to build Arch-based systems.

Build
---

```
makepkg -cd --sign
ssb-pacman-import-local x86_64 regular phidget22networkserver-STUFF.pkg.tar.xz
```

See Also
---

- [ssb-pacman](https://github.com/regular/ssb-pacman)
- [ssb-archiso](https://github.com/regular/ssb-archiso)

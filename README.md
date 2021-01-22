# xb

A simple wrapper for the [XBPS Package Manager](https://docs.voidlinux.org/xbps/index.html) used in [Void Linux](https://voidlinux.org/), written in Python.

Heavily inspired by [Yay](https://github.com/Jguer/yay) for Arch, my goal with xb was to make basic searching and installing via xbps a bit easier.

Very much a work-in-progress, I'll be updating as I can.

## Installation

Just `chmod +x` and throw it in your PATH somewhere.

Currently the only dependency besides Python3 is sudo.

## Usage:
`xb [ <pkgname(s)> | -s <keyword(s)> | -r <pkgname(s)> ]`

### Examples:
`xb <pkgname>`
- If `<pkgname>` matches a valid package name, that package is installed directly.  
  Otherwise, a search is performed.

`xb <pkg> <pkg> ...`  
- When multiple arguments are specified, they are assumed to be exact package names,  
  and `xb` will attempt to install them all (mirroring `xbps-install` functionality).

`xb -s <keyword(s)>`  
- Performs a search using specified keyword(s) to refine results.

`xb -r <pkgname(s)>`  
- Removes specified packages (mirrors `xbps-remove` functionality).

`xb`  
- Calling `xb` with no arguments will perform a repository sync and full system update.

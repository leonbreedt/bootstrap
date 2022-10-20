# bootstrap

Repository containing bootstrap scripts to set up your Mac, from clean install
to fully configured.

## Goals

- A single script is executed once to perform all setup actions, run as the
  very first thing after a clean install

- No dependency on pre-installing anything such as a particular shell version,
  Homebrew, etc.

- No manual actions required

## How it works

The scripts detect your macOS version and architecture, and download
the appropriate [syscfg](#syscfg) and [hf](#hf) static executables.

`syscfg` is used to perform system level configuration of macOS based
on your configuration file. This includes things like:

- Setting system preferences
- Modifying the Dock
- Setting wallpaper
- Installing fonts
- Installing Homebrew
- Installing the Command-Line utilities
- Installing software from .pkg files
- Installing software from .dmg files

`hf` is used to clone a Git repository that contains your dotfiles,
and can also be used like [yadm](https://yadm.io) to manage them
afterwards.

## Why static executables?

After a life-time of Linux distribution maintenance, and working with
`.dll`/.`so`/glibc hell, as well as shell scripts that don't survive a year
of operating system change, I am over depending on anything but a kernel.

Go/Rust for life.

## Can I read the source code to `syscfg` or `hf`?

Yes, of course. They are on GitHub, and licensed under the Apache 2 license.

- [syscfg](https://github.com/leonbreedt/syscfg)
- [hf](https://github.com/leonbreedt/hf)


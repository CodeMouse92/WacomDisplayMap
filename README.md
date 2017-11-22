# WacomDisplayMap

Easily map a Wacom graphics tablet to a display, without having to muck through
a bunch of device lists.

## Authors

- Jason C. McDonald (CodeMouse92)

## Compatibility

This should work on any Debian-based system, and may also work on other Linux
systems. It is designed to work automatically with any graphics tablet that can
be controlled by `xsetwacom`.

**If you encounter any problems with any Linux system or Wacom tablet, please
report in Issues!**

## History

Many Ubuntu systems include a control panel for Wacom graphics tablets, but
some popular distributions (including Ubuntu MATE) don't. This handy script
allows you to quickly map your Wacom tablet to any connected display.

## Prerequisites

You must have the package `pcregrep` installed on your system, which should be
available from your system's default package repository. You should also have
`xsetwacom` on your system, which is usually pre-installed on Ubuntu by default.

## Installation

Simply place the `wacommap` file in a convenient place for scripts, and be sure
the location is included in your environment path. Mark the script as executable
via `chmod +x wacommap`.

Here's an example install, placing the script in your `/usr/local/bin`
directory. Note that we only need the `sudo` because we're working in a system
directory.

```bash
# Move to the location where the script will live.
$ cd /usr/local/bin
# Download the script file from GitHub directly.
$ sudo wget https://github.com/CodeMouse92/WacomDisplayMap/raw/master/wacommap
# Make the script executable. (You are encouraged to read the file BEFORE doing this, so you know what it does.
$ sudo chmod +x wacommap
# Run the script.
$ wacommap
```

## Usage

Simply run `wacommap` to start the script.

First, it will search for compatible Wacom devices. If you receive the message...

> No Wacom stylus or eraser detected.

...be sure you've connected your Wacom graphics tablet to your computer.

Next, it will automatically detect all connected displays. If only one display
is detected, it will automatically select it. Otherwise, if multiple displays
are detected, it will list them and prompt you to select one.

The script will then map all compatible connected Wacom devices to the selected
display.

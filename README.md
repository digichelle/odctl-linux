# ODCtl
OneDrive service control for Linux.

## Description

This is a bash script designed to complement the unofficial [OneDrive for Linux client](https://github.com/abraunegg/onedrive) by [abraunegg](https://github.com/abraunegg/). It provides aliases for controlling the service.

## Why This Exists

Storing development project files on OneDrive is probably a bad idea. The constant creation and deletion of build artifacts wreaks havoc on the service. This is especially true of the unofficial Linux client, as it’s even less tolerant of this behavior than the official Mac and Windows clients. If you do it anyway (as I do), I strongly suggest stopping the OneDrive service before working on a development project.

Because the unofficial Linux client is implemented as a systemd service, it can be controlled with commands such as `systemctl --user stop onedrive`. If you do this as often as I do, this becomes tedious fast. This script reduces that command to a simple `odctl stop`. Much easier!

Some non-developers may benefit from this as well. For example, [Obsidian](https://obsidian.md/) users may wish to stop the OneDrive service before using the app. The app’s auto-save functionality is a touch aggressive and can overwhelm OneDrive.

[Mac](https://github.com/digichelle/odctl-mac) and [Windows](https://github.com/digichelle/odctl-win) variants also exist, should you need them.

## Requirements

- Any Linux distribution with systemd
- OneDrive for Linux by abraunegg

## Install

1. If necessary, set the executable bit on the `odctl` script (using something like `chmod 755 odctl` or `chmod a+x odctl`).
2. Copy the `odctl` script to a directory in your path. I recommend `/usr/local/bin`.

## Usage

### Start OneDrive

```
odctl start
```

### Stop OneDrive

```
odctl stop
```

### Restart OneDrive

```
odctl restart
```

### Show OneDrive Service Status

```
odctl status
```

### Show OneDrive Service Log

```
odctl log
```

### Help

```
odctl --help
```

## License

### MIT License

Copyright © 2026 Michelle Catherine Marcó

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
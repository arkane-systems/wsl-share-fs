# wsl-share-fs
Automatically share the filesystem of a distro with other WSL distros.

This is a systemd unit which automates the mounting of the distribution filesystem under the /mnt/wsl folder, which makes it available to other WSL distributions. It runs automatically when systemd starts. (See https://github.com/microsoft/WSL/issues/4654 for how this works.)

## Why?

Because I'm tired of doing it manually.

# Installation

  1. Set up the WSL Transdebian repository [following the instructions here](https://arkane-systems.github.io/wsl-transdebian/), if you have not already done so.

  2. `apt install wsl-share-fs`

  3. Either restart WSL, or `sudo systemctl start wsl-share-fs`.

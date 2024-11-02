# git-credential-with-kwallet

A git credential.helper program that stores your credentials in the KDE wallet (via DBUS).

## Set-up Guide

This set-up guide assumes that you are running a Linux distro with git and the KDE wallet installed, and that you've installed Ruby (ie. that `/bin/env ruby` finds something). It shouldn't matter which version of Ruby you have, so long as it's decently modern.

If you don't have Ruby installed, then you should install it (eg. by using `sudo snap install rbenv`). I recommend installing through rbenv instead of through your default package manager because if you start using Ruby for anything else, rbenv will make managing different versions of Ruby much easier.

*Step 1:* Download the file `git-credential-with-kwallet`, and put it somewhere in your PATH (I like to use `~/.local/bin`).

*Step 2:* Tell git about the program using the following command:

    git config --global credential.helper with-kwallet

And you're done! KDE wallet will start storing all your credentials.

## Troubleshooting & Bugs

At the moment, I believe this program works well right out of the box, but I'm sure that will change. Please let me know (by opening an issue) if it isn't working for you!

The one issue that has come up a couple times, and is likely to again, is that the qdbus executable has different names on different systems. If you want to try another executable, you can add it to the QDBUS_EXECUTABLES array. If that solves it, please let me know (or create a PR with your change)!

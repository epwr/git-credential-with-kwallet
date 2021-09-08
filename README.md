# git-credential-with-kwallet

A git credential.helper program that stores your credentials in the KDE wallet (via DBUS).

## Set-up Guide

This set-up guide assumes that you are running a Linux distro with git and the KDE wallet installed.

*Step 1:* Download the file `git-credential-with-kwallet`, and put it somewhere in your PATH.

*Step 2:* Tell git about the program using the following command:

    `git config --global credential.helper with-kwallet`

And you're done! KDE wallet will start storing all your credentials.

## Troubleshooting & Bugs

At the moment of release, this program is believed to work well right out of the box. Follow the
Set-up Guide (above) and all should be well. It all is not well, let me know! I'll update this section
with troubleshooting tips as I find out about common problems.

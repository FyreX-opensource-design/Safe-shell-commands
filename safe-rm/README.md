This script can help protect against the rm command from deleting important, or even system-critical files and folders
while there are a few options out there already. the two I found did seem to have their own issues. While one was configurable with AppleScript, it did require quite a bit of setup via the command line.
The other one didn't have any protection for if a poorly done script would end up deleting an important system folder.

Though the best way I could find to make this system-wide was to add `alias rm="/etc/safe-rm/safe-rm.sh"`, which is its install path on the system, to line 4 of ` /etc/bash.bashrc`, or somewhere above the interactive shell check.

Do note that this doesn't completely protect against bad actors, as they could simply create a user-level alias and bypass the system one entirely or go through secomp instead.

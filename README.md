# Touchpad Locking

## Description
On some hardware running Linux the touchpad locking is not working properly, which prevents the user from changing the state of the touchpad.
This can be inconvenient during typing by accidentally moving or clicking the mouse.
This repository contains a script for toggling the touchpad (lock/unlock) which can be called via a custom keyboard shortcut.

## Applying Fix

### Prepare Bash Script
Make 'touchpad' executable in case it is not already.

```
:~$ chmod +x touchpad
```

Verify the functionality of the script 'touchpad' by calling it directly.
If the touchpad was enabled, it should now be disabled and moving the mouse via the touchpad should not work.
Additionally, an notification message should appear on the screen stating the current state of the touchpad.

```
:~$ ./touchpad
```

Copy 'touchpad' to your preferred location (e.g. /usr/local/bin) once you have verified it works as intended.


### Add Keybindings
In order to toggle the touchpad (lock/unlock) via keyboard, add keybindings to 'Control Center -> Keyboard Shortcuts'.  
For example:

```
Name:		Toggle Touchpad
Command:	/bin/bash /usr/local/bin/touchpad
Shortcut:	Ctrl + F11
```

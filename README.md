# Mutli Clipboard
Switch clipboard contents using easily using a command<br />
Images, text and files are supported and unlimited amounts of saved clipboards can be created.<br />
The idea of this is to easily switch keyboards with simple commands. Map commands to keys to use this easily.

## What This Does
This acts as a hotbar in a game would. When 1 is passed and you are currently using 2 (current is saved in data.json), your clipboard contents will be saved in 2 and 1 will then be loaded; if 1 hasn't been used before, the current clipboard is kept but the data is still saved to 2.

e.g.<br />
1: 123, 2: abc, clipboard: myclipboard<br />
When currently using is 1 and you pass 2:<br />
1: myclipboard, 2: abc, clipboard: abc

Clipboards can be named more than just numbers.

## Installation/Setup
1. Install PIL if you are using Python 3 ( `pip install Pillow` )
2. Install PYQT5 ( `pip install pyqt5` )
3. Install pywin32 ( `pip install pypiwin32` or [Installer](https://sourceforge.net/projects/pywin32/files/pywin32/))

## Usage
* `clipboards.py switch [clipboard]` - Will switch current clipboard to the clipboard specified
* `clipboards.py clear` - Clear all clipboards
* `clipboards.py clear 1` - Clear clipboard 1
* `clipboards.py view` - View all clipboards (opens GUI)
* `clipboards.py view 1` - Views clipboard 1

## GUI

![GUI Example](http://i.imgur.com/dp42h1m.jpg "GUI Example")

### Usage
* Click on clipboard to switch to it (auto close feature mentioned below)
* Right click menu on each clipboard
* Clear all clipboards option
* Easy refresh
* Can add from the GUI (will pick the lowest integer)
* Displays both text and images

### Options
* Close GUI when a clipboard is selected - found in data.json:close_on_gui_select
* Keep window on top until closed - found in data.json:stay_on_top
* Display HTML as plain text instead of rendering it in the GUI - found in data.json:html_as_plain_text

### Features
* Dark stylesheet and transparent
* Dynamically displays contents of clipboards
* Will save current clipboard on startup (so you can see what the state it would be if it is switched)
* Can view all clipboard contents easily
* Easily add and remove clipboards

## Thanks to
* [Michael Robertson](https://github.com/MBRobertson) for adding file support.

## Notes
I have included RunGUI.vbs to be attached to a hot key so the GUI can easily be opened.

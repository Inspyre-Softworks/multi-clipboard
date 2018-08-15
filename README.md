# Mutli Clipboard
Switch clipboard contents using a simple GUI<br />
Images, text, files and other formats are supported with unlimited amounts of saved clipboards able to be created.<br />
The idea of this is to easily switch clipboards with a simple click in a GUI. It comes with a built in listener for Ctrl + Windows + C

![Main GUI](https://nitratine.net/images/multi-clipboard/main-gui.png)

### GUI With Settings Open

## What Is This?
This is my solution to constantly overwriting my clipboard. It is a GUI that acts like a hotbar, click on a virtual clipboard to place it on your actual clipboard. Some command line support has also been added in the form of setting and clearing clipboards.

## Getting Started

### Prerequisites
 - Python (tested on 3.4+)
 - Windows

### Installation and Usage
You can install this project using this repository by following these steps:
1. Clone/download this repo
2. Open cmd/terminal and cd to the project
3. Execute ```pip install -r requirements.txt``` and [install this if pywin32 doesn't install](https://sourceforge.net/projects/pywin32/files/pywin32/)

To run the GUI, simply run the ```multi_clipboard.py``` script with no parameters. Alternatively use ```run.vbs``` to open the GUI with no console (can be used for key shortcuts).

### GUI Usage
* Click on clipboard to switch to it (will close automatically on selection by default)
* Right click menu on each clipboard to individually delete/set
* Click on the trash to delete all clipboards
* Click on the plus button to create a new clipboard
* Settings for the GUI can be toggled easily in settings window

### Command Line Usage
* `clipboards.py` - Opens GUI
* `clipboards.py -s [clipboard]` - Will load data from that clipboard if it exists
* `clipboards.py -c *` - Delete all clipboards
* `clipboards.py -c 1` - Delete clipboard 1
* `clipboards.py --start-listener` - Starts the listener if it isn't running
* `clipboards.py --stop-listener` - Stops the listener if it's running
* `clipboards.py --current` - Check what clipboard you are currently on

## The Listener
This package has a built in listener which listens for Ctrl + Windows + C (Left control). This can be enabled in the GUI's settings under "Toggle Listener" or by arguments as described above. This also comes with a feature to make the listener start on startup. To enable this, go into the GUI's settings and click "Listener Autostart" to toggle it on/off.

## GUI With Settings Open

![Main GUI with Settings](https://nitratine.net/images/multi-clipboard/main-gui-with-settings-shown.png)

## So What Happens If...
 - I delete all clipboards? -> Clipboard 0 will be created with the current contents
 - I delete the clipboard I am currently on? -> Nothing, your clipboard will be saved back to that clipboard later.
 - I am shown an error saying my clipboard isn't supported? -> Open up an issue with details on what your clipboard contents are, we can see if it can be supported

## Thanks to
* [Michael Robertson](https://github.com/MBRobertson) for adding file support in previous versions.

## Things that still are being done
 - Convert to package format
    - Add setup.py
    - License
    - PyPI?

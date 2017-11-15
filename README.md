# PyInstaLive
![Version 2.2.7](https://img.shields.io/badge/Version-2.2.7-pink.svg?style=for-the-badge)

This script enables you to record Instagram livestreams as well as download any available replays. It is based on [another script](https://github.com/taengstagram/instagram-livestream-downloader) that has now been discontinued. 


## Quickstart

- Install the prerequisites and then PyInstaLive.
- Run `pyinstalive -c` to generate a configuration file.
- Edit the configuration file using any text editor.
- Run `pyinstalive -r "<live-username>"` to start recording a livestream.


## Installation

#### Prerequisites
You need [ffmpeg](https://ffmpeg.org/download.html), [Git](https://git-scm.com/downloads) and [Python 2.7.x or 3.5>=](https://www.python.org/downloads/) with [pip](https://pip.pypa.io/en/stable/installing/) and [setuptools](https://packaging.python.org/tutorials/installing-packages/#install-pip-setuptools-and-wheel) installed before you can install and use this script. Make sure all tools are accessible via command line (added to your PATH if on Windows, use Google).

#### Installing

Run the following command in command line (as administrator in Windows) / terminal:
```bash
pip install git+https://github.com/notcammy/PyInstaLive.git@2.2.7 --process-dependency-links
```

#### Updating

To update PyInstaLive to the latest version (currently **2.2.7**) run the following command:

```bash
pip install git+https://github.com/notcammy/PyInstaLive.git@2.2.7 --process-dependency-links --upgrade
```

#### Specific versions

If you want to install a specific version of PyInstaLive, you can specify the version tag in the install command:

```bash
pip install git+https://github.com/notcammy/PyInstaLive.git@2.1.0 --process-dependency-links
```

Use the version number you want after the **@** symbol (e.g **2.1.0**).


## Usage
Make sure there is a configuration file called ``pyinstalive.ini`` in the directory you want to run PyInstaLive from.
You can run ```pyinstalive -c``` to automatically generate a default configuration file if one is not present.

Here is an example of a valid configuration file:
```bash
[pyinstalive]
username = johndoe
password = grapefruits
save_path = /
show_cookie_expiry = true
clear_temp_files = false
```

Use the following command to run PyInstaLive:

```bash
pyinstalive -u "<username>" -p "<password>" -r "<live-username>"
```

Where ``<username>`` is your account's username, ``<password>`` is your password and ``<live-username>`` is the username of the user whose livestream or replay you want to record or save.

#### Notes
The `username` and `password` parameters are not required when you have specified these in the configuration file.

If the script is ran and there are available replays as well as an ongoing Instagram livestream, only the livestream will be downloaded. Run the script again after the livestream has ended to download the available replays.


## Example
```bash
pyinstalive -u "johndoe" -p "grapefruits" -r "janedoe"
```
Or (see [note](https://github.com/notcammy/PyInstaLive#notes))
```bash
pyinstalive -r "janedoe"
```

If a livestream is currently ongoing, the terminal output should be something like this:

```
----------------------------------------------------------------------
PYINSTALIVE (SCRIPT V1.0 - PYTHON V2.7.14) - 12:00:01 PM
----------------------------------------------------------------------
[I] Login to "naxunaw" OK!
[I] Login cookie expiry date: 2018-02-13 at 12:00:01
[I] Checking user: 'justinbieber'
[I] Checking for ongoing livestreams...
[I] Starting livestream recording:
[I] Username    : carendelano
[I] MPD URL     : https://scontent-ams3-1.cdninstagram.com/hvideo-frc1/v/rflSWUsyCsuqE-GLYgvW4/live-dash/dash-abr/17880993205152831.mpd?_nc_rl=AfCujc4yG9bJLHVn&oh=87c4fb94668286125f1169e4441056d2&oe=5A0E8951
[I] Viewers     : 2768 watching
[I] Airing time : 5 minutes and 10 seconds
[I] Status      : Active
----------------------------------------------------------------------
[I] Recording livestream... press [CTRL+C] to abort.

[I] Stitching downloaded files into video...
[I] Successfully stitched downloaded files.
----------------------------------------------------------------------
```


## Help
If you have a bug to report please open [an issue](https://github.com/notcammy/PyInstaLive/issues) in the appropriate format:

##### - Expected behavior


##### - Actual behavior


##### - Steps to reproduce problem

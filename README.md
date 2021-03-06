Alfred 2 layout workflow
========================

A simple window layouter based on an Alfred 2 workflow.

# Description

The workflow itself is quite simple just typ in the keyword "lay" (or chose another of your liking) followed by:
* full = Maximize
* left, right, top, bottom = Halves of screen
* topleft, topright, bottomleft, bottomright = Quaters of screen
* center = Center of screen (with 10% border)
* 11,12,13,21,22,23,31,32,33 = Thrids of screen
* 11-12,11-13,11-21,11-22 ... = Some other sizes based on thrids
* togglefullscreen = Toggle full screen mode of active window (if possible)
* ... well the script is quite flexible, so I'm waiting for suggestions

It is multi-screen-able. Even though you cannot move windows from one screen to another (yet?) the scripts tries to figure out with screen you mean (depending on the size of the visible area).

# Screenshots

![Screenshot1](https://dl.dropboxusercontent.com/u/3815280/Bildschirmfoto%202013-09-24%20um%2013.54.58.png)
![Screenshot2](https://dl.dropboxusercontent.com/u/3815280/Bildschirmfoto%202013-09-24%20um%2013.55.22.png)

# Implementation notes

* The script is written in python using PyObjC and the ScriptingBridge. This should be no problem as both is shiped as part of MacOS since 10.5.
* It the application supports scripting, the window is moved "directly". Unluckily some Applications do not support this, so there is a fallback using "SystemEvents". This only works if you have UI scripting enabled: [Graphic User Interface (GUI) Scripting](http://www.macosxautomation.com/applescript/uiscripting/)
* At the moment there are no hotkeys defined, which should be straight forward though ...

# Licence

[MIT Licence](http://opensource.org/licenses/MIT)


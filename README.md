# TownShell

<p align="center">
<a href="./Pictures/TownShell.ico">
<img src="./Pictures/TownShell.ico" alt="TownShell ico">
</a>
</p>


Wanna save some clicks on [Townscaper](https://store.steampowered.com/app/1291340/Townscaper/), this small app will help you !

Get additional keyboard shortcuts to relax your fingers while building your town.

Get access to useful tools to accelerate your building process. Change the height of many blocks at a time. Change the color of your whole structure with a few words.

[![Townshell_Youtube](http://img.youtube.com/vi/QA5MrFqmpVY/0.jpg)](http://www.youtube.com/watch?v=QA5MrFqmpVY)

# Quickstart
Download "TownShell.exe" [here](https://github.com/mokojm/townshell/releases/download/v1.0/TownShell.exe),

Click '**TownShell.exe**'

Since I do not have any certificates, Windows and firewalls might prevent you from opening the .exe. Just skip warning to enjoy TownShell features

Open "Townscaper",
Click "New",
Press "Space" few seconds,

Enjoy the fast click !

Click "Save to Clipboard",
Tap "²" to open "TownShell",
Explore the functions

Back to "Townscaper" click "Load from Clipboard", 
Enjoy the time you've saved !

Explore this file for more features

# Table of contents
1) [Installation](#installation)
2) [Usage](#usage)
	- [Startup screen](#startup-screen)
	- [Keyboard Shortcuts](#keyboard-shortcuts)
	- [Level](#level)
	- [Paint](#paint)
	- [Dig](#dig)
	- [Replicate](#replicate)
	- [Merge](#merge)
3) [Details](#details)
	- [Advanced installation](#advanced-installation)
	- [Shortcuts configuration](#shortcuts-configuration)
	- [More](#theory)
4) [Future Releases](#future-releases)

# Installation

The easiest way to get started is by following the link [here](https://github.com/mokojm/townshell/releases/download/v1.0/TownShell.exe)

For advanced users familiar with Python and Kivy, see [Advanced installation](#advanced-installation)

# Usage

## Startup screen

![TownShell_startup](/ReadMePictures/startup.gif)


## Keyboard shortcuts
Keyboard shortcuts are active by default once TownShell is started. It works only when Townscaper is the foreground window.
Default shortcuts are as follows :

'Open TownShell' ==> '²'

'left_click' ==> 'space'

'right_click' ==> 'c'

'undo click' ==> 'v'

'redo click' ==> 'b'

'custom_left_click' ==> 'maj+space'

'custom_right_click' ==> 'maj+c'

'custom_undo' ==> 'maj+v'

'custom_redo' ==> 'maj+b'

'undo last command' ==> 'ctrl+alt+z'

'redo last command' ==> 'ctrl+alt+x'


For example, by default, keeping 'x' pressed will result in block creation every 0,05 seconds.

Custom shortcuts allow you to have one event done a precise number of times:
1) Press one or several digits
2) Use one of the custom shortcuts described above
Note that if you press several digits, the time between the press needs to be less than one second.
For example, if you press "1" then "2" quickly then you use 'custom_left_click' keyboard shortcut, it will result in 12 blocks getting created.

If you're not satisfied with these shortcuts see [Shortcuts configuration](#shortcuts-configuration)

## Level

![TownShell_level_example](/ReadMePictures/Level.gif)

'level' command give you the ability to elevate your structure at any height (<255) with a bunch of options. To use it, click "Save to Clipboard" on the structure you want the height to change, 
press "²" to open TownShell and enter a command following the rules below. 
Then on Townscaper click "Load from Clipboard".

Note that your original file is not modified.


## Paint

![Paint_example](/ReadMePictures/Paint.gif)

'paint' command give you the ability to change the color of many blocks at a time with a bunch of options.
To use it, click "Save to Clipboard" on the structure you want the height to change, 
press "²" to open TownShell and enter a command following the rules below. 
Then on Townscaper click "Load from Clipboard".

Note that your original file is not modified.

## Dig

![Dig_example](/ReadMePictures/Dig.gif)

## Replicate

![Replicate_example](/ReadMePictures/Replicate.gif)

## Merge

![Merge_example](/ReadMePictures/Merge.gif)

# Details

## Advanced installation
TownShell is written in Python qnd Kivy language. 
If you do not have Python installed on your computer, you can download it and install it from [here](https://www.python.org) 
If you do not have Kivy, you can download it and install it from [here](https://kivy.org/doc/stable/gettingstarted/installation.html)

The following libraries are necessary too : keyboard, mouse, and pyperclip. You can install them using 'pip' from windows command line (cmd.exe) :

```pip install keyboard mouse pyperclip```

Then download the master branch on Git then run "main.py" to start using TownShell.

## Shortcuts configuration
At any time, you can see the active shortcuts on Main screen. If you're not satisfied with the shortcuts provided by default, you can modify them by opening 'townshell.cfg' file. 
1) Use your native notepad application to open it
2) Modify the lines related to the keyboard shortcuts to personify your TownShell. Note that 'pause' is the interval between to automatic clicks in seconds.
3) Save the file, then either restart TownShell or switch Keyboard shortcuts button.

**Warning** ! Beware that Townscaper use already a few keyboard shortcuts, so it's recommended not to use these ones. See: https://www.yekbot.com/townscaper-controls-useful-shortcuts-for-fast-building/

## Concepts
In Townscaper saved files, each position on the grid of Townscaper is called a 'corner'. On each 'corner' you can have one or more blocks. A block is called a 'voxel'. Therefore, every Townscaper building is an assembly of corners of voxels.
If you wish to read more about how Townscaper saved files are made, you can go to the following website : https://medium.com/@chrisluv/getting-hacky-with-townscaper-5a31cf7f4c6a


## From clipboard to customizable dictionaries

Townscaper provides us strings through "Save to clipboard" that will be called "clip" in TownShell program. These clips contain all the information describing a given structure, allowing Townscaper's users to share their creations. 

[alvaro-cuesta](https://github.com/alvaro-cuesta/townsclipper) made a very good script that converts clips to dictionary of corners and voxels using Javascript.
Since TownShell is written in Python, the core part of townsclipper code has been translated and adjusted.

## Configuration file
'townshell.cfg' is the configuration file of TownShell. 

Keyboard shortcuts are stored inside.


## Logging
In 'townshell.cfg', 'loglevel' setting determine the level of log that will be saved in 'town.log'. By default it's "INFO". It can be useful to set it to "DEBUG" when a bug is encountered and needs to be shared.

'town.log' contains only the log information related to the running TownShell. If you're looking for older log information, it's in 'town_old.log'

Kivy log files are also stored in 'log' repository

# Future releases

Here are a few stuffs I'd like to add, implementation is not guaranteed :
- "Reset" button on each screen
- "Write" screen to write text in Townscaper
- "Draw" screen to draw stuff in Townscaper
- "Generate" screen to automate city generation given a map

- Automatic click on "Load on Clipboard" in Townscaper after clicking on "Save to Clipboard" in TownShell
- Add "Ground color" to be filtered in "Level", "Dig" and "Replicate" screen
- Multiple color filter in "Level" and "Replicate"
- Multiple height filters in "Paint" + add height filter in other screens

## Bugs

(to be completed)

# Contributing
I'm not very experienced at programming or using github, so any help on making this project easier to understand will be appreciated.
Do not hesitate to report bugs.

Copyright © 2020, [Álvaro Cuesta](https://github.com/alvaro-cuesta/townsclipper).
//=> Copyright (c) 2020 Álvaro Cuesta

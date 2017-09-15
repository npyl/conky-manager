
Conky Manager
=======================

Simple tool for managing Conky configs.


macOS Port
=======================

***YES!*** There is a macOS port of conky! You may want to checkout it out in [github]( https://github.com/npyl/conky)

## Prologue

I thought it would be nice to have a configuration utility for conky on macOS, too!

## How to build & install

- First, install the following packages: `brew install vala libgee gtk+3 json-glib imagemagick`
- Then, navigate to project directory and go into 'src'
- Open the makefile and edit the line that says: `prefix=/usr` to `prefix=/usr/local/conky-manager`
- Execute the commands: `sudo mkdir /usr/local/conky-manager`, `sudo chown root:wheel /usr/local/conky-manager`
- then `cd ..` and `make` and `make install`  ( You will need sudo for the last two! )
- then last thing, fix some things manually:
	- navigate to project directory/src/share/conky-manager/images/ and copy everything to /usr/share/conky-manager/images .  ( Note the directory 'images' may not exist, you should create it)
	- navigate again to project directory/src/share/conky-manager/themepacks and copy the file to /usr/share/conky-manager/themepacks
	- then type on terminal: `sudo nano /bin/pidof` and inside nano copy-paste the lines:
		`#!/bin/sh`
		
		`ps axc|awk "{if (\$5==\"$1\") print \$1}";`
		
		YOU ARE READY! ;)
		Run using the command `conky-manager`
		
## Should mention

that I took ideas and help from this [site](http://elatov.github.io/2016/01/playing-around-with-conky-on-gentoo/)

## How well does it work?

It works (surprisingly) quite well. I will upload video soon! :)

Conky Manager
=======================

Simple tool for managing Conky configs.  For a native macOS alternative checkout [ManageConky](https://github.com/Conky-for-macOS/Manage-Conky).  Trust me, its good.


macOS Port
=======================

***YES!*** There is a macOS port of conky! You may want to checkout it out in [github]( https://github.com/npyl/conky)

## Prologue

I thought it would be nice to have a configuration utility for conky on macOS, too!

## How to build & install

- First, install the following packages: `brew install vala libgee gtk+3 json-glib imagemagick p7zip`
- Then, navigate to project directory and go into 'src'
- Open the makefile and edit the line that says: `prefix=/usr` to `prefix=/usr/local/opt/conky-manager`
- then `cd ..` and `make` and `cd src && make install`
- then last thing, fix some things manually:
	- type on terminal `ln -s /usr/local/opt/conky-manager/bin/conky-manager /usr/local/bin/conky-manager`
	- then type: `sudo nano /bin/pidof` and inside nano copy-paste the lines:
		`#!/bin/sh`
		
		`ps axc|awk "{if (\$5==\"$1\") print \$1}";`
		
		YOU ARE READY! ;)
		Run using the command `conky-manager`
		
## Should mention

that I took ideas and help from this [site](http://elatov.github.io/2016/01/playing-around-with-conky-on-gentoo/)

## How well does it work?

Check it for yourself: [vid](https://www.youtube.com/watch?v=l3tIiDdnC68)

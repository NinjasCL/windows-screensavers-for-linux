# Windows ScreenSavers for Linux

Collection of Windows Screensavers (Windows 95, 98, XP and 7) that can be used inside Linux.

![Image with XScreenSaver Settings](https://github.com/user-attachments/assets/0bdc3cb2-573e-4eed-a225-02270061fc84)

Maybe unstable. Use with care.

## Installation

These instructions were tested in `debian 12`.

1. Install xscreensaver (or another similar software)

```bash
# apt install -y xscreensaver xscreensaver-gl xscreensaver-gl-extra
```

2. Install wine

```bash
# apt install -y wine winetricks
```

Also install wine32

```bash
# sudo dpkg --add-architecture i386 && sudo apt update
# sudo apt install -y wine32:i386
```

Install display drivers (for Nvidia)

```bash
# sudo apt install -y nvidia-driver-libs:i386
```

3. Configure Wine

```bash
$ winetricks renderer=gl  
```

If there is a config problem. Try deleting the `.wine` dir in `$HOME`.

```bash
$ rm -rf ~/.wine
```

4. Install the `windows95` directory

The route must be `/usr/local/src/windows95`. If you need another one
you must modify the routes inside the bash files.

```bash
# cp -R windows95 /usr/local/src
```

5. Open `xscreensaver-settings`

Select any screensaver and close. This will create the base configuration file

6. Edit `~/.xscreensaver` file

Add the following code to the list of the available screensavers

```text
- GL: 	      "Win95 3D Pipes" 	/usr/local/src/windows95/3dpipes.sh --root  \n\
- GL: 	       "Win95 3D Maze" 	/usr/local/src/windows95/3dmaze.sh --root   \n\
- GL:  "Win95 Flying Through Space"					      \
				  /usr/local/src/windows95/flying.sh	      \
				  --root				    \n\
- GL: 		 "Win95 Orbit" 	/usr/local/src/windows95/orbit.sh --root    \n\
- GL: 		"Win95 Curves" 	/usr/local/src/windows95/curves.sh --root   \n\
- GL: 	    "Win98 Underwater" 	/usr/local/src/windows95/underwater.sh	      \
				  --root				    \n\
- GL: 		"Win98 Jungle" 	/usr/local/src/windows95/jungle.sh --root   \n\
- GL: 	       "Win98 Mystery" 	/usr/local/src/windows95/mystery.sh --root  \n\
- GL: 	       "Win98 Mystify" 	/usr/local/src/windows95/mystifymind.sh	      \
				  --root				    \n\
- GL: 	      "Win98 Baseball" 	/usr/local/src/windows95/baseball.sh --root \n\
- GL: 	     "Win98 Dangerous" 	/usr/local/src/windows95/dangerous.sh	      \
				  --root				    \n\
- GL: 	    "Win98 Golden Era" 	/usr/local/src/windows95/golden.sh --root   \n\
- GL:  "Win98 Inside your Computer"					      \
				  /usr/local/src/windows95/inside.sh	      \
				  --root				    \n\
- GL: 	      "Win98 Leonardo" 	/usr/local/src/windows95/leonardo.sh --root \n\
- GL: 		 "Win98 Space" 	/usr/local/src/windows95/space.sh --root    \n\
- GL: 		"Win98 Sports" 	/usr/local/src/windows95/sports.sh --root   \n\
- GL: 		"Win98 Travel" 	/usr/local/src/windows95/travel.sh --root   \n\
- GL: 		  "WinXP Flag" 	/usr/local/src/windows95/windowsxp.sh	      \
				  --root				    \n\
- GL: 		"Win7 Mystify" 	/usr/local/src/windows95/windows7.sh --root \n\
```

Save the file

7. Open `xscreensaver-settings`

Open again and select your preferred screen saver.

## List of ScreenSavers

* Windows 95:
	- 3D Maze
	- 3D Pipes
	- Flying Through Space
	- Orbit
	- Curves

* Windows 98:
	- Underwater
	- Jungle
	- Mystery
	- Mystify Your Mind
	- Baseball
	- Dangerous Creatures
	- The Golden Era
	- Inside Your Computer
	- Leonardo da Vinci
	- Space
	- Sports
	- Travel

* Windows XP:
	- Flag

* Windows 7:
	- Mystify

## Tips

If you want to configure a screensaver you can use

```bash
$ wine myscreensaver.scr
```

If you want to run a screensaver use

```bash
$ wine myscreensaver.scr /s
```

## Additional Resources

- https://joefreeman.weebly.com/using-windows-sreensavers-on-linux.html
- http://cs.gettysburg.edu/~duncjo01/archive/screensavers/

## 🤩 Credits

All copyrights to their respective owners. 

<p>
  Made with <i class="fa fa-heart">&#9829;</i> by
  <a href="https://ninjas.cl">
    Ninjas.cl
  </a>.
</p>
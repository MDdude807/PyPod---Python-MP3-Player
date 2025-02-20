# ***NEWS***

## NEWEST FILE
[Version 1.0B](https://github.com/MDdude807/PiPod-0-W-2/blob/main/Versions/Ver%201.0B/PiPod.py)

## Announcements

**2/19/25 - Version 1.0 B released February 19th, 2025**  
Currently working on both Windows and Debian.

**Added:**
1. Dark mode
2. Debian support (tested on DietPi)

**2/14/25 - Version 1.0 A released February 14th, 2025**  
Currently works only on Windows. Version 1.0 B should work on Debian.

# About the Project
The PiPod 0W2 was my idea to bring together affordable Raspberry Pi components and the features of my favorite music players, especially the iPod. I want to make an open-source and easily used media player for Linux and Windows users, but I have chosen to target the Raspberry Pi. I will release support for all platforms whenever I can.

### The Software
The project is using [Diet Pi](https://dietpi.com/) as the operating system and is the bulk of the heavy lifting for the actual software. Instead of making this project easier for myself and just using an already made media playing software like [VLC](https://www.videolan.org/vlc/) or [Dragon Player](https://apps.kde.org/dragonplayer/), I decided to code my own music player using [Python](https://www.python.org/) and [Pygame](https://www.pygame.org/news). Python does all the media playback and tracking of metadata and details, while Pygame is the frontend and GUI. The reasoning for the extra work is because I want ***YOU*** to contribute!

### The Hardware
The project is aimed for the Raspberry Pi Zero series boards, and uses DietPi as a base. I personally have used a Waveshare screen and a Raspberry Pi Zero 2 W and some audio tools to create a basic all-in-one device that is a small form factor computer. When I get further in the project, I will give instructions and specifics on the build.

## How to Setup
On your Debian or DietPi install Python and check if Python is installed:
```
Sudo apt update
sudo apt install python3
python3 --version
```

After python3 is installed, install pip to make python package management easier:
```
sudo apt install python3-pip
```
This should make installation of required packages easier, but I will provide a second way to install the packages if pip doesn't work. Pip didn't work for me in my DietPi VM, or my physical install.

Now to install the required packages:
```
pip install mutagen
pip install pygame
```
And if that doesn't work then do this:
```
sudo apt install python3-pygame
sudo apt install python3-mutagen
```

Now to set up the python project to be executable.

First you have to use the `cd` command to navigate to where the python project is. for example I have it in downloads, but it won't be the same for you depending on how you download it or import it. To get to my script I would do this:
```
cd /root/Downloads
```
Your Consle should now say you are in the folder you wanted to enter.

Now you have to convert the python script to be executable. Within the folder you have CD'd into is your python script. Now the name is case sensitive, so be careful:
```
chmod +x PiPod.py
```
***MAKE SURE YOU USE YOUR FILE NAME INSTEAD IF IT IS DIFFRENT***

Now the file is executable. to run it, make sure you are in the folder with the file by using `CD` if youre not sure if the file is in that folder use `ls` to list items in the directorty. If you are in the correct place and your file is in the folder run this:
```
python3 PiPod.py
```
***AGIAN MAKE SURE YOU USE THE RIGHT FILE NAME***

If everything is right, then it should launch! :)

## How to Use
To navigate, use the up and down arrow keys. To go into a folder or into a new screen use Enter key. To play a found MP3 file, use enter agian, to go back a menu, use the left arrow.

When on the Music Info screen, use right arrow to pause and play, up and down to change volume, and the left arrow to go back to the previous menu.

If you have an extra flash drive, format it and name it PIPOD. Plug it in and the drive will be correctly populated with folders that match the MP3's system. Put your songs in MP3 format with all the metadata populated into the folders you want them to be, or create new folders in the required folders. Now plug in your filled drive and hit the option to sync USB, and the songs will be copied over and so will all the folders you made. This makes adding songs much easier!

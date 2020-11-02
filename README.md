# Mauricio's mwm
My MWM setup nothing fancy, yet. I just wanted to know how to work with MWM, most of my costumisation is based on my setup on i3.

![Preview](https://github.com/mauricioph/mwm/blob/master/images/Preview.png?raw=true)

## Patches on this build
Transient window, Fibonacci layout, status commands and hide vacant tags.

## Theme:
| Colour  | HTML Code | Position |
|---------|-----------|----------|
| orange  |  #c37306  | Selected |
| D.Red   |  #232629  | Selected Text |
| L.D.Red |  #232629  | Selected Window Border  |
| White   |  #ffffff  | All Text |
| D.cyan  |  #1d4664  | Bar/Border @ stack   |


## These are the Keybinds:
![Keybpard Layout](https://github.com/mauricioph/mwm/blob/master/images/mac-us-international-keyboard_1024x1024.png?raw=true)

| Keybind |  Command |
|---------|----------|
| Super + a | Audacity Audio editor |
| Super + b | Toggle the bar |
| Super + c | Connect Wifi |
| Super + d | rofi menu |
| Super + e | power off script |
| Super + f | Firefox |
| Super + g | VScode |
| Super + h | Decrease Master Area |
| Super + i | Switch Layout |
| Super + j | Switch Focus Stack |
| Super + k | Switch Focus Stack |
| Super + l | Increase Master Area |
| Super + n | Connect to the wifi |
| Super + r | Fibonacci layout |
| Super + t | lockscreen |
| Super + v | VLC |
| Super + Tab | switch tabs |
| Super + Enter | st Terminal |
| Super + minus | Descrease gaps |
| Super + equal | Increase gaps |
| Super + Shift + equal | Set gaps to 0
| Super + Shift + Enter | Swap Master with Stack window |
| Super + Shift + Space | Toggle Floating |
| Super + Shift + t | Toggle Layout to Vertical Master/Stack|
| Super + Shift + f | Toggle Layout to Vertical Master/Stack|
| Super + Shift + r | Toggle Layout to Dwindle |
| Super + Shift + e | exit mwm |
| Super + Shift + q | Quit the programs |
| Super + Shift + t | Lockscreen script |
| Super + Shift + ENTER | swap focused window with Master |
| XF86 AudioRaiseVolume | pactl set-sink-volume 0 +5% |
| XF86 AudioLowerVolume | pactl set-sink-volume 0 -5% |
| XF86 AudioMute | pactl set-sink-volume 0 0 |
| XF86 MonBrightnessUp | script screen-backlight up |
| XF86 MonBrightnessDown | script screen-backlight down |
| XF86 KbdBrightnessUp | script keyboard-backlight total |
| XF86 KbdBrightnessDown | script keyboard-backlight off |


## Install:
Using the install script will add the session desktop file for lightdm and others display managers at /usr/share/xsessions/ and the scripts to autostart the programs and control keyboard and screen backlights.

```
git clone https://github.com/mauricioph/mwm.git
cd mwm
chmod +x install.sh
./install.sh

# visudo in some distro will allow you to change the sudoers file
visudo

# add the following replacing the user with your username or group

user ALL= (root) NOPASSWD: /usr/local/bin/screen-backlight
user ALL= (root) NOPASSWD: /usr/local/bin/keyboard-backlight

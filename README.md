# morc_menu
Categorized desktop application menu
* independent of any window manager
* highly and easily customizable

morc_menu is a bash script that simulates the functionality of an [Openbox](https://en.wikipedia.org/wiki/Openbox)
/ [Fluxbox](https://en.wikipedia.org/wiki/Fluxbox) style menu without requiring those window
managers or associated dependencies. It was originally
written for the [i3 window manager](https://en.wikipedia.org/wiki/I3_%28window_manager%29), and using '[dmenu-manjaro](https://github.com/oberon2007/dmenu-manjaro)' (wikipedia: [dmenu](https://en.wikipedia.org/wiki/Dwm#dmenu) ) as
as its front-end, but it should also work in pretty much
any X11 environment, and has been tested with
alternative front-ends such as the [normal/vanilla/real version of 'dmenu](http://tools.suckless.org/dmenu/)', as well as  '[rofi](https://davedavenport.github.io/rofi/)', '[zenity](https://en.wikipedia.org/wiki/Zenity)' and
'yada'.

morc_menu generates menus based upon the presence of
.desktop files in the system-wide definition folder
/usr/share/applications and the user-local definition
folder ${HOME}/.local/share/applications, per the
xfreedesktop and linux LSB standards.

A readable version of the script's [man page](https://github.com/Boruch-Baum/morc_menu/wiki/man-page) is available on this repository's [wiki](https://github.com/Boruch-Baum/morc_menu/wiki).

## Requirements

For the presentation front-end:
* dmenu, or
* rofi, or
* zenity, or
* yada, or
* something else.

Optionally, for aligning / positioning the menu at the current mouse pointer:
* [xdotool](http://www.semicomplete.com/projects/xdotool), from package xdotool;
* lsw and wattr, both from package [wmutils](https://github.com/wmutils/core)

## Setup

  If your distribution has a packaged version of this
  script, it is advisable to install that package and
  to follow any supplemental instructions of the
  packager.

  Manually installing the script involves five steps:
  Copy this script file to a convenient location, for
  example, somewhere on your ${PATH}; Make it executable
  by running 'chmod +x /path/to/file'; Optionally, copy
  the script's associated config file to
  ${HOME}/.config/morc_menu; Optionally, copy the
  script's associated man page to somehwere your system
  will recognize (run command 'manpath', and if you can
  not place it in any of those places, run 'man manpath'
  to see how to set $MANPATH), and; Create a keybinding
  for the script. An example keybinding for use with the
  i3 window manager would be to modify your
  ${HOME}/.i3/config file to include a statement in the
  form:
     bindsym $mod+z
             exec "${HOME}/path/to/morc_menu"

## Customization
  This script offers many ways to customize the menu's
  content and 'look' ('skin'). Refer to the script's
  [man page](https://github.com/Boruch-Baum/morc_menu/wiki/man-page) and [configuration file](https://raw.githubusercontent.com/Boruch-Baum/morc_menu/master/morc_menu_v1.conf) for details.

## Copyright and License

 ©2016, Boruch Baum <boruch_baum AT gmx DOT com>

 This program is free software; you can redistribute it
 and/or modify it under the terms of the GNU General
 Public License aspublished by the Free Software
 Foundation; either version 3 of the License, or (at your
 option) any later version.

 This program is distributed in the hope that it will be
 useful, but WITHOUT ANY WARRANTY; without even the
 implied warranty of MERCHANTABILITY or FITNESS FOR A
 PARTICULAR PURPOSE. See the GNU General Public License
 for more details.

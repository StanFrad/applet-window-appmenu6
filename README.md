# Window AppMenu Applet
This is port   [psifidotos](https://github.com/psifidotos/applet-window-appmenu/) and  [proatgram](https://github.com/proatgram/applet-window-appmenu6/) .

This is a Plasma 6 applet that shows the current window appmenu in your panels. This plasmoid was coming from [Latte land](https://phabricator.kde.org/source/latte-dock/repository/master/) but now support only Plasma panels.

<p align="center">
<img src="https://i.imgur.com/T0sLWav.gif" width="580"><br/>
<i>hide menu when active window is minimized</i>
</p>

<p align="center">
<img src="https://i.imgur.com/ARJbMWX.gif" width="580"><br/>
<i>scroll menu support</i>
</p>


<p align="center">
<img src="https://imgur.com/w1EA6lr.png" width="580"><br/>
<i>settings window</i>
</p>

# Features

- Provide spacing option
- Customise your menu colors based on your system color schemes

# Requires

- Qt >= 6.7
- KF6 >= 6.1
- Plasma >= 6.0
- plasma-workspace-devel >= 6.1.0 

**Qt elements**: Quick Widgets DBus

**KF6 elements**: Plasma WindowSystem KDecoration2 Kirigami2 extra-cmake-modules

**X11 libraries**: XCB RandR

**Plasma Workspace**: LibTaskManager

# Install

You can execute `sh install.sh` in the root directory as long as you have installed the previous mentioned development packages


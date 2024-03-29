~~Pulse~~EasyEffectsTray 0.1

This is some kind of quick'n'dirty stand-alone add-on for ~~Pulse~~EasyEffects by Wellington Wallace:

https://github.com/wwmm/easyeffects

It creates a GTK3 status icon in the taskbar (tray) to toggle bypass state on left-click and offering a menu to select from the available presets for in- and outputs on right-click.
Additionally the icon and EasyEffects can be killed.

It requires Python3 and GTK3 (`python3-gi` on Debian based OS) for python. Make the file `easyeffectstray` executable:

```
chmod a+x easyeffectstray
```

And execute it.

Alternatively run the script `install.sh` as root to install the script to `/usr/local/bin`, the icon to `/usr/share/pixmaps` and the application starter to `/usr/share/applications`. This makes the tray icon available in application menus.

The PNGs are not required on run-time since graphics data is base64 encoded in the script itself. So most minimal setup is to just have the executable lying around somewhere.

If you have EasyEffects >= v4.7.4 installed, the icon can be used to toggle visibility of the window instead of toggling bypass. To make use of this feature, make sure to run the easyeffects daemon (argument `--gapplication-service`) and start easyeffectstray with the argument `-h`.

If you'd like to bypass EasyEffects on click in hide-to-tray mode, create a fresh preset called `Bypass`, disable all signal processors and save the settings to the preset. It will appear in the tray icons menu then.

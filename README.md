PulseEffectsTray 0.1

This is some kind of hacky stand-alone add-on for PulseEffects by Wellington Wallace:

https://github.com/wwmm/pulseeffects

It creates a GTK3 status icon in the taskbar (tray) offering a menu to select from the available presets for in- and outputs.
Additionally the icon and PulseEffects can be killed.

It requires Python3 and GTK3 for python. Make the file `pulseeffectstray` executable:

```
chmod a+x pulseeffects
```

And execute it.

The icons are not required since graphics data is base64 encoded in the script itself.

If you'd like to bypass PulseEffects on click, create a fresh preset called `Bypass`, disable all signal processors and save the settings to the preset. It will appear in the tray icons menu then.

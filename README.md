# Playspace Mover

Lets you drag around your playspace by gripping certain buttons. This allows you to "climb" around certain games, and allows you to adjust your floor level on the fly.
This is compatible with KinectToVR, and can run in tandem with any SteamVR app.

## Installation

* Requires VR Input Emulator, which an easy installer can be found [here](https://github.com/matzman666/OpenVR-InputEmulator/releases).
* Grab a PlayspaceMover executable from the [releases page](https://github.com/naelstrof/VRPlayspaceMover/releases).
* Extract anywhere and run anytime, it will automatically detect and connect to SteamVR, then it will automatically detect and work with any devices connected.

## Config

PlayspaceMover can be configured to use different kinds of bindings, currently it only supports button presses. You can change the default buttons by setting button masks in the options. This can be done through either a shortcut, or a commandline.

I find the easiest way is to experiment using the command line, then set up a permanent config with a shortcut!

Open a command line in the folder with PlayspaceMover.exe like so:
![GIF Showing how to open cmd](https://i.imgur.com/jgifVnJ.gif)
---
If you're on Oculus, type `./PlayspaceMover.exe -l 128 -r 128 --resetButtonMask 2` then press enter!
![Image of PowerShell for Oculus](https://i.imgur.com/g2MsPH0.png)
This will set the A and X buttons to move the playspace, and if you press B and Y simultaneously it will reset your playspace!
---
If you're on Vive, try typing `./PlayspaceMover.exe -l 2 -r 2 --resetButtonMask 4` then press enter!
![Image of PowerShell For Vive](https://i.imgur.com/S98It5X.png)
This will set the menu buttons to move your playspace, and if you press both grip buttons simultaneously it will reset your playspace!

### Permanent Config

To make this change "permanent", you can create a new shortcut by right-click dragging it to your desktop.

![GIF showing how to make a shortcut](https://i.imgur.com/zPM27WN.gif)

Then edit it's properties by right-clicking on it, and hitting properties.
Then add your desired button mask options to the "Target:" section.

![Image of shortcut properties](https://i.imgur.com/rUSzA8l.png)

Done! Double click on that shortcut to launch your configured playspace mover!

Try `./PlayspaceMover.exe --help` for more help on bit-masks and other stuff!

## Tips

* VR Input emulator likes to keep HUGE logs if you're on oculus (18+GB), set `X:/Steam/steamapps/common/SteamVR/drivers/00vrinputemulator/bin/win64/driver_vrinputemulator.log` to read-only to prevent this!

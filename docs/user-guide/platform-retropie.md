# Platform notes: RetroPie

Other than the official Raspberry Pi releases you can found on the [download page](getting-started.md), Pegasus is also from the RetroPie repositories. You can install it by two ways:

- a) From the RetroPie setup menu
- b) Using the Frontend Chooser tool

Note: you will need RetroPie version 4.3 (released on September 21, 2017) or later to install Pegasus through RetroPie.

## From the setup menu

You can start the RetroPie setup script from the terminal (`sudo ~/RetroPie-Setup/retropie_setup.sh`) or from another already installed frontend. You will be greeted with a text-based interface. To install Pegasus, select *Manage Packages &rarr; Manage experimental packages &rarr; pegasus-fe &rarr; Install from binary*. The latest release will then be downloaded. You can also update your existing installation here.

![retropie screenshot](img/retropie-expmenu.png)

After the installation, you can either call `/opt/retropie/supplementary/pegasus-fe/pegasus-fe` manually, or edit `/opt/retropie/configs/all/autostart.sh` to launch Pegasus on boot (instead of eg. ES2).

## Using the Frontend Chooser

There's also a graphical tool for installing various frontend and setting them up to boot automatically.

![retropie frontend chooser screenshot](img/retropie-frontendchooser.png)

It is available from [HERE](https://github.com/mmatyas/retropie-frontendchooser).

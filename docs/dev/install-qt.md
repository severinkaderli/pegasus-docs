# Installing Qt for desktop

Qt is a cross-platform application framework used by Pegasus. At least Qt 5.8 is requred, with 5.9 or later recommended for better performance on embedded platforms. For desktop platforms you can get the Qt tools using their installer:

<a href="https://www1.qt.io/download-open-source/"><button type="button" class="btn btn-success"><i class="fa fa-cloud-download"></i> &nbsp; Download the Qt installer</button></a>

Then walk through the installation, and select the component "Desktop gcc" (Linux), "MinGW" (Windows) or "macOS" for macOS:

<table><tr>
    <td><img style="max-width:100%" src="../img/install-qt-2.png"></td>
    <td><img style="max-width:100%" src="../img/install-qt-6.png"></td>
</tr></table>

Now you have the Qt libraries and the Qt Creator IDE installed.

!!! note "Components on Windows"
    On **Windows** you can choose between MinGW and MSVC compiler packages. If you're planning to edit the source code and you want to use Visual Studio, you can select the matching MSVC component instead of MinGW.

!!! warning "Embedded"
    These instructions are for **desktop** platforms. For embedded devices, you have to compile Qt manually, or use the prebuilt libraries available on Pegasus' GitHub page. See [Cross compile Qt](cross-compile-qt.md).


# Alternative installations

## Linux

On many Linux distros, the Qt libraries in the official repositories are often several years old (as a trade-off between stability and access to the latest software), or miss some components.

### Ubuntu, Debian

**Debian 10** (buster/testing) contains an up-to-date Qt release and building Pegasus should be possible.

**Ubuntu 18.04** contains an up-to-date Qt release, but misses a few necessary packages. You can either use the Qt installer (see above), or the followin PPAs:
On **Ubuntu**, you can use the following PPAs to get the latest Qt releases:

```sh
sudo add-apt-repository ppa:beineri/opt-qt-5.11.1-bionic

sudo apt-get update
sudo apt-get install  \
    qt59declarative  \
    qt59graphicaleffects  \
    qt59gamepad  \
    qt59imageformats  \
    qt59multimedia  \
    qt59svg  \
    qt59tools

source /opt/qt511/bin/qt511-env.sh
```

To use this installation, you will need to call `/opt/qt511/bin/qt511-env.sh` (or `/opt/qt59/bin/qt59-env.sh` on 14.x/16.x) every time you open a new terminal. You can do this by adding the `source ...` line above to your `~/.bashrc` file (or whatever shell you use).

!!! info "16.04 and 14.04"
    On older Ubuntu releases, you can use `ppa:beineri/opt-qt596-xenial` and `ppa:beineri/opt-qt596-trusty`.

### Arch

If you're using **Arch**, you can get Qt from AUR; here's the relevant [wiki page](https://wiki.archlinux.org/index.php/qt#Installation).

## Windows

### MSYS2

Qt is available in the MSYS2 repos. See [https://wiki.qt.io/MSYS2](https://wiki.qt.io/MSYS2).

### vcpkg

At the time of writing, Qt 5.9 is available in vcpkg as a port.

## macOS

### Homebrew

Qt is available in the Homebrew repos, but may not be up to date. See [http://brewformulas.org/qt5](http://brewformulas.org/qt5).

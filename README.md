# debian-flatpak-firefox
Debian (stable release) ships Firefox ESR by default. This version of Firefox lags behind the regular release. Those who wish to use up-to-date Firefox on Debian could install the [flatpak version](https://flathub.org/apps/details/org.mozilla.firefox). This script will:

* Install the flatpak version of Firefox.
* Install ffmpeg-full to fix a [video lag bug](https://bugzilla.mozilla.org/show_bug.cgi?id=1628203).
* Install fonts.conf to fix a [fuzzy font bug](https://bugzilla.mozilla.org/show_bug.cgi?id=1621915).

I have not tested the script on other systems, but it should also work on other branches of Debian (e.g. testing, unstable) and other Debian-based systems (e.g. Ubuntu).

## Requirements
This script requires that the `flatpak` package is already installed system-wide. It can be installed by executing the following as root or superuser:
```
apt update
apt install flatpak
```

## Usage
1. Download the script to the Debian system.
2. Make the script executable: `chmod +x debian-flatpak-firefox`.
3. Execute `./debian-flatpak-firefox` from the directory where the script is located to install it for the current user.

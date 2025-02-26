---
title: Download Linux
eleventyNavigation:
  key: <i class="fa fa-linux" aria-hidden="true"></i>Linux
  order: 3
---

<div class="download-content">
  <div class="row">
    <div class="column">
      <div>
        <h1>Linux Download</h1>
        <br>
        <a class="button is-big" href="https://flathub.org/apps/details/org.polymc.PolyMC">Install from FlatHub</a>
        <a class="button is-big" href="https://github.com/PolyMC/PolyMC/releases/download/{{version.current}}/PolyMC-Linux-{{version.current}}-x86_64.AppImage">Download (AppImage)</a>
        <a class="button is-big" href="https://github.com/PolyMC/PolyMC/releases/download/{{version.current}}/PolyMC-Linux-{{version.current}}.tar.gz">Download (tar.gz)</a>
        <a class="button is-big" href="https://github.com/PolyMC/PolyMC/releases/download/{{version.current}}/PolyMC-Linux-portable-{{version.current}}.tar.gz">Download Portable (tar.gz)</a>
      </div>
    </div>
    <div class="column">
      {% image "Modpack Installer", "./src/img/screenshots/LauncherLight.png", "./src/img/screenshots/LauncherDark.png" %}
    </div>
  </div>
</div>

<div class="infobox top">

# <img src="https://www.vectorlogo.zone/logos/archlinux/archlinux-icon.svg" height="20"/> Arch Linux / Manjaro

There are several AUR packages available:  
[![polymc](https://img.shields.io/badge/aur-polymc-blue)](https://aur.archlinux.org/packages/polymc/)  
[![polymc-bin](https://img.shields.io/badge/aur-polymc--bin-blue)](https://aur.archlinux.org/packages/polymc-bin/)  

```
# stable source package:
yay -S polymc
# stable binary package:
yay -S polymc-bin
# latest git package:
yay -S polymc-git
```
You can replace yay -S with your preferred [AUR helper's](https://wiki.archlinux.org/title/AUR_helpers) install command.
</div>

<div class="infobox top">

# <img src="https://www.vectorlogo.zone/logos/debian/debian-icon.svg" height="20" /> Debian / Ubuntu

We use [makedeb](https://docs.makedeb.org/) for our Debian packages.  
Several MPR packages are available:

[![polymc](https://img.shields.io/badge/mpr-polymc-orange)](https://mpr.makedeb.org/packages/polymc)  
[![polymc-bin](https://img.shields.io/badge/mpr-polymc--bin-orange)](https://mpr.makedeb.org/packages/polymc-bin)  

## Installation using Prebuilt MPR (recommended)

```
curl -q 'https://proget.makedeb.org/debian-feeds/prebuilt-mpr.pub' | gpg --dearmor | sudo tee /usr/share/keyrings/prebuilt-mpr-archive-keyring.gpg 1> /dev/null
echo "deb [signed-by=/usr/share/keyrings/prebuilt-mpr-archive-keyring.gpg] https://proget.makedeb.org prebuilt-mpr $(lsb_release -cs)" | sudo tee /etc/apt/sources.list.d/prebuilt-mpr.list
sudo apt update
sudo apt install polymc
```
NOTE: Prebuilt MPR only officially supports Debian 11 and Ubuntu 20.04, but you can change the '$(lsb_release -cs)' to focal or bullseye if you are in another distribution.    

## Installing with an MPR helper 

Installing UNA

```
bash <(curl -fsL https://github.com/AFK-OS/una/raw/main/install.sh)

una update
```
            
Installing PolyMC 

```
# stable source package:
una install polymc
# stable binary package:
una install polymc-bin
# latest git package:
una install polymc-git
```
You can replace una install with your preferred [MPR helper's](https://docs.makedeb.org/using-the-mpr/list-of-mpr-helpers/) install command.
</div>

<div class="infobox top">

# <img src="https://www.vectorlogo.zone/logos/getfedora/getfedora-icon.svg" height="20"> Fedora & CentOS Stream

Two RPM packages are available on [Copr](https://copr.fedorainfracloud.org/coprs/sentry/polymc/).

```
# enables copr repo
sudo dnf copr enable sentry/polymc
# stable releases
sudo dnf install polymc
# nightly releases (git master)
sudo dnf install polymc-nightly
```
</div>

<div class="infobox top">

# <img src="https://www.gentoo.org/assets/img/logo/gentoo-signet.svg" height="20" /> Gentoo

Ebuilds are available in the official Gentoo repository, under [`games-action/polymc`](https://packages.gentoo.org/packages/games-action/polymc). 
Note that, for the time being, it is not stabilized, so it's masked for `~amd64` only.

```bash
sudo emaint sync -a

# If you need to unmask the package, and considering `package.accept_keywords` to be a folder.
echo ">=games-action/polymc-1.1.1" | sudo tee -a /etc/portage/package.accept_keywords/polymc
# Or do this if you want to build from the latest commit instead of a release
echo "=games-action/polymc-9999 **" | sudo tee -a /etc/portage/package.accept_keywords/polymc

emerge games-action/polymc
```

Old ebuilds, as well as additional information, can be found [in the old polymc overlay repository](https://gitlab.com/flowln/polymc-gentoo/). Have fun! :)
</div>

<div class="infobox top">

# <img src="https://www.vectorlogo.zone/logos/nixos/nixos-icon.svg" height="20" /> Nix

A [Nix derivation](https://github.com/PolyMC/PolyMC/blob/develop/packages/nix/NIX.md) is available.
</div>

<div class="infobox top">

# <img src="https://upload.wikimedia.org/wikipedia/commons/d/d0/OpenSUSE_Logo.svg" height="20"> openSuse

An RPM package is available on [Copr](https://copr.fedorainfracloud.org/coprs/sentry/polymc/).

```
. /etc/os-release

curl "https://copr.fedorainfracloud.org/coprs/sentry/polymc/repo/$ID/sentry-polymc-$ID.repo" | sudo tee "/etc/zypp/repos.d/sentry-polymc-$ID.repo"
```
</div>

<div class="infobox top">

# <img src="https://bitcu.co/en/wp-content/uploads/2020/07/Void_Linux_logo.svg_.png" height="20"> Void Linux

PolyMC is available on the official Void repository.

```
sudo xbps-install PolyMC
```
</div>

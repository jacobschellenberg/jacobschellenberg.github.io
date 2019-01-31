---
layout: post
title:  "Ubuntu Setup"
date:   2019-01-30 07:00:00 -0700
category: [blog, daily]
---

I've been on a security/privacy binge these last couple weeks. I can't put my finger exactly on what kicked it off, but it comes down to this: _I want control over my data._ This is less of a blog post, and more of a reference to the things that I did to help secure and take control of my data. I'd say it's mostly for future me, since it's specific to my hardware and needs, but perhaps there is something in here that will help you. Take a gander.

# Intial Setup
## Helpful Commands

### Update Packages
* `sudo apt-get update` # must run first

* `sudo apt-get install` # then run to install updates

### Fix Package Dependencies
* If a `sudo apt-get install *.package` fails, follow it with:
* `sudo apt-get -f install`

### Install Package
* `sudo dpkg -i *.deb`

### Extract tarball.tar
* `tar -xvf *.tar`

* -x : Extract a tar ball.
* -v : Verbose output or show progress while extracting files.
* -f : Specify an archive or a tarball filename.
* -j : Decompress and extract the contents of the compressed archive created by bzip2 program (tar.bz2 extension).
* -z : Decompress and extract the contents of the compressed archive created by gzip program (tar.gz extension).

## Late 2013 Macbook Pro Specific
### Wireless Driver
* If you don't tether via bluetooh, you'll have to gather all the dependencie files from another machine.
* Wait you don't have another machine? Chicken/Egg!

1. Tether to bluetooth internets (tethered to my android phone)
2. sudo apt-get update
3. sudo apt-get install
4. Copy `pool > restricted > b > bcmwl > *.deb` to desktop
5. Copy `pool > main > d > dkms > *.deb` to desktop
6. Open Terminal to desktop
7. sudo dpkg -i *.deb

* [https://packages.ubuntu.com/trusty/admin/bcmwl-kernel-source](https://packages.ubuntu.com/trusty/admin/bcmwl-kernel-source)

### Computer Setup
* Firefox addons:
* Privacy Badger: [https://www.eff.org/privacybadger](https://www.eff.org/privacybadger)
* uBlock Origin: [https://addons.mozilla.org/en-GB/firefox/addon/ublock-origin/](https://addons.mozilla.org/en-GB/firefox/addon/ublock-origin/)
* Cookie AutoDelete: [https://addons.mozilla.org/en-GB/firefox/addon/cookie-autodelete/](https://addons.mozilla.org/en-GB/firefox/addon/cookie-autodelete/)
* HTTPS Everywhere: [https://www.eff.org/https-everywhere](https://www.eff.org/https-everywhere)
* Decentraleyes: [https://addons.mozilla.org/en-GB/firefox/addon/decentraleyes/](https://addons.mozilla.org/en-GB/firefox/addon/decentraleyes/)

### Change splash screen
* Themes used to be installed in a different location. Just use the new location and you should be good.
* New location is: `/user/share/plymouth/themes/`

* `sudo cp -R ./vinyl /usr/share/plymouth/themes/` # copy the theme directory to the new location

* `sudo ln -sf /usr/share/plymouth/themes/vinyl/vinyl.plymouth /etc/alternatives/default.plymouth` # create a link and copy contents to the default.plymouth file

* `sudo update-initramfs -u -k all` # Update the bootloader/splash screen references?

### Gnome Tweak Tool
* Use this to hide the trashcan...
* `sudo apt install gnome-tweak-tool`

### Helpful Links:
* Privacy Tools: [https://www.privacytools.io/](https://www.privacytools.io/) # Follow the Firefox about:config stuff

### Things to Install
* `sudo apt install tlp` # auto battery management - better battery life
* `sudo apt install git` # source control
* `sudo apt install vscode` # programming, dotnet core
* `sudo apt install gnome-tweak-tool` # Hide the trashcan on desktop

### RUBY
* `sudo apt install ruby`
* `sudo apt install ruby-bundler`

### JEKYLL
* The quick start on the Jekyll home page didn't work for me, I had to follow these steps.
[https://jekyllrb.com/docs/installation/ubuntu/](https://jekyllrb.com/docs/installation/ubuntu/)
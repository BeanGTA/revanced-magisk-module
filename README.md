# YouTube ReVanced Magisk Module

<sub>(unaffiliated whatsoever)<sub>

This repo includes a simple script that downloads all the latest version of necessary prebuilt revanced tools and the stock APKs of YouTube and YouTube Music from APKMirror, applies the patches and creates magisk modules.

You will need to install the stock YouTube app matching with the module's version on your phone, there is no need for the split APKs or SAI anymore, the regular APK is just fine. The link is also provided in release notes.

You can get the [latest CI release](https://github.com/j-hc/revanced-magisk-module/releases) from here.

## Updating
The modules support Magisk update which means you will receive updates from your Magisk app, downloading from github releases and reflashing is not necessary.

### Note
If you wish to include/exclude some patches to your liking:
 * Star the repo :eyes:
 * Fork the repo
 * Edit the patcher args in [`build.sh`](./build.sh)
 * Start the workflow to build

# Building the Magisk Modules

```bash
sudo apt-get update && sudo apt-get upgrade -y && \
sudo apt-get -yq install gnupg curl && \
sudo apt-key adv \
  --keyserver hkp://keyserver.ubuntu.com:80 \
  --recv-keys 0xB1998361219BD9C9 && \
wget https://cdn.azul.com/zulu/bin/zulu-repo_1.0.0-3_all.deb && \
sudo apt-get install ./zulu-repo_1.0.0-3_all.deb && \
sudo apt-get update && \
sudo apt-get install zulu17-jdk -y && \
sudo apt-get install zip -y && \
sudo apt-get install binutils -y && \
git clone https://github.com/BeanGTA/revanced-magisk-module.git && \
cd revanced-magisk-module && \
./build.sh all
```

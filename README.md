# Final Fantasy XI ONLINE - Linux Installation Instructions

## Download the game files (optional)

1. First step is optional as Lutris can do this for you.

2. Download our [download](https://vana-time.com/api/v1/downloads/ffxiDownload.sh) script or go to [PlayOnline](http://www.playonline.com/ff11us/download/media/install_win.html) website and download them manually. 

3. Store the files in your `downloads folder`. 

> **Information**
>
> If you're on Arch or a Arch based distro do the following

> **Warning**
> 
> Before running the below script, feel free to [inspect](https://github.com/Mandracord/ffxi-linux-installer/blob/main/lutris-fix) it first. 

1. Open a terminal and run the following command: `curl -fsSL https://mandracord.com/lutris-fix | sh` 
*This will append a fix to your lutris installation to enable [this fix](https://forums.lutris.net/t/errno-104-connection-reset-by-peer/25137/12)* 

![alt text](https://github.com/Mandracord/ffxi-linux-installer/blob/main/assets/1.png?raw=true)

*TUI guide* 

## Optional: Download ProtonPlus flatpak

In order to sandbox wine and proton versions and switch between it's strongly recommended using some form of Proton manager, like ProtonPlus.

Run the following command in a terminal or open your store app if you've already enabled Flatpak support: `flatpak install flathub com.vysp3r.ProtonPlus` 

## Install using Lutris

1. Open Lutris and let it install any dependencies it requires. 

![alt text](https://github.com/Mandracord/ffxi-linux-installer/blob/main/assets/lutris-1.png?raw=true)

2. Press the [+] button in the upper-left corner

![alt text](https://github.com/Mandracord/ffxi-linux-installer/blob/main/assets/lutris-2.png?raw=true)

3. Press the top option "Search Lutris website for installers" and search "Final Fantasy XI Online" and select "Final Fantasy XI ONLINE", first result.

![alt text](https://github.com/Mandracord/ffxi-linux-installer/blob/main/assets/lutris-3.png?raw=true)

4. For best compatablity for Windower and DXVK, select "Full (US) version with D8VK"

*Ignore it says D8VK which is included in DXVK, it will still run without problems*

![alt text](https://github.com/Mandracord/ffxi-linux-installer/blob/main/assets/lutris-4.png?raw=true)

5. Select installation path, keep default unless you know what you're doing

6. If you downloaded the files manually or using the download script mentioned earlier in this readme, pick "Select file" for the installation files and navigate to where you saved them.

7. Press "Install"

8. This will take a while, let is do it's thing.

## Install Windower

1. Repeat all the steps from "Install using Lutris" until you get to select what installer to use, pick "Windower 4 Live". 

> **Warning**
>
> You must installed the game using the script called "Full (US) version with D8VK" else the Windower install script will fail

2. This can take a while to install all the wine dependencies. 

3. Optional: Install additional fonts using Winetricks. 

![alt text](https://github.com/Mandracord/ffxi-linux-installer/blob/main/assets/lutris-5.png?raw=true)

*Open Winetricks*

![alt text](https://github.com/Mandracord/ffxi-linux-installer/blob/main/assets/lutris-6.png?raw=true)

*Press OK*

* You might get a popup about sharing report statistics, select YES|NO 

![alt text](https://github.com/Mandracord/ffxi-linux-installer/blob/main/assets/lutris-7.png?raw=true)

*Install a Font*

* Select the fonts you wish to install. Suggested to at least install "Consolas".

* You may see some popup warnings, just press OK to progress. Eventuelly you'll see the winetricks popup again then it'll be installed.

* Alternatively you can run it in a terminal with these commands:

If you didn't change your install path:

```bash
export WINEPREFIX=~/Games/final-fantasy-xi-online
cd ~/Games/final-fantasy-xi-online
winetricks consolas 
```

* And you'll see an output similar to this: 

```bash
------------------------------------------------------
warning: You are using a 64-bit WINEPREFIX. Note that many verbs only install 32-bit versions of packages. If you encounter problems, please retest in a clean 32-bit WINEPREFIX before reporting a bug.
------------------------------------------------------
Using winetricks 20250102 - sha256sum: 53194dead910f8a5eb1deacaa4773d4e48f5873633d18ab1ecd6fdb0cb92243b with wine-10.0 (Debian 10.0~repack-6) and WINEARCH=win64
Executing w_do_call consolas
------------------------------------------------------
warning: You are using a 64-bit WINEPREFIX. Note that many verbs only install 32-bit versions of packages. If you encounter problems, please retest in a clean 32-bit WINEPREFIX before reporting a bug.
------------------------------------------------------
consolas already installed, skipping
```
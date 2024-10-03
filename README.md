# b43-more-wifi-channels
Patches to compile Openwrt 12.09 (codename Attitude Adjustment) with more wifi channels in b43 driver.
Only for old 802.11g wifi cards like Broadcom BCM4318.

You may need an old Linux distro to compile this ancient OpenWrt version (around 2014).

1. Download Attitude Adjustment version 12.09.1  
```sh
git clone -b attitude_adjustment git://git.openwrt.org/openwrt/svn-archive/openwrt.git attitude_adjustment
```
2. Drop patches and *patch-br.sh* script into the build root
3. Execute the script, this will apply all patches  
    `./patch-br.sh`
4. Configure Openwrt with menus, save and make the world

New frequencies added:
* 2494 - channel 15
* 2402 - channel 16

Tested on these old routers:  
* Telsey CPVA502+W with a BCM4318 onboard wifi
* Comtrend CT-5361 with a BCM4318 mini-pci wifi

Communication was succesfully made using two routes flashed with this identical patched firmware. Configured
as AP-WDS (()) CLIENT-WDS
# ArcherC7v2

this repository is used for install and update your C7 AC1750 TPLink router to run with latest openwrt


first you will need to flash dd wrt with `factory-to-ddwrt-IL.bin` special version for the IL module and then revert using webrevert bin `ArcherC7v2_webrevert.bin` and after that you can flash and run open wrt with `openwrt.bin` which is `23.05.4` version , and configutre everything as you want.

i recommended update and add to crontab this things

```
30 3 * * * reboot
* 3 * * * /bin/opkg update
10 3 * * * opkg list-upgradable | cut -f 1 -d ' ' | xargs -r opkg upgrade
```
the first are for remove unwanted if router is infected 
the sec are update to source list
and the last one is upgrade packages.

# About this fork
This fork contains only a view adjustments.
I only have inverters and no battery-stuff.
Also i added new models to the .map-File, based on this infos: https://files.sma.de/downloads/SMA_Modbus-de-en_V25.zip


# openhab_modbus_sma_inverter
This repository stores everything you need to implement SMA Inverters in openHAB with modbus protocol. All you need is an enabled modbus tcp server on your inverters, an openHAB instance with modbus binding installed and all the stuff out of this repository.

# Installation
* Activate Modbus on your Inverters and connect them to your ethernet
* Install Modbus Binding on you openHAB instance
* Install JavaScript and Map Transfomation in openHAB
* clone this git repository and store the files in the right openHAB configuration folders:

```
-rw-r--r-- 1 openhab openhab  9676 Sep 26 07:46 conf/items/sma.items
-rw-r--r-- 1 openhab openhab  2121 Nov  7 12:25 conf/rules/sma.rules
-rw-r--r-- 1 openhab openhab  2960 Jul 24 20:29 conf/sitemaps/sma.sitemap
-rw-r--r-- 1 openhab openhab 10235 Nov  7 12:15 conf/things/sma.things
-rw-r--r-- 1 openhab openhab    83 Jul  2 22:15 conf/transform/smalimit1000.js
-rw-r--r-- 1 openhab openhab    82 Jul  2 22:15 conf/transform/smalimit100.js
-rw-r--r-- 1 openhab openhab    85 Sep 11 20:43 conf/transform/smalimit10_undef.js
-rw-r--r-- 1 openhab openhab    76 Jul  2 22:14 conf/transform/smalimit.js
-rw-r--r-- 1 openhab openhab    80 Sep 11 19:01 conf/transform/smalimit_undef.js
-rw-r--r-- 1 openhab openhab   917 Jul  8 21:16 conf/transform/sma.map
```
that's it... now you should see values in your SMA Sitemap, or in the openHAB UI.

This example Configurations are for:
* SMA Sunny Tripower 8.0
* SMA SunnyBoy Storage 3.7-10

If you have to use other modbus IDs, you can download modbus documentation from:
* https://www.sma.de/service/downloads.html

# More Informations:
* https://www.laub-home.de/wiki/OpenHAB_SMA_Wechselrichter_mittels_Modbus_einbinden

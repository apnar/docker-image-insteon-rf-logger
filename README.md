# Container to log Insteon RF traffic using rfcat dongle




Example to run:
```
docker run -d \
           --name insteon \
           --device /dev/bus/usb/003/004 \
           -v [data dir]:/data \
           apnar/insteon-rf-logger
```

Hardware needed:

You’ll need some hardware to actually talk RF, there are a number of options evilpete’s software supports but for someone who is only going to use the hardware for working with Insteon (as opposed to broader RF hacking) the cheapest and easiest is something using the TI cc1111 chip.  The chip then needs to be programed with a firmware called rfcat.

If I were to do this again I would purchase a device called the Yard Stick One.  It has the proper chip and is also pre-flashed with the rfcat firmware.  As such it should be plug-and-play.  Depending on antenna choice you’re looking at around $100-$129 for it:

https://greatscottgadgets.com/yardstickone/
https://hakshop.myshopify.com/products/yard-stick-one?variant=6649135621

The other option, which I went with before finding the yard stick one, is to buy a cc1111 evaluation board from TI called the CC1111EMK868-915.  You can buy it directly from TI or many other of the usual electronics distribution houses for around $75:

http://www.ti.com/tool/cc1111emk868-915

The problem is that it doesn’t come with the rfcat firmware installed and you need another device to program it.  I opted to get a board called the GoodFET to do the firmware flashing.  It unfortunately ran another $50 which was a little pricey for a one time use device, at least I could get it Prime.  If anyone wants me to flash their CC1111EMK868-915 with rfcat for them I’m happy to do so, just message me.

http://goodfet.sourceforge.net/
http://smile.amazon.com/Hackaday-Goodfet42/dp/B015P8219Y/
https://www.adafruit.com/products/1279


Forum Thread:
https://forum.universal-devices.com/topic/17474-how-to-receive-send-log-spoof-all-insteon-rf-traffic/


ESP8266 WeMos Shield for HopeRF RFM69 and RFM12 Modules
=======================================================

This shield is used to hold HopeRF RF [module][4] Software with WeMos ESP8266 boards it has just few minimal features. 
- I2C Pullups placement
- Classic I2C 128x64 OLED connector
- Placement for RFM12B/RFM69CW/RFM69W/RFM69HW RF module
- Placement for choosing single Wire, SMA or u-FL Antenna type
- 2 x WS2812B Type LED for visual indication
- Atmel ATSHA204 for crypto
- Custom switch on GPIO2

You can find more information on WeMos on their [site][1], it's really well documented.
I now use WeMos boards instead of NodeMCU's one because they're just smaller, features remains the same, but I also suspect WeMos regulator far better quality than the one used on NodeMCU that are just fake of originals AMS117 3V3.

Boards heve been tested with RFM69HW and are working fine, no problem so far, just a silk error on V1.0, RFM module indication is reversed.
This mean that RFM69W/RFM69HW is for RFM12B/RFM69CW and vice-versa, please check with module pinout before soldering.
**This have been corrected on V1.0a+ release**

**I didn't tested with RFM12/RFM69CW module.** If someone tested and have it working (or not), please let me know.

Detailed Description
====================

Look at the schematics for more informations.

### Schematic  
![schematic](https://raw.githubusercontent.com/hallard/WeMos-RFM69/master/pictures/WeMos-RFM69-sch.png)  


Diode D1 (1N4148) is for level voltage of WS2812B. Decreasing 1st led to VCC to 4.3V (see this [post][5]) but It should works out of the box (so without D1 and JP4 closed) without any problem. 
Depending on WS2812 type, if it does not work or flicker, open JP4 (cut wire) and put D1 in place.

### Boards  
<img src="https://raw.githubusercontent.com/hallard/WeMos-RFM69/master/pictures/WeMos-RFM69-top.svg" alt="Top">&nbsp;
<img src="https://raw.githubusercontent.com/hallard/WeMos-RFM69/master/pictures/WeMos-RFM69-bot.svg" alt="Bottom"> 

You can order the PCB of this board at [PBCs.io][3], if you do so, PCBs.io give me little discount that allow me to buy new boards.

### Assembled boards

I currently have the boards from OSHPARK but dit not tested them yet

##License

You can do whatever you like with this design.

##Misc
See news and other projects on my [blog][2] 
 
[1]: http://www.wemos.cc/wiki/doku.php?id=en:d1_mini
[2]: https://hallard.me
[3]: https://PCBs.io/share/8Vkkr 
[4]: http://www.hoperf.com/rf_transceiver/modules/
[5]: http://www.electrobob.com/ws2812-level-translator/


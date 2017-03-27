# PMSensorNet

# Particulate matter matters particularly
Particulate matter (PM) or particulates – are microscopic solid or liquid matter. PM of a size between 2.5 and 10 micrometres (μm) are a WHO group 1 carcinogen. In plain English - very cancerous. "In 2013, a study involving 312,944 people in nine European countries revealed that there was no safe level of particulates and that for every increase of 10 μg/m3 in PM10, the lung cancer rate rose 22%. The smaller PM2.5 were particularly deadly, with a 36% increase in lung cancer per 10 μg/m3 as it can penetrate deeper into the lungs."

https://en.wikipedia.org/wiki/Particulates

So PM is bad, bad bad and you should know how much of it is in the air you breathe.

# Project scope
This project attempts to quantify PM using a network of cheap COTS (commercial off the shelf) sensors. You will find everything to buy, build and run a sensor. You would not be reading this README.md without the work of the original team, http://luftdaten.info/feinstaubsensor-bauen/ and https://github.com/opendata-stuttgart/feinstaub-map. I am very grateful for the work these teams have done. 

This is the first US-installed sensor in Portland, Oregon: https://opensensemap.org/explore/58d82cf2b69fac0011215087, measuring temperature in Celcius, humidity and PM2.5 and PM10.

# Project purpose
The purpose of this repository is to equip you with a checklist and steps. You should be able to get your sensor running within half hour if you have all parts.

# Motivation
The city of Portland in Oregon has some dirty secrets. When I moved here, I didn't know that 

1. Precision Castparts Corp. is the number one air polluter in the U.S. (disputed by PCC, not surprisingly) https://en.wikipedia.org/wiki/Precision_Castparts_Corp.#cite_note-19
2. Glas production facilities within residential neighborhoods emit large amounts of toxic heavy metals such as lead, arsenic and cadmium
3. The agency entrusted with making sure our water is clean and the air is fresh is not positioned to do just that.
4. Emission control standards in the United States are much, much weaker than in the European Union.



# Hardware

Here is what you need to buy:

1. NodeMCU ESP8266 ($9) CPU/WLAN https://www.amazon.com/gp/product/B010O1G1ES/ref=oh_aui_detailpage_o05_s00?ie=UTF8&psc=1
2. SDS011 ($24) fine particulate sensor http://www.ebay.com/itm/291919396235
3. DHT22 ($12) temperature & humidity sensor (optional) https://www.amazon.com/gp/product/B0130I6MIC/ref=oh_aui_detailpage_o05_s00?ie=UTF8&psc=1
4. cables 
5. 6ft Micro-USB cable
6. Power supply for USB device 
7. Housing for the device

Total cost for all components was about $50.

# Software

Once you have aquired the hardware and assembled it, you need to flash the firwmware for the Arduino. 

1. Install Arduiono: https://www.arduino.cc/en/Main/Software
2. Go to Arduiono settings and add URL into "Additional Board Manager URLs" http://arduino.esp8266.com/stable/package_esp8266com_index.json
3. Go to "Tools -> Board -> Board manager“ and search for "esp8266", then install "esp8266 by ESP8266 Community"
installieren
4. Download firmware https://www.madavi.de/sensor/update/data/latest.bin

## If you are on a Mac, do this:
1. Open "Terminal" app
2. Flash firmware using the following command:
    ~/Library/Arduino15/packages/esp8266/tools/esptool/0.4.9/esptool -vv -cd nodemcu -cb 57600 -ca 0x00000 -cp /dev/cu.$TTYUSBYOUNEEDTOSPECIFY -cf ~/Downloads/latest.bin
## If you are on a Windows PC, do this:
## If you are on a Linux PC, do this:

# Data

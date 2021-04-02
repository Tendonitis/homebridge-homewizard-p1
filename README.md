# homebridge-homewizard-p1

This does not work yet. It is in Development.

Supports HomeWizard Wifi P1 devices on the Homebridge platform. Additional hardware required.
This is a modified version of the https://github.com/crashtestoz/homebridge-http-lux plugin.
This version only supports the light sensor. Lightlevel is the amount of watts you are returning or receiving.









FROM PREVIOUS PLUGIN

# Installation

1. Install homebridge using: npm install -g homebridge
2. Install this plugin using: npm install -g homebridge-http-lux
3. Update your configuration file. See sample-config.json in this repository for a sample.

# Configuration


Configuration sample file:

 ```
 "accessories": [
     {
         "accessory": "HttpLux",
         "name": "Ambient Light Level",
         "url": "http://192.168.0.20/api/lightlevel",
         "http_method": "GET"
     }
 ]

```


The defined endpoint will return a json looking like this
```
{
	"lightlevel": 450
}
```


This plugin acts as an interface between a web endpoint and homebridge. You will need additional hardware to expose the web endpoints with the light level information. I built my Temperature, Humidity and Light Sensor on the NodeMCU board with Arduino IDE.

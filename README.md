# WiFi-Sunrise-Alarm-Clock

ESP8266 microcontroller with DS3231m RTC to control an RGBW LED strip and turn it into a web interfaceable sunrise alarm (Lichtwecker!)

An ESP32-S compatible sketch is available as well!

https://www.youtube.com/watch?v=NbgbeNN9tp0

## Idea

Making a DIY sunrise alarm with a RGBW LED strip that can be controlled through a web browser. The simulated sunrise that wakes you up softly.

## Setup & Functions

In this project I used an Adafruit Feather Huzzah ESP8266, with DS3231m RTC to control a RGBW LED strip through N-channel MOSFET's. The microcontroller is connected to the home WiFi network and can be controlled from any device that can run a browser. 

A parts list and more detailed descriptions of the project (schematics, PCB desgin, etc.) can be found on https://www.aufbauprinzip.com/home/esp8266-color-mixer-using-javascript

### Functions

<img src="images/interface.png" width="200"> <img src="images/interface2.png" width="200">

* toggle individual LED's with corresponding buttons (Red, Green, Blue or White)
* toggle "Night Light" (mix of RGB to give a soft purple light)
* set alarm time (in 24h format)
* reset button, which will appear after setting the alarm time
* LED strip blinks red when RTC can not be initialized


## Getting Started



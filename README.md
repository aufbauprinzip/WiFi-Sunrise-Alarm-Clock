# Light-Alarm-Clock

ESP8266 microcontroller with DS3231m to control an RGBW LED strip and turn it into a web interfaceable light alarm (Lichtwecker!)

## Idea

Making an DIY light alarm with a RGBW LED strip. The light alarm will simulate the sunrise the sunrise to wake you up softly.

## Setup & Functions

In this project I used an Adafruit Feather Huzzah ESP8266, with DS3231m RTC to control a RGBW LED strip. The microcontroller is connected to the home WiFi network and can be controlled from any device that can run a browser. 

### Functions

<img src="images/interface.png" width="200"> <img src="images/interface2.png" width="200">

* toggle individual LED with corresponding button (Red, Green, Blue or White)
* toggle "Night Light" (mix of RGB)
* set alarm time (in 24h format)
* reset button will appear after setting alarm time
* blinks red when RTC can not be initialized


## Getting Started

Change WiFi-Name and WiFi-Password to your credentials:
```c
// SSID of WiFi network and password of WiFi network
const char* ssid = "WiFi-Name";
const char* password = "WiFi-Password"; 
```

Change Pins to whatever you are using:
```c
//Assigning variables for LED pins
uint8_t WHITEpin = 15;
uint8_t BLUEpin = 13;
uint8_t REDpin = 14;
uint8_t GREENpin = 12;
```

Set intial time of RTC by commenting this line and setting the current time. After setting the time, comment this line again and upload it to the microcontroller again. The DS3231(M) can also fetch the time automatically the time from the internet. I didn't wanted to relay on a internet connection with this code though. Once the time is set, the DS3231(M) is very reliable and can hold the time untile the 3V battery runs out (years, if not decades)
```c
  //DS3231M.adjust(DateTime(2020, 4, 4, 13, 04, 00)); // Sets time of DS3231M
```

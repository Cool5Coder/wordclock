# WordClock
[![Version](https://img.shields.io/badge/version-4.0.0-green.svg?style=for-the-badge)](#) [![mantained](https://img.shields.io/maintenance/yes/2020.svg?style=for-the-badge)](#)

[![maintainer](https://img.shields.io/badge/maintainer-Goran%20Zunic%20%40panbachi-blue.svg?style=for-the-badge)](https://www.panbachi.de)


# Requirements

## Healthcheck
* [FastLED](https://github.com/FastLED/FastLED)

## WordClock
* [FastLED](https://github.com/FastLED/FastLED)
* [NTPClient](https://github.com/arduino-libraries/NTPClient)
* [WifiManager](https://github.com/tzapu/WiFiManager)
* [ArduinoJson](https://github.com/bblanchon/ArduinoJson)

# Assemble
[![Word-Clock - Die WLAN Wort-Uhr zum selber bauen](https://img.youtube.com/vi/FvAM1t0tISE/0.jpg)](https://www.youtube.com/watch?v=FvAM1t0tISE)

# Customizations
## Modify `user_config.h` to change config
| Key                 | Values                                                           | Comment                  |
|---------------------|------------------------------------------------------------------|--------------------------|
| GRID_ROWS           | 10<br>11                                                         | count of rows            |
| GRID_COLS           | 11                                                               | count of cols            |
| GRID_FIRST          | 0: top-left<br>1: top-right<br>2: buttom-left<br>3: buttom-right | position of first led    |
| GRID_LANGUAGE       | de_DE: german<br>de_DE_alt: german alternative                   | langauge                 |
| GRID_SINGLE_MINUTES | 0: before<br>1: after                                            | position of minutes leds |

# Installation
Make your Arduino ready for Wemos D1 mini e.g. https://makesmart.net/blog/read/esp8266-d1-mini-programmieren-der-start-mit-der-arduino-ide
- Change the grid settings in the `wordclock/user_config.h`.
- Upload the sketch `wordclock/wordclock.ino` to your Wemos D1 mini (or other ESP8266).
- Enjoy


# Usage
The WordClock creates a WiFi-Hotspot with the name "WordClock". Connect e.g. your smartphone to the hotspot and you will be forwared to the config page, where you can set the WiFi credentials.
Check in your router what IP-adress your WordClock got. Open a webbrowser and go to `http://[YOUR_WORDCLOCK_IP]`. For (example) the IP-adress `192.168.178.20` go to `http://192.168.178.20`.

# Functions

## Set color
You can set a foreground and background color on your clock.

## Set time offset
You can set a time offset to specify your timezone.

## Set DND
You can set a time span in which the clock should be switched off.

## PWA
You can use the webbrowser function "Add to start screen" to install the webinterface as an app to your android (and possibly ios) smartphone.

# Create own grid-layout
To create your own grid-layout visit the Wiki: [Create Grid-Layout](https://github.com/panbachi/wordclock/wiki/Create-Grid-Layout)


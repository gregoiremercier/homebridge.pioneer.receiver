# homebridge-pioneer-SC-LX88
This project was forked from [homebridge-pioneer-avr](https://github.com/kazcangi/homebridge-pioneer-avr).
homebridge-pioneer-avr is a plugin made for [homebridge](https://github.com/nfarina/homebridge),
which declare your Pioneer AVR as a TV in homekit (iOS 12.2+ needed).
It should work with Pioneer AVRs supported by the iControl AV5 App.

For me (Pioneer SC-LX88) the original module made my homebridge crash while checking the available inputs.
So I changed some settings in order to finish scanning the inputs with no crashing.

## Features

Declare your AVR as a homekit TV :
* Turn AVR On/Off
* Auto discover inputs
* Select active input in home app
* Select inputs to shown in the input list
* Save visibility status for inputs
* Rename inputs in home apps
* Control volume through the command in control center
* Control AVR with Remote in Control Center on iOS

## Installation

This plugin is not yet on NPM. Insatllation only via GitHub at the moment...

1. Install the homebridge framework using `npm install -g homebridge`
2. Install **homebridge-pioneer-SC-LX88** using `npm i homebridge-pioneer-sc-lx88`
3. Update your configuration file. See `sample-config.json` in this repository for a sample.

## Accessory configuration example

```json
"accessories": [
	{
        "accessory": "pioneerAvrAccessory",
        "model": "SC-LX88",
        "name": "My Pioneer AVR",
        "description": "AV Receiver",
        "host": "192.168.1.128",
        "port": 23
	}
]
```

*Notice: If port 23 does not work, try port 8102.

## Links

https://github.com/rwifall/pioneer-receiver-notes

https://github.com/merdok/homebridge-webos-tv

https://github.com/TG908/homebridge-vsx

## Release Notes

### v0.8.4
* More bugs fixed

### v0.8.3
* Fixed bugs

### v0.8.2
* Fixed functionality for the Pioneer SC-LX88

### v0.8.1

* Modify telnet-avr to comply with RS232 specs

### v0.8.0

* Completely rewrite communication with AVR

### v0.7.0

* Use AVR's web interface if available

### v0.6

* First support for remote keys (through Control Center -> Remote on iOS)

### v0.5

* Save CurrentVisibilityState for inputs

### v0.4

* Allow to rename inputs in Home app

### v0.3

* Turn AVR On/Off
* Auto discover inputs
* Select active input in home app
* Select inputs to show in the input list
* Control volume through the command in control center with iPhone +/- buttons

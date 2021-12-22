# ESPStick

**NOTE** This project is still a **HEAVY** work in progress! Designs have not yet been tested in person and have the possibility of not working. I have board in the mail, and assembly and testing will begin as soon as I get them :)

## Purpose

The goal of this project, similar to my [ESPHub](https://github.com/emwjacobson/ESPHub) project, is a hardware and software combo project. I've always liked the idea of portable electronics, so for this project I wanted to go for a battery-first design. I wanted to be able to mount an 18650 battery on the bottom while also be able to charge it through a microusb port.

## Usage

I have designed this project alongside my [ESPStick](https://github.com/emwjacobson/ESP32_Wifi_Toolkit) repo, but any code can be ran on it!

One thing to note about this board, is that the two buttons on it are **NOT** the typical Reset and Boot buttons found on other boards. Instead these are wired to the GPIO pins and can be used in software!

## Schematic

![Schematic](images/schematic.png)

## Design Model

![Model](images/model.png)

## History

### v0.2

After assembling a couple v0.1 boards I noticed that there was a problem near the TP4056 IC. I when I got near pin 1 (sometimes I didn't even have to touch, just move my hand near it) the board would disconnect. I realized that this was caused because I left the TEMP pin floating instead of connecting it to ground. I also realized that when powered via the battery, there was no LED to indicate that anything was powered, which made testing somewhat hard to do.

In v0.2 I have added an power LED as well as connecting the TEMP pin to ground to keep the TP4056 stable.

(I also fixed the schematic having the wrong revision number on it!)

### v0.1

This was the initial board design. It featured a MicroSD card slot as well as circuitry to manage an attached battery.
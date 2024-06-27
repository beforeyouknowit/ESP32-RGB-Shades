# ESP32 RGB Shades
![ESP32 RGB Shades front printed circuit board render](https://github.com/beforeyouknowit/ESP32-RGB-Shades/blob/main/renders/front.png "ESP32 RGB Shades front printed circuit board render")
![ESP32 RGB Shades rear printed circuit board render](https://github.com/beforeyouknowit/ESP32-RGB-Shades/blob/main/renders/rear.png "ESP32 RGB Shades rear printed circuit board render")

This repo currently represents an electronics update, based on the  ESP32 Pico Mini, as a redesign of [macetech/RGBShades](https://github.com/macetech/RGBShades) from 2015.

I was one of the Kickstarter backers of macetech's original campaign for "RGB Shades", described here: https://www.kickstarter.com/projects/macetech/rgb-led-shades

Redesigned in KiCad 8.x, based on original Eagle files from Macetech's website.

## Features
New electronics include:
- USB-C PD via STUSB4500 IC, which negotiates with USB-C PD supplies (e.g. modern power bank batteries and wall adapters) for 20V output, up to 5A, or 100W.
- TDK ICS-43434 microphone, with I2S digital output, for onboard audio analysis and beat detection.
- Jumper for selecting microphone digital output as left (default) or right channel audio over I2S.
- 5V, 1.5A linear voltage regulator for powering WS2812B LEDs from 20V USB-C PD supply.
- 3.3V, 1.0A linear voltage regulator for powering onboard ICs.
- Slight changes to rear ear-stem geometry to accommodate new USB-C PD IC and passives.

What hasn't changed:
- Same power switch.
- Same pushbuttons. (Now labeled as "Animate" and "Brightness".)
- Same CP2102N USB to UART, with "full remote reset" capabilities, making firmware flashing just as easy.
- Same 0.1" (DuPont connector/header) through-holes for direct CP2102N debug, e.g. for bypassing USB.
- Same JST connector to existing RGBShades display, i.e. the front part of the glasses assembly.
- Same glasses assembly hardware positions; meant as a direct upgrade for existing RGBShades owners.

## License
This project is licensed under CERN-OHL-S 2.0 or later version. See the LICENSE file for details.

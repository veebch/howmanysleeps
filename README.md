![Action Shot](/images/action.jpg)

[![YouTube Channel Views](https://img.shields.io/youtube/channel/views/UCz5BOU9J9pB_O0B8-rDjCWQ?style=flat&logo=youtube&logoColor=red&labelColor=white&color=ffed53)](https://www.youtube.com/channel/UCz5BOU9J9pB_O0B8-rDjCWQ) [![Instagram](https://img.shields.io/github/stars/veebch?style=flat&logo=github&logoColor=black&labelColor=white&color=ffed53)](https://www.instagram.com/v_e_e_b/)

# How Many Sleeps?

An Advent Calendar progress-bar decoration that uses a Raspberry Pi Pico W (2) to show you how many sleeps until Christmas (during Advent). It has
a light dependent resistor (LDR) to make the lights only turn on when it is dark and an override button so that you can turn 
the lights off at bedtime. 

Outside of advent, it acts as an automatic light, which is also pretty.


## Assembly

### Components

#### Electronics 

- Rasperry Pi Pico 2W (it is compatible with the original W too)
- 1m 144 LED neopixel strip (We used a WS2812 B Eco)
- Momentary Switch
- Light Dependent Resistor (LDR)

#### Enclosure
 
- Prototype board
- 1m L shaped metal strip
- 1m wooden strip (rectangular cross section) 
- 23 separator fins and two end pieces (all in [/3d](3d) directory)

## Build Video

A whizz through the build process:

[![YouTube](http://i.ytimg.com/vi/zQKZN75o05Y/0.jpg)](https://www.youtube.com/watch?v=zQKZN75o05Y)

## Wiring

The LDR and the momentary switch both go to GND from GPIO 26 and 15 respectively. 
The NeoPixel strip is connected to GPIO 19 (as well as VSYS and GND)

## Software

Copy the file main.py onto your Pico using whatever method you find easiest. For this single file, it is probably quickest just to use Thonny. Put your WiFi details into the code and that should be it!

## Operation

At dusk (the LDR value can be adjusted in the code if needed) the lights turn on. If it is currently Advent, then the bar acts as a progress bar, charting the number of sleeps until Christmas.
Outside of advent, the light will be a 'breathing' pattern.

Pressing the momentary switch will disable the lights until it gets light again. When it gets bright again, the Pico will reset.

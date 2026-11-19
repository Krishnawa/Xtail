# XPulse 200 XTail

## Overview
XTail is a custom smart tail-light controller project for the Hero XPulse 200 motorcycle using an addressable WS2812 LED strip. The project combines tail light, brake light, and turn indicator functionality with animated lighting effects.

## Features
- Tail light mode with reduced brightness
- Brake light mode with high-brightness red illumination
- Left turn indicator animation
- Right turn indicator animation
- Indicator priority over brake light
- WS2812 (NeoPixel) LED strip support
- Compact microcontroller-based design (ATtiny85 / Arduino compatible)

## Hardware
### Inputs
| Function | Pin |
|----------|-----|
| Brake Input | D2 |
| WS2812 Data Output | D3 |
| Left Indicator Input | D6 |
| Right Indicator Input | D7 |

### LED Configuration
- LED Type: WS2812B
- LED Count: 20 LEDs
- Tail Light Color: Red (Dim)
- Brake Light Color: Red (Bright)
- Indicator Color: Amber/Yellow

## Operating Modes
### Tail Light
```
RRRRRRRRRRRRRRRRRRRR
```

### Brake Light
```
RRRRRRRRRRRRRRRRRRRR
(High Brightness)
```

### Left Indicator + Brake
```
YYYYY>>>>RRRRRRRRRRR
```

### Right Indicator + Brake
```
RRRRRRRRRRR<<<<YYYYY
```

## Software
### Required Library
```cpp
#include <Adafruit_NeoPixel.h>
```

### Development Environment
- Arduino IDE 2.x
- Adafruit NeoPixel Library
- ATtiny85 Core (if using ATtiny85)

## Project Structure
```
XTail/
├── README.md
├── firmware/
│   └── xtail_controller.ino
├── hardware/
│   └── schematic.pdf
└── images/
    └── demo.jpg
```

## Future Improvements
- Hazard light mode
- Startup animation
- Dynamic brake effect
- Waterproof enclosure
- CAN bus integration

## Author
Krishnaswaroop 

## License
Personal Project

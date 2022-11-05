# Overview
## What is FarmBot
FarmBot is an opensource, microcontroller-based device, designed by Tier 10 Technology Ltd  as a platform that can be used to automate some of your gardening tasks. It is geared towards hydroponic farms, but any farming type can utilize it.

At its initial inception, the FarmBot V1.0 has connections that allow for the measurement of:

- Water/nutrient mix in reservoirs
- Water/nutrient mix temperature
- Atmospheric/Environmental temperature

## Design
As stated earlier, the FarmBot is an opensource project, designed using a microcontroller, specifically the Raspberry Pi Pico. By utilizing a microcontroller, we can enable:

1. Ease of implementation by people who don't have much of a technical background
2. Ease of adoption and modification by seasoned developers and hobbyist

We've also decided to use components that can be easily acquired. Making it opensource, anyone can review the code and designs, and make appropriate modifications should newer ways to perform tasks are required. It also means that if you're not a fan of the components that we used in our design, you can easily change it to a sensor you prefer.

The default components covered are the Ultrasonic Sensor (to measure distance), a DS18B20 Digital temperature sensor (to measure liquid temperature) and a DHT22 digital temperature sensor (to measure temperature and humidity).

### Raspberry Pi Pico
The Raspberry Pi Pico is the core of the system. Here's a few reasons why we went with the Raspberry Pi Pico (and Pico W):

- Dual-core processor
- 26 Pins (this ideally means you can read 26 sensors or control 26 things)
- Requires 5V DC
- Can operate in -20°C to +85°C
- Can be coded with MicroPython (basically a stripped down version of Python)

### Additional Components

Here's a list of components we used for this design:
- Ultrasonic Sensor (5V)
- DS18B20 digital temperature sensor (3.3V)
- 4.7Kohm resistor
- DHT22 digital temperature sensor (5V)
- 16x2 LCD screen (5V)
- Red LED (3.3V)
- 2.1mm Barrel jack
- 9V power adapter (2.1mm connector)
- 470 ohm resistors (x2)
- JHT connectors (4 pin connectors x4 and 3 pin connector x2)
- 3D printed case

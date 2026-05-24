# Automatic Nutrition Mixing for Hydroponics

IoT-based automated system that mixes and delivers nutrient solutions for hydroponic plants. Monitors pH, TDS (PPM), water level, and adjusts nutrient concentration automatically via peristaltic pumps.

## Features

- **Auto Nutrient Mixing** — automatically mixes Nutrisi A + B + water in correct proportions
- **TDS Monitoring** — TDS meter measures nutrient density (PPM) in real-time
- **Water Level Detection** — AC/DC water level sensor monitors tank levels
- **Flow Rate Control** — sensor flow measures nutrient delivery rate
- **IoT Dashboard** — Blynk IoT platform for remote monitoring and control
- **Plant Monitoring** — Raspberry Pi Camera tracks plant growth via daily image capture
- **RTC Scheduling** — real-time clock for timed nutrient delivery cycles
- **Protection** — relay + optocoupler for overvoltage protection

## Components

| Component | Function |
|-----------|----------|
| Arduino Mega (built-in ESP8266) | Main microcontroller + WiFi |
| Pompa Aquarium AC/DC | Mix nutrients and water |
| Water Level Sensor (AC/DC) | Monitor tank water level |
| TDS Meter | Measure nutrient density (PPM) |
| RTC Module | Real-time clock for scheduling |
| Relay Module | Overvoltage protection |
| Optocoupler 4-pin | Prevent high voltage damage to circuit |
| Pompa 12V | Deliver mixed nutrients to plants |
| Sensor Flow | Measure nutrient flow rate |
| Raspberry Pi Camera | Monitor plant growth daily |
| LED 5V | Status indicator |
| Resistor 330 Ohm | Current limiter |

## How It Works

1. TDS sensor reads current nutrient density in water tank
2. Arduino compares with target PPM for specific plant (e.g. pakcoy)
3. Peristaltic pumps activate to add Nutrisi A, Nutrisi B, or water as needed
4. Flow sensor confirms correct delivery amount
5. Water level sensor monitors tank capacity
6. All data pushed to Blynk IoT dashboard in real-time
7. Raspberry Pi Camera captures daily plant growth images
8. RTC schedules automatic mixing cycles

## Platform

- **Blynk IoT** — remote monitoring dashboard (PPM, water level, flow rate, camera feed)
- **Arduino IDE** — ESP8266/Arduino Mega programming
- **Raspberry Pi** — plant growth image capture and processing

## Test Results

- Tested with pakcoy (bok choy) cultivation at Smart Green House, Politeknik Negeri Jember
- 24-hour non-stop monitoring via Blynk IoT
- Successful auto-mixing and nutrient delivery

## Hi-Fidelity Amplifier With Active-Crossovers and Room Correction

These are the PCBs represented a two-year passive effort to create, from scratch, an entire hi-fi amplifier with build-in DSP support for active crossovers and room 
correction.

### Overview

The amplifier has the following specifications:

* Four LM3886 68W amplifier channels in two monoblocks
* Five line-level RCA analog inputs
* One phono/vinyl RCA input with built-in amplifier and RIAA correction
* Four 192kHz/24-bit digital SPDIF inputs and one TOSLINK optical
* IR remote connection, and built-in web server for configuration and web-app access
* Custom digital signal processor with active-crossovers and room correction ability based on biquad filters and parametric EQ
* Over-the-air code updates and wifi diagnostic information 

### Project Style Guide

#### Power Monitors

There are several INA260 power meters.  

1) MAIN Digital/Analog PSU monitor, address GND/SCL
2) MAIN Positive rail for channel amplifiers, address SCL/GND
3) 7V to 5V converter, address GND/GND
4) 7V to 3V converter, address GND/3V
5) Positive analog converter,  3V/GND
6) Entire 7V converter, 3V/3V

#### Temperature Sensors

1) Microprocessor board, address GND/GND
2) Digital/Analog PSU, address GND/3V#
3) Monoblocks 1, address 3V3/GND and 3V3/3V3
4) DSP, address float/GND

#### LED lights and resistors

The following voltages and LED colours should be used for consistency. In general, all LEDs are set at 2ma of current are 0603 size.

##### Digital Voltages

- 3.3V - Blue, set to ~2ma using 150R 
- 5.0V - Red, set to ~2ma using 1.3K

##### Analog Voltages

* +3.3V - Yellow, set to ~2ma using 620R
* +9.5V - Yellow, set to ~2ma using 3.6K
* -9.5V - Blue, set to ~2ma using 3.3K
* +34V - Yellow, set to ~2ma using 16K
* -34V - Blue, set to ~2ma using 16K
* 12V - Red, set to ~2ma using 4.7K
* Positive DC - Yellow, set to 2ma
* Negative DC - Blue, set to 2ma

#### SPDIF

- TODO: ADded more inputs
- TODO: Maybe add isolation transformers
- TODO: Change ground plane so SPDIF ground doesn't interfere with analog DAC ground

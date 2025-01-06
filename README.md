# kicad-duct-turbo-fan-controller
Fan controller projects for the duct turbo, terrabloom and ac infinity fans

Simple project marrying up 3 premade boards, the esp32 doit v2, a buck-boost board and a scd41 board.

Connects to the ducturbo 3.5mm to PWM control the fan speed.

Low side mosfet PWM chosen so that removal (or potentially failure) of the esp32 keeps the fan off.

Board will also work with the AC Infinity fans however there seems to be in internal 10k resistor on these fans, so changing R5 from 10K to 1K is needed to get the "off" voltage down to under 1 volt. With the following pins:

GND → GND

10V → VBUS

PWM → D+

TACH → D-

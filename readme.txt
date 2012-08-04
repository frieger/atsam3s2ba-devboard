Cortex-M3 development platform

************************
* UNTESTED, DO NOT USE *
************************

Features:
- 5x5 cm size
- Provides breakout headers to almost all pins
- Provides crystal pads
- USB socket
- On-board usb-powered voltage regulator
- User LED
- Convenient Flash erase and reset switches

Components needed
Ceramic chip capacitor, 0603, 100 nF			9x			C3, C4, C5, C6, C8, C9, C11, C12, C21
Ceramic chip capacitor, 0603, 2.2 uF			6x			C1, C7, C10, C18, C19, C20
Ceramic chip capacitor, 0805, 10 uF				1x			C2
Tantalum chip capacitor, Package C, 10 uF		1x			C17
Panasonic capacitor, 100 uF						1x			C12
Ceramic chip capacitor for crystals, 0603		4x			C13, C14, C15, C16 (value see below)
LED, 0603										2x			D1, D2 (value see below)
Resistor for LED, 0603							2x			R3, R4 (value see below)
Resistor for USB, 0603	(find out value!)		2x			R1, R2
Crystal, 16 MHz, HC49							1x			X2
Watch crystal, 32KiHz, TC26						1x			X1, when using whatch crystal, see product line
MCU, ATSAM3S2BA, TQFP-64						1x			IC1
Pin header, 2x1									4x			Jumper headers USB, GND, 3.3V
Jumpers											4x			Jumpers USB, GND, 3.3V
MCP1703-3.3	voltage regulator, SOT-223			1x			U1
Push switch, 6x6mm, through-hole				2x			Reset, Erase switch
Mini-USB-B socket								1x			J1
Headers (male/female), 1x16						2x			board edges
Headers (male/female), 1x18						1x			board edges
Headers (male/female), 1x2						1x			when not using watch crystal, see product line

Product line:
(i) When using watch crystal:
	Populate 		X1, C13, C14
	Do not populate	header near crystal
(ii) External ADC triggering/no watch crystal:
	Populate header near crystal
	Solder wires from crystal pad to header
	Do not populate X1, C13, C14

MCU and USB socket are on the bottom side. Headers can be installed on the top or bottom side. 
Board can be mounted with 2 M3 screws. No insulation required.
Low-current LEDs recommended. Output voltage 3.3V

Capacitors for crystals
Parasitic capacitance currently unknown. Find out formula to calculate capacitor value.

LED resistors

calculation result
        current
voltage 5mA     10mA    15mA    20mA
1.8V	300     150     100     75
2.0V	260     130      87     65
2.5V	160      80      53     40
3.0V	 60      30      20     15

real-world resistors (E12 series, 1%)
        current
voltage 5mA     10mA    15mA    20mA
1.8V	330     150     100     82
2.0V	270     120      82     68
2.5V	150      82      56     39
3.0V	 68      33      22     15

Not recommended to run LEDs at 20 mA from the MCU. Low-current LEDs recommended.


USB resistors
TODO: Find out value of USB resistors from Atmel datasheet
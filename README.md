# Boycorder Color
Game Boy Color-inspired Tricorder.

A mobile sensor logger, based on the Raspberry Pi Pico and fit into a Game Boy Color reproduction case.

![PCB Front Render](images/front-sc-cgb-l.png)
![PCB Back Render](images/back-sc-cgb-l.png)

## Analog Sensors
The Raspberry Pi Pico's three analog pins are currently assigned as:

- ADC0 - Wired to the position of the Status Light in the CGB form factor. It's intended that either a status LED or a photoresistor can be placed here.
- ADC1 - Wired to EXT Port pin 2. Made available either through the EXT port, or through a separate breakout in the "Cartridge Connector" area.
- ADC2 - Volume Wheel in the CGB form factor to detect values from a potentiometer.
## Buttons
The Boycorder has eight buttons, based on the same conductive silicone design as the original Game Boy.

Currently, each button is wired directly to a GPIO.
## Power Management
This design mostly depends on the internal power management of the Raspberry Pi Pico. It can accept either two AA batteries or one 14500 with a dummy battery to bridge the other battery slot.

A diode will automatically switch to the highest voltage volume source. Safe input voltage range is 1V8 to 5V5.

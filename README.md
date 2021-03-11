# Marlin for Sapphire Pro

## Meatpack

This branch has Meatpack enabled. If you want to use Octoprint with it, you have to enable the Meatpack plugin

## With 4 x TMC2209 (UART), auto off heat sink fan and optical endstop on Z axis

* Uses the most recent bugfixes and features of Marlin (branch bugfix-2.0.x) - use at your own risk
* Linear Advance is enabled but K value is set to 0 (= optional, set it via gcode M900)
* Connector for the second hotend is used as fan output for the heatsink fan on the hotend. Turns off below 50�C
* Expects an optical endstop on the Z axis (Z min endstop)
* Filament runout sensor is enabled
* Abort print when endstop is hit (optional via gcode)

A few pictures of the hardware side (UART)

https://www.thingiverse.com/thing:4344191

## Alternative

If you came here searching for a Marlin version for unmodified Sapphire Pros, prepared for UART. you may want to look at this repository: https://github.com/le3tspeak/Marlin-2.0.X-Sapphire-PRO

## Files adapted to Sapphire Pro with TMC2209 (UART)

* pins_MKS_ROBIN_NANO.h
* Configuration.h
* Configuration_adv.h

## Sapphire Pro modifications
* X Y Z steppers RX/TX go to PE5 (thermocouple) pin
* E stepper RX/TX goes to PA6 (stepper 5 STEP) pin
* Hotend heat sink fan on HE1 connector (turns off below 50�C)
* Optical endstop on Z axis
* E3D V6 hotend with sock

See the location of the pins here https://github.com/makerbase-mks/MKS-Robin-Nano/blob/master/hardware/MKS%20Robin%20Nano%20V1.2_004/MKS%20Robin%20Nano%20V1.2_004%20PIN.pdf

## License

Marlin is published under the [GPL license](/LICENSE) because we believe in open development. The GPL comes with both rights and obligations. Whether you use Marlin firmware as the driver for your open or closed-source product, you must keep Marlin open, and you must provide your compatible Marlin source code to end users upon request. The most straightforward way to comply with the Marlin license is to make a fork of Marlin on Github, perform your modifications, and direct users to your modified fork.

While we can't prevent the use of this code in products (3D printers, CNC, etc.) that are closed source or crippled by a patent, we would prefer that you choose another firmware or, better yet, make your own.


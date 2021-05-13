# Motor-driver-with-position-feedback-HAT_

The aim of the project is to design a motor driver with position feedback HAT that can be attached to the 40 GPIO pins of the Pi. The HAT will make it possible to track and control the instantaneous position of the M1N10FB11G Brushless DC Motor which has an incremental encoder attached to its shaft.

The HAT has 3 subsystems that can each be developed and tested independently, i.e. The power supply unit, motor position feed-back and status LEDs:

Power Supply Unit
	a) The PiHat will be powered by the mains through a 5mm Barrel Jack that will supply the board with +12V DC.
	b) The 12V from the Barrel Jack will then be fed into the LTC3638 buck converter which outputs a regulated 5V and can supply up to a maximum of 250mA.
	c) A custom IC chip was chosen so as to reduce the time required for the design of the regulator.

Motor Position Feedback
	a) The Motor Position Feedback Subsystem is made up of the incremental encoder, the motor driver L293D and the Pi.
	b) The incremental encoder will be connected to the shaft of the DC motor M1N10FB11G. However, it will be controlled by the board through its pins.
	c) The encoder has 6 pins that will be connected to the PiHat through screw terminals instead of header pins which may not work well in a dusty environment.
	d) The L293D was chosen due to its high-noise-immunity inputs which protect the subsystem against noise that may come from the power supply and from the inrush current it may experience when the motor turns on.

Status LEDs
	a) There are 3 status LEDs, 1 is positioned near the jack and turns on when the PiHat is connected to the mains.
	b) The 2nd and the 3rd are connected on the output pins of the motor driver. These 2 turn on and off repeatedly when the motor is running.

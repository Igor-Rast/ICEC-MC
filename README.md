# ICEC-MC
ICEC-MC Cape for BeagleBone Black

## Introduction
ICEC-MC is a project to create the plans, prototype board and software for a completly Open Source Motor Controller board in the form of a Cape that can be placed on a BeagleBone Black.
The ICEC-MC is build to fit the needs of the FirePick Delta Modular Tool system, Incorporating 4 Modular Tool headers. 
But should also be no problem to handle any other type of 3d printer or CNC machine.
 

## Project Status

Using Printipi (thanks Collin) the basic driver for moving the FirePickDelta is working. 
G1 commands are beeing performed correctly, G2 and a look ahead function are the next on the line to get fixed.
The calculations for the FirePick seems proven and i am now turning to the BBB for more pins so we can connect the neccecary for our project.
also an graphical user interface would be nice. 

+ idea  
- schematic / logic
- match pinouts
- board layout
- proto run
- debug


### Features

##### 4 endstop connection (x,y,z axis + Bed Level switch)
- configurable as opto or switch type(pull up)

##### 4 FirePick Delta EAT Modular Tool Headers ( new design +2p)
- new 18 pin header for EAT Modular Tool board to include Stepper VRef & BBB_ADC_GND 
- Old 16p EAT tool should work without problems, just dont populate the Termistor parts. ( wire differently)
 
##### 4 embedded DRV8825 stepper drivers (x,y,z,e)
- Digital Current Control (DAC088S085)
- All DRV8825 stepping modes (full step, half step, 1/4 step, 1/8 step, 1/16 step, 1/32 step).,

##### 4 steppers connection tru Modular Tool Header (one tool at a time)
- Digital Current Control (DAC088S085) (if new EAT tool used)

##### 7 BBB ADC inputs for thermistor 
- 3 on board
- 4 accessable tru Modular Tool Headers

##### 4 Servo connections 
- connect up to 4 servos or ledstrips

##### E-Stop Logic Circuit (Oh shit, Button)
- deactivate all steppers and tools with the push of a button.

##### Imbedded voltage regulators
- 12V step down --> fans , if using 24V on motors
- 5C step down --> beaglebone black and logic

##### I2C controlled standalone PWM controller (PCA9685PW)  
- 3 Enbedded Hi-Power Mosfest (AON6758) e.g. heatbed/hotend/vacuumpump
- 3 Embedded Low-Power Mosfet (NIF5002) e.g. fan/leds
- 4 PWM control of D_Out on Modular Tool Headers
- 6 PWM signals left unused (break these out?/add some status leds?)

##### 40pin Connection for Graphical Interface Expansion using cheap 4.3inch 3.2 TFT LCD modules 
- ssd1962 display driver 
- touch sensor 
- sd card reader

##### Remote on function for ATX powersupply
- turn the ATX PSU on/off using the M81/M82 (single ATX supply)

##### BBB reset button


## Developers
TODO: setup google group
If you'd like to be involved in the development of ICEC-MC, please PM me.







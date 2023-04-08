# RC MOTOR THRUST STAND v 1.0
 ![](/Images/RCMTTSPWM_4829x3529.png) 
# Project
**Warning a fast-spinning propeller can do a lot damage, very quickly!!**

**Treat this project and my code with caution!!**

**Any time there is power applied to the ESC and motor assume the propeller will start up at any time and without any warning!!**

I build and fly RC freestyle quadcopters and RC planes. I needed a way to test RC motor power characteristics, to help me choose the correct motor for a particular build. Commercial versions are available; however, these can be expensive. 
I set out to build a simple RCMTS, using kitchen scales and an angle bracket, but then I thought, maybe I could do better and learn something along the way?

My version is based on an Arduino Nano and uses a load cell HX711
amplifier circuit to measure the grams of thrust produced by a hobby RC motor and propeller combination.

I started with a digital scale tutorial.
This taught me how the load cell and code work to produce a measurement that can be viewed through Serial Monitor or on a small OLED display.
I built a breadboard version of the digital scale and calibrated the load cell.
I then built a simple PWM motor control circuit, when I understood how they both worked, I incorporated what I had 
Learnt and developed my own code.
# Components
Arduino Nano, 5KG Load Cell + HX711 Amplifier, I2C 2004 20X4 LCD Module Display, 10K Linear Potentiometer, 3 x Push Button Switches,
3 x 10 kΩ ±5% Resistors (pulldown), Turnigy Plush 30amp (Any standard PWM ESC), LED, buzzer, 330Ω resistor, Pin headers and Dupont Jumper Wires,
Aluminium bar, nuts and bolts, motor mount, motor.

My load cell is mounted on a strip of aluminium bar drilled to match the load cell and a spare Quadcopter arm drilled and fitted
to the other side of the load cell.I then clamp this into a heavy vice.


 ![](Images/RC_MOTOR_THRUST_STAND_PHOTO_2405x2250.png)
 
 # Operation
 I started with a digital scale tutorial, which uses a 5KG load cell and HK711 amplifier.
https://randomnerdtutorials.com/arduino-load-cell-hx711/

The first thing to do is calibrate the load cell with a known weight and change the calibration
Factor in the code. 
I modified the code to display thrust in grams on an IIC/I2C/TWI 2004 20X4 LCD display.
I used analogRead a 10k linear potentiometer to map the values to PWM.
The output is determined by the potentiometer setting or the PWM pre-set, sent to a 
standard PWM ESC, in turn controls an RC motor.

Three push buttons are used for Tare, Safe Start and PWM pre-set.
Tare, is used to zero the load cell in relation to any deviation.
Safe Start, I added as a safety factor, so you have to push a button before the Arduino will
Output a PWM signal to the ESC.
PWM pre-set, used to output set PWM values for timed intervals 1250us, 1500us, 1750us and 2000us, for 2 secs each. 
This gives a repeatable bench mark, when comparison testing different motors.
The buzzer and LED are used as a start-up warning.

This version can be combined with a separate RC power meter and used to test different RC motor and propeller combination outputs.

# Improvements?
Include voltage and current in the display?
DShot instead of PWM?

Coming soon... 
RCMTS v2.0 !

This uses a resistor voltage divider circuit, ACS758LCB-050B-PFF-T 50A Hall Current Sensor and a
precision LM4040 4.096V Voltage Reference Breakout.
With additional code, this allows the display of voltage and current in the range of 30V DC - 50 Amp.


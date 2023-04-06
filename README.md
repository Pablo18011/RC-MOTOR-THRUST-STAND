# RC MOTOR THRUST STAND
 ![](/Images/RC_MOTOR_THRUST_STAND_SAFE_4829x3529.png) 
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
Arduino Nano, 5KG Load Cell + HX711 Amplifier, I2C 2004 20X4 LCD Module Display, 10K Linear Potentiometer, 3 x Push Button Switches
Turnigy Plush 30amp (Any standard PWM ESC), LED, buzzer, 330Ω resistor, Pin headers and Dupont Jumper Wires,
Aluminium bar, nuts and bolts, motor mount, motor.

My load cell is mounted on a strip of aluminium bar drilled to match the load cell and a spare Quadcopter arm drilled and fitted
to the other side of the load cell.I then clamp this into a heavy vice.


 ![](Images/RC_MOTOR_THRUST_STAND_PHOTO_2405x2250.png)
 
 # Operation


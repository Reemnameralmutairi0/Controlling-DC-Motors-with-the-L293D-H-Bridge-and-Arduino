# Controlling-DC-Motors-with-the-L293D-H-Bridge-and-Arduino
# Pre requirement
* Create an account in [TINKERCAD]
* Create a new Circui
# Tools:
1. Breadboard.
2. Arduino Uno R3.
3. DC Motors.
4. Wires.
5. L293D H Bridge.
6. Battery
# What is L293D H Bridge?
A motor driver is an integrated circuit chip which is usually used to control motors in autonomous robots. Motor driver act as an interface between Arduino and the motors . The most commonly used motor driver IC’s are from the L293 series such as L293D, L293NE, etc. These ICs are designed to control 2 DC motors simultaneously. L293D consist of two H-bridge. H-bridge is the simplest circuit for controlling a low current rated motor.L293D has 16 pins.

# Steps :
### tep1: Connect Enable1&2,Enable3&4 and power1 with (5v) pin on Arduino.
### step2: Connect input1 with 13 pin, input2 with 12, input3 with 8 pin pin, input4 with 7 pin on Arduino.
### step3: Ground pins (4,5,12,13) on L293D connected to GND pin on Arduino.
### step4: Connect Output1&Output2 with DC Motor1, Output3&Output4 with DC Motor2.
 NOTE: DC Motor will rotating in clockwise direction and if you want to run DC motor in anticlockwise direction we need to some change in the code (Replace HIGH to LOW and vice versa). 
```
{
void loop()
  digitalWrite(13, HIGH);
  digitalWrite(12, LOW);
  digitalWrite(8, HIGH);
  digitalWrite(7, LOW);
  }
 ```
But, if you want it to rotate in both directions with a while in between, then you need to set a delay for number of millisecond then the direction of rotation changes to other side.


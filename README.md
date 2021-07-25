# Controlling-DC-Motors-with-the-L293D-H-Bridge-and-Arduino
# Pre requirement
* Create an account in [tinkercad](https://www.tinkercad.com/)
* Create a new Circui
# Tools:
1. Breadboard.
2. Arduino Uno R3.
3. DC Motors.
4. Wires.
5. L293D H Bridge.
6. Battery

![<img width="722" alt="126025503-9585c978-9fe4-44d1-a189-04eda20e7190" src="https://user-images.githubusercontent.com/86169417/126885653-e2a32cb5-9031-49c2-8584-6bd3707c5f98.png">]

# What is L293D H Bridge?
A motor driver is an integrated circuit chip which is usually used to control motors in autonomous robots. Motor driver act as an interface between Arduino and the motors . The most commonly used motor driver IC’s are from the L293 series such as L293D, L293NE, etc. These ICs are designed to control 2 DC motors simultaneously. L293D consist of two H-bridge. H-bridge is the simplest circuit for controlling a low current rated motor.L293D has 16 pins.

# Steps :
### tep1: Connect Enable1&2,Enable3&4 and power1 with (5v) pin on Arduino.
### step2: Connect input1 with 13 pin, input2 with 12, input3 with 8 pin pin, input4 with 7 pin on Arduino.
### step3: Ground pins (4,5,12,13) on L293D connected to GND pin on Arduino.
### step4: Connect Output1&Output2 with DC Motor1, Output3&Output4 with DC Motor2.
 NOTE: DC Motor will rotating in clockwise direction and if you want to run DC motor in anticlockwise direction we need to some change in the code (Replace HIGH to LOW and vice versa). 
```
void loop()
  digitalWrite(13, HIGH);
  digitalWrite(12, LOW);
  digitalWrite(8, HIGH);
  digitalWrite(7, LOW);
 ```
But, if you want it to rotate in both directions with a while in between, then you need to set a delay for number of millisecond then the direction of rotation changes to other side.
 ```
 // C++ code
//
void setup()
{
  pinMode(13, OUTPUT);
  pinMode(12, OUTPUT);
  pinMode(8, OUTPUT);
  pinMode(7, OUTPUT);
}

void loop()
{
  digitalWrite(13, HIGH);
  digitalWrite(12, LOW);
  digitalWrite(8, HIGH);
  digitalWrite(7, LOW);
  delay(2000); // Wait for 1000 millisecond(s)
  digitalWrite(13, LOW);
  digitalWrite(12, HIGH);
  digitalWrite(8, LOW);
  digitalWrite(7, HIGH);
  delay(2000); // Wait for 1000 millisecond(s)
 
}

 ```
# Output Sample
# Learning references:

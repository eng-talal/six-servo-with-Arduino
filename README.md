# Connecting and Programming 6 Servo Motors in a Simulation Program

This guide explains how to set up and program an electronic circuit containing 6 servo motors using a simulation program like Tinkercad.

## Materials Needed
- Simulation software (e.g., Tinkercad)
- 6 Servo motors
- Arduino board (e.g., Arduino Uno)
- Breadboard
- Jumper wires
- Power supply (if required)

## Circuit Setup

1. **Open the Simulation Software:**
   - Go to [Tinkercad](https://www.tinkercad.com/) and create a new circuit project.

2. **Add Components to the Workspace:**
   - Drag and drop an Arduino Uno board onto the workspace.
   - Add 6 servo motors to the workspace.
   - Optionally, add a breadboard to organize the connections.

3. **Connect the Servo Motors:**
   - **Signal Wires:**
     - Connect the signal wire (usually yellow or white) of each servo motor to a digital pin on the Arduino. For example:
       - Servo 1 to pin 3
       - Servo 2 to pin 5
       - Servo 3 to pin 6
       - Servo 4 to pin 9
       - Servo 5 to pin 10
       - Servo 6 to pin 11
   - **Power Wires:**
     - Connect the power wire (usually red) of each servo motor to the `5V` pin on the Arduino (or an external power supply if needed).
   - **Ground Wires:**
     - Connect the ground wire (usually black or brown) of each servo motor to the `GND` pin on the Arduino.

## Programming the Arduino

1. **Open the Code Editor:**
   - In the simulation program, open the code editor to write the Arduino sketch.

2. **Write the Code:**

   ```cpp
   #include <Servo.h>

   // Create servo objects
   Servo servo1;
   Servo servo2;
   Servo servo3;
   Servo servo4;
   Servo servo5;
   Servo servo6;

   void setup() {
       // Attach servos to their respective pins
       servo1.attach(3);
       servo2.attach(5);
       servo3.attach(6);
       servo4.attach(9);
       servo5.attach(10);
       servo6.attach(11);
   }

   void loop() {
       // Example movement: Sweep all servos from 0 to 180 degrees
       for (int pos = 0; pos <= 180; pos += 1) {
           servo1.write(pos);
           servo2.write(pos);
           servo3.write(pos);
           servo4.write(pos);
           servo5.write(pos);
           servo6.write(pos);
           delay(15); // Wait for the servo to reach the position
       }

       // Move back from 180 to 0 degrees
       for (int pos = 180; pos >= 0; pos -= 1) {
           servo1.write(pos);
           servo2.write(pos);
           servo3.write(pos);
           servo4.write(pos);
           servo5.write(pos);
           servo6.write(pos);
           delay(15); // Wait for the servo to reach the position
       }
   }

3. **Run the Simulation:**

   
- Click the "Start Simulation" button to run the circuit and see the servos move according to the code.


## Testing and Adjustments

1. **Test the Servo Movement:** 

- Observe the movement of each servo motor in the simulation. The servos should sweep back and forth between 0 and 180 degrees.

2. **Adjust as Needed:** 

- Modify the servo angles, speed, or control logic in the code to suit your specific project requirements.

Now you've successfully connected and programmed a circuit with 6 servo motors in a simulation program!

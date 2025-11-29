IR-Finger Rehabilitation Device:
The IR-Finger Rehabilitation Device is a low-cost, Arduino-based physiotherapy system designed to assist with finger mobility rehabilitation. 
Using an infrared remote, the patient or clinician can trigger precise, programmable movements of two servo-driven finger supports, enabling repeatable motor-control exercises and controlled range-of-motion training.
The system uses a 38 kHz IR receiver and a DollaTek mini remote to fully control servo rotation patterns, including direction change, incremental movements, and programmable resets.

Features:
- Fully IR-controlled finger rehabilitation mechanism
- Two SM-S2309S servo motors operating in coordinated or opposite directions
- Supports full and half-step movements (180° or 90°)
- Customisable movement sequences
- Resettable “programming state” using the OK button
- Powered by 2× 18650 Li-ion cells
- Completely open-source (C++ / Arduino IDE)

Key Hardware Componets:
- Adeept Robotics Control Board - Arduino Uno R3 compatible motor/servo controller used to drive servos and read IR signals
- Fasizi 38 kHz IR Receiver - IR demodulator used to detect NEC remote signals
- DollaTek Mini Remote - Standard NEC-protocol IR remote used to control movement
- 2× SM-S2309S Servos - Mini servo motors used for finger actuation
- 2× 18650 Lithium Cells - Power supply for the motors and controller board

Software: 
- Language: C++
- Development Environment: Arduino IDE
- Libraries: IRremote (by Armin Joachimsmeyer), Servo.h

Wiring Overview: 
IR Reciever to Adeept board
Reciever Pin    Board Pin
OUT/S            D3 (Signal pin)
VCC/ +5V         5V
GND/-            GND

Servo 1        Signal Pin- D10      Power 5V + GND
Servo 2       Signal Pin- D11      Power 5V + GND


Setting up the IR Remote: 
Follow these steps to correctly configure the IR remote:

1. Install IRremote Library
Open Arduino IDE
Go to Tools → Manage Libraries
Search for IRremote
Install the library by Armin Joachimsmeyer

2.Connect the IR Receiver
Make sure the Fasizi IR receiver’s signal pin is connected to D3, not SDA, DSCI, or servo rails incorrectly.

3. Upload code 1: Setting up IR Remote and Receiver

4. Open Serial Monitor
Set baud = 9600
Press remote buttons
Note the hexadecimal values

5. Insert the codes into main programme

6. Upload main programme

License: MIT License - free to use, modify, and distribute

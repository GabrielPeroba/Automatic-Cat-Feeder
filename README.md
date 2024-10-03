# Automatic Feeder with Fur Elise Melody Using Arduino

This Arduino project automates feeding with a servo motor and plays "Fur Elise" using a buzzer at specific times (6:00:30 AM/PM). The system is controlled by an RTC (Real-Time Clock) to ensure accurate scheduling.

## Features

- **Scheduled Feeding**: The servo motor dispenses food at 6:00:30 AM and 6:00:30 PM.
- **Musical Alert**: Plays "Fur Elise" by Beethoven before dispensing food.
- **Real-Time Clock**: Uses the RTC (PCF8563) to keep track of time accurately.
- **Buzzer**: Outputs the melody using a buzzer connected to pin 11.

## Components

- Arduino UNO (or compatible)
- Servo motor (connected to pin 9)
- Buzzer (connected to pin 11)
- RTC Module (PCF8563)
- Wires, breadboard, and power supply

## Wiring Diagram

1. **Servo Motor**:  
   - Signal wire to pin 9  
   - Power and ground to 5V and GND
2. **Buzzer**:  
   - Positive to pin 11  
   - Ground to GND
3. **RTC Module (PCF8563)**:  
   - SDA to A4  
   - SCL to A5  
   - VCC to 5V  
   - GND to GND

## Code Overview

The code initializes the RTC and monitors the current time. If the time is 6:00:30 (AM or PM), it:
1. Plays the "Fur Elise" melody.
2. Activates the servo motor to release food for 1 second.

After dispensing, the servo motor is deactivated to save power.

### Key Variables
- **`buzzer`**: Pin for the buzzer (set to 11).
- **`servoAttached`**: Boolean flag to track the servo's state.
- **`melody[]`**: Array storing the "Fur Elise" notes and durations.
- **`tempo`**: Controls the speed of the melody (default is 80 BPM).

## How to Use

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/username/automatic-feeder-arduino.git

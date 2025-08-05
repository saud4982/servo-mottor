🛠️ Servo Motor Control with Arduino
📖 Project Description
This project demonstrates how to control a servo motor using an Arduino. The servo motor is controlled by sending PWM (Pulse Width Modulation) signals, allowing it to rotate to a specific angle between 0° and 180°. This is useful in robotics, RC vehicles, and other automation applications where precise positioning is needed.

🧰 Components Used
Arduino Uno (or any compatible board)

SG90 Servo Motor (or similar)

Jumper Wires

Breadboard (optional)

Power source (via USB or battery)

🔌 Wiring Diagram
Servo Wire	Connects To Arduino
Brown / Black (GND)	GND
Red (VCC)	5V
Orange / Yellow (Signal)	Digital Pin (e.g. D9)

💻 Arduino Code Example
cpp
Copy
Edit
#include <Servo.h>

Servo myServo;

void setup() {
  myServo.attach(9); // Attach servo to pin 9
}

void loop() {
  for (int angle = 0; angle <= 180; angle++) {
    myServo.write(angle);
    delay(15);
  }

  for (int angle = 180; angle >= 0; angle--) {
    myServo.write(angle);
    delay(15);
  }
}
✅ How It Works
The Servo library makes it easy to send angle commands.

The servo smoothly sweeps from 0° to 180° and back in a loop.

You can modify the code to respond to sensors, buttons, or potentiometers for interactive control.

📦 Future Improvements
Add potentiometer to control angle manually

Control multiple servos

Integrate with Bluetooth / Wi-Fi (e.g., using HC-05 or ESP8266)

Build a robotic arm

📸 Preview (Optional)
Add images or GIFs of your setup in action

# servo-mottor

# 🚦 Arduino PWM Traffic Light Simulator

A hardware prototyping project that simulates a standard 3-way traffic light signal using an Arduino microcontroller. Instead of abrupt binary switching, this project leverages **Pulse Width Modulation (PWM)** to create smooth, realistic fading transitions between the Red, Yellow, and Green channels.

## 🧠 How It Works (The PWM Method)

Traditional digital outputs (`digitalWrite`) only allow for strict HIGH (5V) or LOW (0V) states, which makes LEDs snap on and off instantly. 

This project utilizes `analogWrite()` to manipulate the duty cycle (0-255) of the Arduino's hardware PWM pins:
* **Incandescent Simulation:** By gradually incrementing and decrementing the duty cycle, the code mimics the natural thermal inertia and realistic "fade-in/fade-out" effect of classic incandescent traffic light bulbs.
* **Perceived Brightness Balancing:** Different colored LEDs naturally emit different lumen levels at identical voltages. Using PWM allows for fine-tuned brightness scaling so that Red, Yellow, and Green appear uniformly bright to the human eye.

---

## 🛠️ Components & Hardware Requirements

* **Microcontroller:** Arduino Uno, Nano, or any board with PWM-enabled pins.
* **LEDs:** 1 x Red LED, 1 x Yellow LED, 1 x Green LED.
* **Resistors:** 3 x 220Ω current-limiting resistors.
* **Prototyping:** 1 x Breadboard and standard jumper wires.

---

## 🔌 Circuit Schematic & Wiring

Connect your components on the breadboard according to the configuration below. Make sure to connect the LEDs to pins marked with a tilde (~), as these are the dedicated PWM pins on the Arduino.

| Component | Arduino Pin | Connection Notes |
| :--- | :--- | :--- |
| **Red LED Anode (+)** | **Pin 3** (PWM) | Through 220Ω Resistor |
| **Yellow LED Anode (+)** | **Pin 5** (PWM) | Through 220Ω Resistor |
| **Green LED Anode (+)** | **Pin 6** (PWM) | Through 220Ω Resistor |
| **All LED Cathodes (-)** | **GND** | Connected to common Ground rail |

---

## 🚀 Software Setup & Deployment

1. **Install the IDE:** Ensure you have the [Arduino IDE](https://www.arduino.cc/en/software) installed.
2. **Clone the Repository:** 
```bash
   git clone [https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git](https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git)

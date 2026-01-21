
## 1. **INTRODUCTION TO OBSTACLE AVOIDER AND MOTION DETECTION CAR**

---

This project implements an Arduino-based smart car that avoids obstacles and stops immediately when motion is detected. The car uses dual ultrasonic sensors for obstacle detection and a PIR motion sensor for accident prevention. The system is designed to demonstrate basic robotics, sensor integration, and motor control using Arduino. It is intended for learning embedded systems and autonomous vehicle behavior.

---

## 2. **PROJECT STRUCTURE**

---

### **Obstacle Avoider Car**

```
Obstacle-Avoider-Car/
├── obstacle_avoider.ino
├── README.md
└── components_list.txt
```

---

## 3. **MODULES**

---

### **1. Motor Control**

This module controls the two DC motors using the L298N motor driver.
It provides basic motor functions:

* Forward
* Backward
* Turn Left
* Turn Right
* Stop

These functions are used to navigate the car based on sensor inputs.

---

### **2. Ultrasonic Sensor (HC-SR04)**

This module implements dual ultrasonic sensors for obstacle detection.

* Each sensor measures distance using trigger and echo signals.
* If an obstacle is detected within **3 inches**, the car changes direction.
* Sensor 1 checks left side, sensor 2 checks right side.

---

### **3. Motion Sensor (PIR)**

This module implements a PIR motion sensor to detect movement in front of the car.

* If motion is detected, the car stops immediately.
* It helps prevent accidents and ensures safety.

---

### **4. Obstacle Avoidance Logic**

This logic combines readings from both ultrasonic sensors:

* If obstacle detected by left sensor → turn right
* If obstacle detected by right sensor → turn left
* If no obstacle → move forward

---

### **5. Safety Control Logic**

This logic is responsible for accident prevention:

* If motion sensor output is HIGH → stop the car for 3 seconds
* Then resume operation

---

## 4. **GETTING STARTED**

---

```
git clone https://github.com/SyedaEshal26/Obstacle-Avoider-and-Motion-Detection-Accident-Proof-Car.git
cd Obstacle-Avoider-and-Motion-Detection-Accident-Proof-Car
```

---

## 5. **USAGE**

---

1. Open Arduino IDE.
2. Connect Arduino UNO with the circuit.
3. Open `rob_car.ino`.
4. Upload the code to Arduino.
5. Power ON the car.
6. Observe obstacle avoidance and motion stop behavior.

---

## 6. **CIRCUIT CONNECTIONS**

---

| Arduino Pin | Component               |
| ----------- | ----------------------- |
| 7           | Right Motor Output 1    |
| 6           | Right Motor Output 2    |
| 5           | Left Motor Output 1     |
| 4           | Left Motor Output 2     |
| 10          | Right Motor Speed (PWM) |
| 11          | Left Motor Speed (PWM)  |
| 9           | Ultrasonic 1 Trigger    |
| 8           | Ultrasonic 1 Echo       |
| 3           | Ultrasonic 2 Trigger    |
| 2           | Ultrasonic 2 Echo       |
| 12          | Motion Sensor Output    |

---

## 7. **Contributing**

---

If you would like to contribute to this project, please fork the repository and submit a pull request.

---


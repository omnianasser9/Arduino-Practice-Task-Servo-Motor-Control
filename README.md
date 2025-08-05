
# Servo Motor Control using Arduino

 ✅ Overview
This task demonstrates my understanding and hands-on practice with two Arduino examples using a servo motor:

1. **Knob Example** – controlling the servo motor using a potentiometer.
2. **Sweep Example** – sweeping the servo back and forth automatically.

---

 1. 🔁 Sweep.ino

- The servo motor is connected to pin 9.
- It moves from 0° to 180°, then back to 0°, repeating forever.
- Controlled via a `for` loop with 1° step.
- Delay of 15ms allows the servo to move smoothly.

### 🔧 Code Summary:
```cpp
for (pos = 0; pos <= 180; pos += 1) {
  myservo.write(pos);
  delay(15);
}
for (pos = 180; pos >= 0; pos -= 1) {
  myservo.write(pos);
  delay(15);
}
````

 🎯 Purpose:

To test the full motion range of the servo and ensure smooth operation.

---

 2. 🎚️ Knob.ino

* Uses a potentiometer connected to analog pin A0.
* Reads analog input (0-1023), maps it to angle (0-180).
* Servo position updates in real-time as the knob is turned.

 🔧 Code Summary:

```cpp
val = analogRead(potpin);
val = map(val, 0, 1023, 0, 180);
myservo.write(val);
```

 🎯 Purpose:

To demonstrate real-time interactive control over the servo angle using a physical input.

---

🛠️ Hardware Used:

* Arduino Uno
* SG90 Servo Motor
* Potentiometer
* Breadboard and Jumper Wires
* USB Cable

---

 📸 Screenshots

* Attached screenshots from the Arduino IDE for both Knob and Sweep examples.
* Code is fully functional and uploaded successfully.

---

👤 Prepared by:

Omnia Nasser
Arduino Practice Task — Servo Motor Control

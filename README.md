# RoboDog v1 - Robot Dog with Digital Sensing

**RoboDog v1** is a 3D-printed robot dog project designed and built by **Jinna Arunplod**.  
The project started from a simple idea: making a friendly robot dog for people who love dogs but cannot keep a real dog because of dog-fur allergies.

This robot dog combines 3D design, 3D printing, servo motors, ESP32 control, an OLED face display, and a gas/smoke sensor.

## Project Story

I have always been a dog lover. After my dog passed away, I wanted to have that feeling of companionship again. But because I am allergic to dog fur, having another real dog was not easy. So I decided to use engineering, 3D printing, electronics, and coding to build my own robot dog.

## Main Features

- 3D-printed robot dog body and parts
- ESP32-based control system
- Servo motor movement
- OLED screen for robot face expression
- MQ135 gas/smoke sensor for air quality sensing
- Basic robot dog actions:
  - Stand
  - Sit
  - Sleep
  - Give hand / high five
- Designed for maker learning, robotics practice, and STEM education

## 3D Printed Parts

The project includes these main printable parts:

| Part | Quantity |
|---|---:|
| Body + Head | 1 |
| Upper Leg / Hip Part | 4 |
| Lower Leg / Knee Part | 4 |
| Foot | 4 |
| Ear | 2 |

> Note: Please check the orientation and servo mounting direction before printing all parts.

## Hardware

| Component | Quantity | Notes |
|---|---:|---|
| ESP32 + expansion board | 1 | Main controller |
| MG90S servo motor | 10 | 8 for legs, 2 for ears |
| OLED I2C 0.96 inch | 1 | Robot face display |
| MQ135 gas/smoke sensor | 1 | Air quality / smoke sensing |
| 3D printed body parts | 1 set | Body, head, legs, feet, ears |
| Jumper wires | As needed | For connection |
| External servo power supply | 1 | Recommended for stable servo movement |

## Servo and Sensor Pin Configuration

| Function | GPIO |
|---|---:|
| Front Left Hip | 13 |
| Front Left Knee | 12 |
| Front Right Hip | 14 |
| Front Right Knee | 27 |
| Back Left Hip | 26 |
| Back Left Knee | 25 |
| Back Right Hip | 33 |
| Back Right Knee | 32 |
| Left Ear Servo | 34 |
| Right Ear Servo | 35 |
| MQ135 Gas Sensor | 4 |
| OLED I2C SDA | 21 |
| OLED I2C SCL | 22 |

> Important: GPIO 34 and GPIO 35 on many ESP32 boards are input-only pins. If the ear servos do not work, move them to PWM-capable output pins such as GPIO 16, 17, 18, or 19 and update the code.

## Software

- Arduino IDE
- ESP32 board support package
- Servo library for ESP32
- OLED display library
- AI-assisted coding was used during development to help generate and improve code ideas

## How to Build

### 1. Print the 3D Parts

Print all main parts:

- Body + head
- 4 upper leg / hip parts
- 4 lower leg / knee parts
- 4 feet
- 2 ears

Recommended print settings:

- Material: PLA
- Layer height: 0.2 mm
- Infill: 15-25%
- Supports: Use where needed, especially around overhangs and servo slots
- Wall loops: 2-3
- Print one test leg part first before printing the full set

### 2. Prepare the Servos

You need 10 MG90S servo motors.

Before assembling:

1. Connect each servo to the ESP32.
2. Run a servo-centering sketch.
3. Set each servo to the center position, usually 90 degrees.
4. Attach the servo horn only after centering.

This step is very important. If the servos are not centered, the robot may not stand correctly.

### 3. Assemble the Body

1. Place the ESP32 expansion board inside or on top of the body.
2. Install the hip servos into the body/leg mounting points.
3. Attach the upper leg parts to the hip servos.
4. Attach the lower leg parts to the knee servos.
5. Attach the feet.
6. Attach the head and ears.
7. Mount the OLED display in the front face opening.
8. Mount the MQ135 sensor where it can sense air properly.

### 4. Wire the Electronics

Connect all servos and sensors according to the pin table above.

For servo motors, do not power all servos only from the ESP32 USB port. Use a separate 5V power supply for the servos and connect the power supply ground to the ESP32 ground.

### 5. Upload the Code

1. Open Arduino IDE.
2. Install ESP32 board support.
3. Select your ESP32 board.
4. Install required libraries.
5. Open the RoboDog Arduino code.
6. Check the GPIO pin numbers.
7. Upload to the ESP32.

### 6. Test Movement

Test one movement at a time:

1. Stand
2. Sit
3. Sleep
4. Give hand / high five

If a leg moves in the wrong direction, adjust the servo angle in the code or reverse the servo orientation.

### 7. Test Air Quality Display

The MQ135 sensor is used to detect air quality / gas / smoke changes.

The OLED display can show different face expressions or messages such as:

- Good air quality
- Bad air quality

## Printing Reminder

Do not print all files immediately without checking the model and scale first.

Recommended workflow:

1. Print one upper leg and one lower leg first.
2. Test fit with the MG90S servo.
3. Check screw holes and movement clearance.
4. Print one foot and test the connection.
5. After confirming the fit, print the full set.

This avoids wasting filament if your printer tolerance is different.

## Safety Notes

- Use an external power supply for the servos.
- Do not connect servo power incorrectly.
- Check wiring before powering on.
- MQ135 readings are for educational demonstration only, not for life-safety gas detection.
- Adult supervision is recommended for young makers.

## Project Goal

The goal of RoboDog v1 is to show that a young maker can turn a personal idea into a real working robot using 3D design, electronics, coding, and creativity.

## Credits

Created by **Jinna Arunplod**  
AIT International School  
MakerWorld: `https://makerworld.com/en/@jinna.maker`

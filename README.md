                                                                DRISHTI


<img width="4160" height="2893" alt="bri smart spects" src="https://github.com/user-attachments/assets/c5d94df0-c015-4d02-9153-b8f7861c9172" />

What If a Pair of Spectacles Could Guide a Visually Impaired Person?

Imagine being a visually impaired student on a large college campus. Reaching the library, laboratory, classroom, or canteen often requires assistance from friends, staff, or family members. Navigating unfamiliar environments independently can be difficult and sometimes unsafe.

To address this challenge, we developed Smart Spectacles That Enable Safe Navigation and Emergency Assistance for Visually Impaired Users. This wearable assistive device combines GPS navigation, obstacle detection, voice guidance, and emergency location sharing to help visually impaired individuals travel safely and independently.

The Problem

Visually impaired individuals face several mobility challenges:

- Difficulty navigating unfamiliar environments.
- Dependence on others for reaching destinations.
- Risk of collisions with nearby obstacles.
- Limited access to immediate assistance during emergencies.

Traditional white canes are useful for detecting nearby objects but cannot provide destination guidance or emergency communication.

Proposed Solution

The proposed Smart Spectacles system acts as a wearable navigation companion. It provides:

- GPS-based destination guidance.
- Voice instructions for navigation.
- Obstacle detection and warning.
- Emergency SOS location sharing.
- Easy-to-use button-based destination selection.

The device is designed to improve independence, confidence, and safety for visually impaired users.

Key Features

- Real-time GPS navigation
- Voice-guided assistance
- Obstacle detection using ultrasonic sensing
- Emergency SOS alert system
- Wearable and lightweight design
- Easy destination selection

Components Used

Hardware Components:

- ESP32-WROOM-32
- ESP8266 Node MCU
- Neo-7M GPS Module
- HC-SR04 Ultrasonic Sensor
- DF Player Mini
- Speaker
- SD Card 
- Push Buttons
- SOS Button
- Rechargeable Battery
- Spectacle Frame

Software Tools:

- Arduino IDE
- Tiny GPS++
- DF Robot DF Player Mini Library
- Blynk Platform

System Architecture



The project uses two microcontrollers for efficient operation.

<img width="512" height="476" alt="flow chart" src="https://github.com/user-attachments/assets/cad67477-4088-42cd-97af-201e54a934db" />


ESP32-WROOM-32

Responsible for:

- GPS data acquisition
- Navigation calculations
- Destination selection
- Voice guidance generation
- SOS message transmission

ESP8266

Responsible for:

- Obstacle detection
- Warning generation

By distributing tasks between two controllers, the system achieves reliable and responsive performance.

Project Demonstration

https://drive.google.com/file/d/1o9CXdtoK8ZXkNWSgqVOfLhswVpKzXm1l/view?usp=drivesdk

In this demonstration, the user selects the College Canteen as the destination using the navigation button.

The Smart Spectacles obtain the current GPS location and calculate the direction toward the selected destination. The system then provides voice instructions such as:

- Go Straight
- Turn Left
- Turn Right
- Destination Reached

At the same time, the obstacle detection module continuously monitors the surroundings and alerts the user whenever an obstacle is detected.





Working Principle

Step 1 – Destination Selection

The user selects a predefined destination using push buttons.

Example destinations:

- College Canteen
- ATM
- CCF Lab
- New Block

The selected destination coordinates are stored in the system.

Step 2 – GPS Tracking

The GPS module continuously acquires the user's current location.

The ESP32 processes the latitude and longitude values and compares them with the selected destination.

Step 3 – Navigation Guidance

The navigation algorithm calculates:

- Distance to destination
- Bearing angle
- Direction of movement

Based on these calculations, voice instructions are generated through the speaker.

Step 4 – Obstacle Detection

The ESP8266 continuously reads data from the ultrasonic sensor.

If an obstacle is detected within a predefined distance, the system immediately alerts the user.

Step 5 – Emergency Assistance

If the SOS button is pressed:

- Current GPS coordinates are obtained.
- A location link is generated.
- The location is sent through the Blynk platform.
- Caregivers can quickly locate the user.

Hardware Implementation

<img width="800" height="900" alt="WhatsApp Image 2026-06-18 at 20 10 05" src="https://github.com/user-attachments/assets/6cd6a672-4624-45f6-885d-6cb9d50da8a2" />


The electronic components are integrated into a spectacle frame to create a compact wearable device.

The ultrasonic sensor is positioned to detect obstacles in front of the user, while the speaker provides clear voice guidance. Push buttons allow easy destination selection, and the SOS button provides emergency support.



 GPS Navigation and Emergency Alert Circuit Diagram
 
 
<img width="900" height="400" alt="circuit" src="https://github.com/user-attachments/assets/8546f96f-23a2-4b7a-b69a-695291d28574" />



This circuit is built around the ESP32-WROOM-32 microcontroller, which performs GPS navigation, destination selection, voice guidance, and emergency alert functions. The Neo-7M GPS module continuously provides the user's current location to the ESP32. Four push buttons are used to select predefined destinations such as the College Canteen, ATM, CCF Lab, and New Block.

A DF Player Mini module connected to a speaker plays pre-recorded voice instructions stored on a microSD card. Based on the navigation algorithm, the ESP32 generates audio guidance such as "Go Straight", "Turn Left", "Turn Right", and "Destination Reached".

An SOS push button is provided for emergency situations. When pressed, the ESP32 obtains the current GPS coordinates and sends a location alert through the Blynk IoT platform, allowing caregivers to quickly locate the user.

The ESP32 was selected for this subsystem because it provides sufficient processing power, Wi-Fi connectivity, and multiple serial interfaces required for GPS and DF Player communication.

Obstacle Detection Circuit Diagram

 <img width="900" height="400" alt="circuit diagram" src="https://github.com/user-attachments/assets/ed43f120-36eb-44d8-aae3-0648badfa7da" />



This circuit is built around the ESP8266 NodeMCU microcontroller and an HC-SR04 ultrasonic sensor. The ultrasonic sensor continuously measures the distance between the user and nearby obstacles by transmitting and receiving ultrasonic waves.

When an obstacle is detected within approximately 80 cm, the ESP8266 activates a buzzer to alert the user. This immediate warning helps prevent collisions with walls, furniture, and other objects during navigation.
A dedicated ESP8266 controller was used for obstacle detection to reduce the processing load on the ESP32 navigation system and ensure reliable real-time operation of both functions simultaneously.
The obstacle detection subsystem operates continuously and independently, providing an additional layer of safety for visually impaired users while navigating.

Testing and Results


<img width="470" height="770" alt="smart specs" src="https://github.com/user-attachments/assets/1e012eb9-2c5a-4b8d-be23-7c4325244b12" />

<img width="490" height="800" alt="WhatsApp Image 2026-06-18 at 16 14 10" src="https://github.com/user-attachments/assets/a3eb65cd-3190-456e-b331-78d2c381e693" />


The prototype was tested in a college campus environment.

Observations:

- GPS tracking worked reliably in outdoor conditions.
- Voice instructions were clear and understandable.
- Obstacle detection successfully alerted the user.
- Destination guidance functioned correctly.
- SOS location sharing worked successfully.

The system demonstrated stable performance during continuous operation.


Applications

- Navigation assistance for visually impaired students.
- Accessibility support in colleges and universities.
- Workplace navigation assistance.
- Public campus guidance systems.
- Personal safety and emergency support.

Future Enhancements

Future improvements may include:
- Voice command-based destination selection.
- AI-powered object recognition.
- Camera-assisted navigation.
- Mobile application integration.
- Dynamic route planning.
- Indoor navigation using Bluetooth beacons.

Conclusion

Smart Spectacles That Enable Safe Navigation and Emergency Assistance for Visually Impaired Users is a wearable assistive technology solution designed to improve mobility and independence. By integrating GPS navigation, obstacle detection, voice guidance, and emergency assistance, the system helps visually impaired individuals navigate educational institutions, workplaces, and public environments with greater confidence and safety.
This project demonstrates how embedded systems and IoT technologies can be used to create meaningful solutions that improve accessibility and quality of life.

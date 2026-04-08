DRISHTI – Smart Glasses for the Visually Impaired


![WhatsApp Image 2026-04-01 at 01 36 36](https://github.com/user-attachments/assets/97b16b21-c6f2-4248-a17f-9af881f56333)

DRISHTI is an intelligent smart eyewear system designed to empower visually impaired individuals by enhancing their safety, confidence, and independence in everyday navigation. It seamlessly integrates real-time obstacle detection with GPS-based directional guidance, acting as a reliable digital companion that “sees” and “guides” on behalf of the user. Built on a dual ESP32 architecture, one module continuously monitors the surroundings to detect obstacles and provide instant alerts, while the other processes location data and delivers clear voice instructions such as “Go Straight,” “Turn Left,” or “Turn Right.” This combination ensures both immediate safety and accurate navigation. As the user approaches the selected destination, the system intelligently recognizes it and announces “Destination Reached,” providing a complete navigation experience. In addition, DRISHTI includes an emergency SOS feature that can transmit the user’s live location to caregivers, adding an extra layer of security. Compact, efficient, and user-friendly, the system is designed not just as a technological solution, but as a meaningful step toward enabling independent mobility and improving the quality of life for visually impaired individuals.

KEY FEATURES

- Real-time obstacle detection
- GPS-based navigation system
- Voice guidance (Left / Right / Straight)
- Dual ESP32 architecture for better performance
- Emergency SOS alert system
- Easy destination selection using buttons
- Portable and wearable design
  
 SYSTEM ARCHITECTURE

This system uses 2 ESP32 modules:

 ESP32 – 1 (Obstacle Detection Unit)

- Connected to ultrasonic sensor
- Detects obstacles in real time
- Gives instant alerts  

 ESP32 – 2 (Navigation + Alert Unit)

- Connected to GPS module
- Calculates direction and distance
- Controls DFPlayer for voice instructions
- Sends SOS alert using Blynk


COMPONENTS USED

- 2 × ESP32 Microcontrollers
- Neo-7M GPS Module
- Ultrasonic Sensor (HC-SR04)
- DFPlayer Mini
- Speaker
- Push Button
- Buzzer / Vibration Motor
- Battery


Working Principle

1. Ultrasonic sensor detects obstacles → gives immediate alert
2. GPS module provides current location
3. User selects destination using buttons
4. System calculates direction and distance
5. Voice instructions guide the user
6. SOS button sends live location in emergency


BLOCK DIAGRAM

<img width="412" height="376" alt="image" src="https://github.com/user-attachments/assets/6e779e3a-e2b1-4b18-a79e-eead327ef08b" />





FLOW CHART



<img width="412" height="364" alt="image" src="https://github.com/user-attachments/assets/46e61e23-af3f-4c90-8fd3-8eb320727eab" />

<img width="412" height="317" alt="image" src="https://github.com/user-attachments/assets/3d7097b5-d241-4649-80ac-1772f90ceaf8" />

CIRCUIT DIAGRAM

![WhatsApp Image 2026-04-08 at 11 35 45](https://github.com/user-attachments/assets/56772472-007b-40c4-8e39-1bfaea1c7fff)
![WhatsApp Image 2026-04-08 at 11 35 44](https://github.com/user-attachments/assets/17550fb4-81ac-4149-b0dc-39db0d098231)

 
TECHNOLOGY USED

- Embedded C/C++
- ESP32 Programming
- TinyGPS++ Library
- DFPlayer Mini Library
- Blynk IoT Platform


 APPLICATION

- Assistive technology for visually impaired
- Smart wearable navigation system
- Safety device for independent mobility



 FUTURE SCOPE

- Mobile app integration
- AI camera for object detection
- Voice command input
- Real-time Google Maps integration
- Indoor navigation system


  DEMO VIDEO
  
  https://drive.google.com/file/d/1o9CXdtoK8ZXkNWSgqVOfLhswVpKzXm1l/view?usp=drivesdk



  AUTHOR

  Brijit Shite
  
  B.Tech Electronics & Communication Engineering
  
  Model engineering college


⭐ Star this repo if you like it!

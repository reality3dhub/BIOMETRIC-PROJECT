Project Overview: Biometric Attendance System

The biometric attendance system you're working on utilizes RFID tags to store fingerprint templates. These RFID tags are then used by lecturers to log their attendance. The attendance data is subsequently downloaded into the system, and the results are published to the lecturers' WhatsApp numbers using an API. The project aims to provide an efficient and secure method for tracking attendance using biometric authentication.

Components Used:

ESP32: This microcontroller serves as the main control unit for the system. It facilitates communication between various components and processes the attendance data.

Fingerprint Sensor: The fingerprint sensor captures and processes the fingerprints of lecturers. It stores the fingerprint templates securely and verifies identities during attendance logging.

RFID Module: The RFID module is responsible for reading and writing data to RFID tags. It stores the fingerprint templates on these tags, which are then used for attendance logging.

OLED Display: The OLED display provides a user-friendly interface for interacting with the system. It can display instructions, prompts, and status messages during operation.

API for WhatsApp Integration: This component enables the system to publish attendance results to lecturers' WhatsApp numbers. It communicates with the WhatsApp platform to send messages containing the attendance data.

Connections:

ESP32 <-> Fingerprint Sensor:

Connect the data pins (e.g., UART or SPI) of the fingerprint sensor to the corresponding pins on the ESP32.
Implement the necessary communication protocol (e.g., UART, SPI) between the ESP32 and the fingerprint sensor.
Utilize GPIO pins for additional control signals, such as interrupt pins for fingerprint detection events.
ESP32 <-> RFID Module:

Establish a communication interface (e.g., UART, SPI) between the ESP32 and the RFID module.
Connect the required data pins of the RFID module to the corresponding pins on the ESP32.
Implement protocols for reading and writing data to RFID tags using the RFID module.
ESP32 <-> OLED Display:

Connect the OLED display to the ESP32 using the appropriate communication protocol (e.g., I2C, SPI).
Assign GPIO pins on the ESP32 for controlling the OLED display (e.g., for turning it on/off, sending data).
ESP32 <-> API for WhatsApp Integration:

Implement network communication protocols (e.g., HTTP, MQTT) on the ESP32 for interfacing with the API.
Configure the ESP32 to send HTTP requests or messages to the API endpoint containing attendance data.
Obtain necessary authentication credentials (e.g., API keys) for accessing the WhatsApp API.
Power Supply:

Ensure all components receive a stable power supply according to their voltage and current requirements.
Use voltage regulators or power management circuits to regulate and distribute power from the main source to individual components.

Project Description: Biometric Attendance System Operation

The biometric attendance system operates in several steps to efficiently track and manage attendance using fingerprint authentication and RFID technology. Here's how the system works:

Initialization:

The system boots up, initializing the ESP32 microcontroller and all connected components, including the fingerprint sensor, RFID module, and OLED display.
Enrollment Phase:

Lecturers initiate the enrollment process by presenting their fingerprint to the fingerprint sensor.
The fingerprint sensor captures the unique characteristics of the fingerprint and generates a template.
This template is securely stored on an RFID tag using the RFID module. Each lecturer is assigned a unique RFID tag containing their fingerprint template.
Attendance Logging:

During scheduled class sessions, lecturers use their assigned RFID tags to log their attendance.
They present their RFID tags to the RFID module, which reads the fingerprint template stored on the tag.
The fingerprint sensor captures the lecturer's fingerprint and compares it with the stored template on the RFID tag for authentication.
If the authentication is successful, the system records the lecturer's attendance for that session.
Data Processing:

The ESP32 processes the attendance data, managing the timestamps, lecturer identities, and session information.
It updates the internal database or memory with the attendance records for further analysis and reporting.
Result Publication:

Once the attendance data is processed, the system publishes the results to the lecturers' WhatsApp numbers using the configured API.
This publication includes details such as the session attended, time of attendance, and any additional information required.
Lecturers receive real-time notifications on their WhatsApp accounts, allowing them to monitor attendance remotely.
User Interaction:

Throughout the process, the OLED display provides feedback and status updates to users.
It displays prompts for fingerprint enrollment, instructions for attendance logging, and confirmation messages upon successful authentication.
Users can interact with the system through the OLED display to view attendance statistics, troubleshoot issues, or perform administrative tasks.
Security Measures:

The system implements robust security measures to safeguard sensitive data, including fingerprint templates and attendance records.
Encryption protocols may be employed to secure data transmission between components and external systems, such as the WhatsApp API.
Access controls and authentication mechanisms prevent unauthorized access to the system and its functionalities.


https://youtu.be/9_nlaEOjLQ4?si=exWOIoT2Xnkmwl85

YOUTUBE LINK


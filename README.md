Smart Ceiling Fan Controller
This project aims to transform a standard ceiling fan into a smart device that can be controlled remotely using the Blynk application and a standard Infrared (IR) remote control. The project is built on the ESP8266 microcontroller platform.

Key Features
Dual Remote Control: Control the fan via the Blynk app on your smartphone or a physical IR remote.

Multi-Speed Control: Change the fan speed across three different levels (Speed 1, 2, and 3), in addition to the OFF state.

Timer Functionality: Set a timer to automatically turn off the fan after a predefined duration (60, 120, 240, or 480 minutes).

Status Monitoring: The Blynk app displays the current fan status, speed, and timer state in real time.

Secure Connection: The device connects to your Wi-Fi network and the Blynk server using specified credentials.

Required Components
Microcontroller: ESP8266 NodeMCU or a similar board.

Relay Module: A 4-channel relay module to control the fan's speed settings.

IR Receiver: An IR receiver module (e.g., VS1838B).

Jumper Wires: For connecting the components.

Blynk App: A project configured in the Blynk app with appropriate widgets (buttons, sliders, display widgets).

Wiring Diagram
Connect your components to the ESP8266 pins as defined in the code:

Component	ESP8266 Pin	Notes
Relay OFF	D1 (GPIO5)	Turns the fan completely off
Relay Speed 1	D3 (GPIO0)	For the first speed setting
Relay Speed 2	D4 (GPIO2)	For the second speed setting
Relay Speed 3	D5 (GPIO14)	For the third speed setting
IR Receiver	D2 (GPIO4)	To receive signals from the remote
Setup
Install Libraries:

Blynk: BlynkSimpleEsp8266

IR: IRremoteESP8266

You can install them from the Arduino IDE via Sketch > Include Library > Manage Libraries....

Update the Code:

Create a new project in the Blynk app to get your Auth Token.

In the code, replace the placeholder values with your own:

BLYNK_TEMPLATE_ID

BLYNK_TEMPLATE_NAME

auth[] (Blynk Auth Token)

ssid[] (Your Wi-Fi name)

pass[] (Your Wi-Fi password)

Upload the Code:

Connect your ESP8266 board to the computer.

In the Arduino IDE, select the correct board and COM port.

Click the Upload button to flash the code to your board.

Additional Notes
Ensure that the IR codes in your remote match the ones defined in the code. You might need to use an IR decoder sketch to find your remote's codes.

If the relays don't function correctly, you may need to invert the LOW and HIGH states in the digitalWrite function, depending on your specific relay module.

If you encounter any issues, feel free to open a new "Issue" in this repository.

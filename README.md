# Digital Home Guard

This project implements a smart alarm system for a two-room house. The system is designed to detect activity inside the house and react according to the security mode selected by the user.

## Features

### Operating Modes
1.  **Inactive:** The system ignores all sensors.
2.  **Home:** Monitors only the main door and windows (perimeter protection).
3.  **Away:** Monitors all sensors, including motion inside.

### System Capabilities
* **Sensors:**
    * Motion detection in each room.
    * Window opening detection in each room.
    * Main door sensor.
* **Security:** Uses a **4-digit PIN** code to change security modes.
* **Exit Delay:** A 15-second timer allows the user to leave the house after activating "Away" mode.
* **Alert:** Triggers a sound alarm when an intrusion is detected.

## How It Works
1.  **Startup:** The system starts in the **Inactive** state.
2.  **Activation:** Enter the PIN code to switch modes.
3.  **Home Mode:** The alarm triggers only if a window or the main door is opened.
4.  **Away Mode:** The alarm monitors all sensors (including motion) and triggers on any suspicious activity.
5.  **Deactivation:** To turn off the alarm, enter the PIN code and select the **Inactive** mode.

## Implementation Details
The project is developed using **Logisim**. It uses a digital circuit comprised of:

* **15-second Counter:** For the exit delay timer.
* **Register:** Stores the correct PIN code.
* **4-bit Comparator:** Validates the entered PIN against the stored code.
* **Multiplexer:** Controls the output for the display.
* **7447 Circuit:** Drivers for the Seven Segment Display (Hexadecimal numbers).

## Future Improvements
* Replace registers with **RAM memory** for storing the PIN.
* Add a **wireless connection** for remote control.
* Integrate a **mobile notification system**.

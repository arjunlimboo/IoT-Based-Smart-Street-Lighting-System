Here's a `README.md` file tailored for your project:

---

# Arduino IoT Cloud-Based Motion Detection and Light Control System

This project implements a motion detection and light control system using Arduino IoT Cloud. The system detects motion using IR sensors and adjusts LEDs based on ambient light levels. All sensor data and system status are synchronized with the Arduino IoT Cloud for monitoring and control.

## Features

- **Motion Detection**: Uses three IR sensors to detect motion in specific areas.
- **Light Control**: Activates LEDs when motion is detected and the light level is below a predefined threshold.
- **IoT Integration**: Syncs sensor data and device states with Arduino IoT Cloud for remote monitoring.
- **Debugging Information**: Outputs system status and sensor readings to the Serial Monitor.

## Components Used

- **Microcontroller**: Arduino-compatible board with IoT Cloud support.
- **Sensors**: 
  - 3 x IR motion sensors (GPIO pins: D1, D5, D6).
  - 1 x LDR (Light Dependent Resistor) for light level detection (Analog pin: A0).
- **Actuators**: 
  - 3 x LEDs (GPIO pins: D2, D7, D8).
- **Connectivity**: Wi-Fi for IoT Cloud integration.

## Code Files

1. **`thingProperties.h`**: Contains cloud-related configurations and property definitions.
2. **`main.ino`**: Main program logic, including motion detection, light level monitoring, and IoT Cloud updates.

## Setup Instructions

1. **Hardware Assembly**:
   - Connect the IR sensors, LEDs, and LDR to the appropriate GPIO pins as defined in the code.
   - Ensure a stable power source for the Arduino board.

2. **Cloud Configuration**:
   - Set up an Arduino IoT Cloud account.
   - Create a new thing and add the required properties (`lightLevel`, `motionDetected1`, `motionDetected2`, `motionDetected3`).
   - Link the thing with your device.

3. **Code Upload**:
   - Open the `.ino` file in the Arduino IDE.
   - Include the `thingProperties.h` file in the project folder.
   - Configure Wi-Fi credentials in `thingProperties.h`.
   - Compile and upload the code to the Arduino board.

4. **Testing**:
   - Monitor the Serial Monitor for debugging information.
   - Verify that the LEDs respond to motion and light level changes as expected.
   - Check IoT Cloud to confirm synchronization.

## Customization

- Modify the `lightThreshold` value in the `.ino` file to adjust sensitivity to light.
- Add additional sensors or actuators as needed, updating the code accordingly.
- Customize cloud properties to include additional functionality.

## Dependencies

- Arduino IDE with IoT Cloud support.
- Arduino IoT Cloud library (`ArduinoIoTCloud.h`).

## License

This project is open-source and can be modified and distributed under the terms of the MIT License.

---

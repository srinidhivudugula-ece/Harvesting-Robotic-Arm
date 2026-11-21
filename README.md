Project Overview
AGRI-PICK is an automated agricultural harvesting system designed to reduce manual effort in fruit harvesting and minimize the collection of unripe fruits.
The system detects the presence of a fruit using an ultrasonic sensor, analyses its colour using predefined RGB profiles representing TCS3200 colour sensor readings, 
and determines whether the fruit is ripe or unripe.Based on the classification result,a four-servo robotic arm automatically picks ripe fruits and transfers them to a 
designated collection basket.Unripe fruits are rejected without activating the harvesting mechanism.The project demonstrates the integration of embedded systems, 
sensor-based detection, colour classification, servo motor control and automated decision-making for smart agriculture.

Objectives
1.Develop an automated fruit detection system.
2.Identify fruit ripeness using RGB colour values.
3.Differentiate ripe and unripe fruits through threshold-based classification.
4.Design a four-degree-of-freedom robotic harvesting mechanism.
5.Automate fruit picking, lifting, transferring and releasing operations.
6.Reduce unnecessary harvesting of unripe fruits.
7.Demonstrate the application of robotics and embedded systems in precision agriculture.

Program Configuration
The following parameters can be modified in the Arduino program:
| Parameter | Current Value | Description |
|---|---:|---|
| MIN_DISTANCE | 5 cm | Minimum fruit detection distance |
| MAX_DISTANCE | 20 cm | Maximum fruit detection distance |
| RESET_DISTANCE | 25 cm | Distance required to rearm |
| RED_THRESHOLD | 600 | Minimum red value |
| GREEN_MIN | 200 | Minimum green value |
| GREEN_MAX | 650 | Maximum green value |
| BLUE_MAX | 450 | Maximum blue value |

Servo positions can also be calibrated according to the mechanical structure of the robotic arm.

Serial Monitor Output
The Arduino Serial Monitor operates at 9600 baud.

Example output:

```text
==========================
 AGRI-PICK ROBOTIC SYSTEM
==========================
Automatic mode activated

Distance: 12.5 cm
--------------------------
FRUIT DETECTED
Fruit profile: RIPE RED FRUIT

RED: 850
GREEN: 400
BLUE: 180

STATUS: RIPE
HARVESTING...
FRUIT COLLECTED

Waiting for next fruit...
```

For an unripe fruit, the system displays:

```text
FRUIT DETECTED
Fruit profile: UNRIPE GREEN FRUIT

RED: 250
GREEN: 800
BLUE: 350

STATUS: UNRIPE
FRUIT REJECTED

Waiting for next fruit...
```
Applications
- Smart agriculture and precision farming.
- Automated fruit harvesting.
- Selective harvesting based on fruit maturity.
- Agricultural robotics research.
- Embedded systems and automation education.
- Development of intelligent farming equipment.

##Future Improvements
The project can be extended with the following features:
1. **Physical TCS3200 Integration:** Replace predefined RGB profiles with actual colour measurements.
2. **Advanced Ripeness Detection:** Implement more accurate colour calibration and fruit-specific classification.
3. **Machine Vision:** Integrate a camera for fruit identification and position estimation.
4. **Inverse Kinematics:** Calculate robotic arm joint angles based on fruit coordinates.
5. **Multiple Fruit Recognition:** Identify different fruit varieties and apply individual ripeness thresholds.
6. **IoT Integration:** Monitor harvesting operations remotely through a mobile or web dashboard.
7. **Improved Mechanical Design:** Develop a mobile robotic platform for practical agricultural applications.

    Project Limitations
- RGB colour values are simulated using predefined profiles; physical TCS3200 sensing is not implemented yet.
- The system uses threshold-based classification rather than machine learning.
- Fruit profiles are selected sequentially from a fixed dataset.
- The robotic arm uses predefined servo positions rather than real-time coordinate-based movement.
- Fruit detection is based on distance and does not independently identify fruit shape or location.
- The current program assumes a fixed picking position and collection basket position.

**Building smarter agricultural solutions through robotics and automation! 🌱🤖**

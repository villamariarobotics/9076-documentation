# FRC Team 9076 Electrical Handbook

Welcome to the FRC Team 9076 Electrical Handbook! This guide is intended for electrical team members, mentors, and anyone interested in learning more about the electrical systems of our robot.

## Electrical Fundamentals

Before diving into the specifics of our robot's electrical system, let's review some fundamental electrical concepts:

**Voltage (V)**: Electrical potential difference between two points in a circuit, measured in volts (V). Voltage is analogous to pressure in a water pipe, it creates the force that pushes current through the circuit.
**Current (I)**: The flow of electric charge through a conductor, measured in amperes (amps, A). Current is similar to the rate of water flow through a pipe.
**Resistance (R)**: Opposition to electric current flow in a material, measured in ohms (Ω). Resistance is like the narrowness of a pipe, it hinders the flow of current.
These three quantities are interrelated by Ohm's Law: V = IR, where V is voltage, I is current, and R is resistance.

## Electrical Safety

Safety is paramount when working with electricity. Here are some key safety principles:

**Follow general safety rules** As well as these additional rules be sure to follow the general safety rules outlined in the team handbook.
**Always wear safety glasses** when working on electrical components.
**Never work on live circuits** Make sure everything is powered down before touching any electrical components (some exceptions apply).
**Use proper tools and equipment** The right tools will help you complete tasks safely and efficiently.
**Be aware of your surroundings** Keep flammable materials away from electrical components.
**Know where battery leak clean up equipment is located**
**If you're unsure about something, ask a mentor or an experienced member!**

## Our Robot's Electrical System

The electrical system of our robot is the heart and nervous system, powering everything from the motors to the sensors. Here's a general overview of the key components:

**Battery:** Provides the 12V DC power source for the entire robot.

**Power Distribution Hub (PDH):** Distributes power from the battery to different subsystems safely.

**Motor Controllers:** Regulate the speed and direction of the motors based on input from the robot controller.

**Sensors:** Gather data about the robot's environment (e.g., distance, light levels).

**Encoders:** encoders are used to gather data about the angle of rotation or number of rotations of a shaft .

**Vision system:** vision systems are used for vision processing on the robot and include a coprocessor which is usually powered one POE (Power Over Ethernet).

**Roborio:** The "brains" of the robot, process sensor data and send control signals to motors and other actuators.

## Electrical Design and Build Process

The electrical team plays a crucial role in designing, building, and testing the robot's electrical system. Here's a simplified breakdown of the process:

**Design Review:** Electrical team collaborates with other subteams to understand robot requirements and power needs.

**Schematic/diagram Creation:** Develop a schematic or  diagram that illustrates the electrical components and their connections.

**Component Selection:** Choose appropriate electrical components based on specifications and desired functionality.

**Prototyping:** Build a simplified prototype circuit off the robot to test functionality and identify any errors.

**Wiring and Assembly:** wire electrical components onto the robot  and use appropriate connection methods and assembly any components that need it (don’t forget to grease the gearboxes!).

**Testing and Debugging:** Thoroughly test the entire electrical system to ensure it functions as designed.

## Tools and Resources

The electrical team utilizes various tools and resources to complete its tasks. Here are some common examples:

**Multimeter:** Measures voltage, current, and resistance.

**Soldering Iron and Solder:** Used to create permanent electrical connections.

**Wire Strippers and Cutters:** Prepare wires for soldering and connections.

**Heat Shrink Tubing:** Provides insulation and protection for electrical connections.

**Crimpers:** used to add crimp connectors to wire

**Wago connectors** : used to make non permanent connections with wire

## Electrical components

This is a list of some of the specific electrical used on the robot and a detailed description of what they are used for

* **Roborio:** The NI-roboRIO is the main robot controller used for FRC. The roboRIO serves as the “brain” for the robot running team-generated code that commands all of the other hardware.
* **Rev Power Distribution Hub (PDH):** The REV Power Distribution Hub (PDH) is designed to distribute power from a 12VDC battery to various robot components. The PDH features 20 high-current (40A max) channels, 3 low-current (15A max), and 1 switchable low-current channel. The Power Distribution Hub features toolless latching WAGO terminals, an LED voltage display, and the ability to connect over CAN or USB-C to the REV Hardware Client for real-time telemetry.
* **Robot Signal Light (RSL):** The Robot Signal Light (RSL) is required to be either Allen-Bradley 855PB-B12ME522 or AndyMark am-3583. It is directly controlled by the roboRIO and will flash when enabled and stay solid while disabled.
* **Radio:** OpenMesh OM5P-AC wireless radio is used as the robot radio to provide wireless communication functionality to the robot. The device can be configured as an Access Point for direct connection of a laptop for use at home. It can also be configured as a bridge for use on the field. The robot radio should be powered by one of the 12V/2A outputs on the VRM and connected to the roboRIO controller over Ethernet. For more information, see Programming your Radio.
* **Rev Radio Power Module (RPM):** The REV Radio Power Module is designed to keep one of the most critical system components, the OpenMesh WiFi radio, powered in the toughest moments of the competition. The Radio Power Module eliminates the need for powering the radio through a traditional barrel power jack. Utilizing 18V Passive POE with two socketed RJ45 connectors, the Radio Power Module passes signal between the radio and roboRIO while providing power directly to the radio. After connecting the radio and roboRIO, easily add power to the Radio Power Module by wiring it to the low-current channels on the Power Distribution Hub utilizing the color coded push button WAGO terminals.
* **120A Breaker:** The 120A Main Circuit Breaker serves two roles on the robot: the main robot power switch and a protection device for downstream robot wiring and components. The 120A circuit breaker is wired to the positive terminals of the robot battery and Power Distribution boards. For more information, please see the Cooper Bussmann 18X Series Datasheet (PN: 185120F)
* **12V Battery:** The power supply for an FRC robot is a single 12V 18Ah Sealed Lead Acid (SLA) battery, capable of meeting the high current demands of an FRC robot. For more information, see the Robot Battery page.
* **Limit Switch:**
* **Rev Pneumatic Hub (PH):** The REV Pneumatic Hub is a standalone module that is capable of switching both 12V and 24V pneumatic solenoid valves. The Pneumatic Hub features 16 solenoid channels which allow for up to 16 single-acting solenoids, 8 double-acting solenoids, or a combination of the two types. The user selectable output voltage is fully regulated, allowing even 12V solenoids to stay active when the robot battery drops as low as 4.75V.
Digital and analog pressure sensor ports are built into the device, increasing the flexibility and feedback functionality of the pneumatic system. The USB-C connection on the Hub works with the REV Hardware Client, allowing users to test pneumatic systems without a need for an additional robot controller.
* **Compressor:** FRC robots often utilize compressed air systems for powering pneumatic cylinders and actuators. The pneumatic air compressor serves as the heart of this system, responsible for generating and maintaining the pressurized air needed for operation. These compressors are typically 12-volt DC units specifically designed for mobile applications like robotics. They come in various sizes and performance levels, and choosing the right one depends on the air requirements of your robot's pneumatic system.
* **Solenoids:** FRC robots that use compressed air systems rely on pneumatic air solenoids to control the flow of pressurized air. These solenoid valves act like electrically controlled switches. When a signal is sent to the solenoid, it opens or closes a passage, allowing compressed air to flow to specific pneumatic cylinders or actuators within the robot. Solenoids come in various configurations (2-way, 3-way, etc.) depending on the desired air flow control needs of your robot's mechanisms.
* **servos:** In FRC, servo motors are ideal for controlled movements with a limited range. Unlike continuous-spinning motors, servos rotate to a specific commanded position and hold it. This makes them perfect for actuating mechanisms that require precise positioning, such as opening and closing claws or tilting a camera mount. However, their lower torque output compared to standard motors means servos are best suited for tasks that don't require high force.
* **Servo Power Module:** The Servo Power Module from Rev Robotics is capable of expanding the power available to servos beyond what the roboRIO integrated power supply is capable of. The Servo Power Module provides up to 90W of 6V power across 6 channels. All control signals are passed through directly from the roboRIO.
* **Spark Max Motor Controllers:** The SPARK MAX Motor Controller is an advanced brushed and brushless DC motor controller from REV Robotics. When using CAN bus or USB control, the SPARK MAX uses input from limit switches, encoders, and other sensors, including the integrated encoder of the REV NEO Brushless Motor, to perform advanced control modes. The SPARK MAX can be controlled over PWM, CAN or USB (for configuration/testing only). For more information, see the SPARK MAX User’s Manual.
* **Spark Flex Motor controllers:** The SPARK Flex is a new smart motor controller that is compatible with the REV ION System. Its dockable form factor allows for the direct mounting onto a NEO Vortex, simplifying wiring while maintaining flexibility. Improving upon the foundation of the SPARK MAX Motor Controller, new features include 3-phase current sensing, reverse polarity protection, and an expanded Data Port with additional interfaces. When docked to an adapter, the SPARK Flex can control any existing NEO or compatible brushless/brushed DC motor.
* **NEO Brushless Motor V1.1:** The NEO Brushless Motor is the first brushless motor designed to meet the unique demands of the FRC community. NEO offers an incredible power density due to its compact size and reduced weight. As it is designed to have similar performance characteristics and matching mounting features, NEO can be a drop-in replacement for CIM-style motors. This motor is perfect for your FRC Robot, Industrial platform or Warehouse robot, Electric skateboards and more!
* **NEO 550 Brushless Motor:** The NEO 550 Brushless Motor is the newest member in the NEO family of brushless motors. Its output power and small size are specifically designed to make NEO 550 the perfect motor for intakes and other non-drivetrain robot mechanisms. Mounting holes and pilot match a standard 550 series motor, making it natively mount to many existing off-the-shelf gearboxes.
* **Neo Vortex brushless motor:** The NEO Vortex is a high-power, high-performance, and high-resolution sensored brushless motor that is compatible with the REV ION System. It features a dockable controller interface that can be mounted directly to the SPARK Flex Motor Controller or our NEO Vortex Solo Adapter allowing control from any brushless motor controller like the SPARK MAX Motor Controller. Its through-bore rotor is the heart of its unique interchangeable shaft system, facilitating easy integration with various robot mechanisms.

## Maintaining Electrical Systems

Regular maintenance is vital for optimal robot performance. Electrical team members should:

**Inspect wires and connections** for damage or wear and tear.
**Check motors/components** for wear and replace them if necessary.
**Clean sensors** to ensure accurate data collection.
**Update firmware** on controllers if needed.
**Do a full electrical check** in accordance to the electrical checklist

## Conclusion

The electrical team plays a critical role in the success of FRC Team 9076. By understanding electrical fundamentals, practicing safety, and working collaboratively, the electrical team ensures our robot has the power and control it needs to perform at its best.

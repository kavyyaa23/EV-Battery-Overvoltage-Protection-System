# EV Battery Overvoltage Protection System

## 📌 Project Overview

This project presents an embedded overvoltage protection system designed for electric vehicle (EV) battery applications.

The system continuously monitors the input battery voltage using a voltage-sensing network. An LM393 comparator evaluates the sensed voltage against a predefined safety threshold. When an overvoltage condition is detected, the switching stage is activated to disconnect the load and protect the connected circuit.

The design was developed and validated using KiCad SPICE simulation to study the circuit response under different input-voltage conditions.

## 🎯 Objectives

- Monitor EV battery voltage continuously.
- Detect voltage levels exceeding the defined safe threshold.
- Provide automatic load disconnection during an overvoltage condition.
- Use a comparator-based decision circuit for protection.
- Implement MOSFET/NMOS-based electronic switching.
- Validate the circuit operation through SPICE simulation.

## ⚙️ Main Components

| Component | Function |
|---|---|
| LM393 Comparator | Compares the sensed voltage with the reference threshold |
| Voltage Divider | Scales the input voltage to a suitable sensing level |
| NMOS / MOSFET | Controls the load switching and protection action |
| Red LED | Indicates an overvoltage/protection condition |
| Green LED | Indicates normal operating condition |
| Resistors | Voltage sensing, reference and LED current limiting |
| EV Battery Supply | Input voltage source for the protection circuit |

## 🔧 Working Principle

The system follows a simple protection sequence:

**Battery Voltage → Voltage Sensing → LM393 Comparator → MOSFET/NMOS Switching → Load Protection**

1. The battery/input voltage is continuously monitored.
2. A voltage-divider network scales the input voltage to a suitable level.
3. The LM393 comparator compares the sensed voltage with the defined reference threshold.
4. Under normal voltage conditions, the system maintains normal operation.
5. When the input voltage exceeds the safe threshold, the comparator changes its output state.
6. The MOSFET/NMOS switching stage responds to the comparator output.
7. The load is disconnected to prevent damage caused by excessive voltage.
8. The status LEDs provide a visual indication of the operating condition.

## 🔌 Circuit Design

The protection circuit consists of three primary stages:

### 1. Voltage Sensing

A resistor-based voltage divider is used to reduce the input voltage to a level suitable for the comparator input.

### 2. Comparator Stage

The LM393 comparator continuously evaluates the sensed voltage against a reference threshold.

### 3. Protection Switching Stage

The comparator output controls the MOSFET/NMOS switching stage. When an overvoltage condition occurs, the switching stage disconnects the protected load.

## 🖥️ KiCad SPICE Simulation

The circuit was designed and simulated using **KiCad SPICE**.

The simulation was used to verify the switching behavior of the protection circuit when the input voltage crosses the defined threshold.

The simulated output demonstrates the change in protection-state response between normal and overvoltage conditions.

## 📊 Expected Operation

| Condition | Comparator Response | Protection Stage | Status |
|---|---|---|---|
| Safe voltage | Normal state | Load connected | 🟢 Normal |
| Voltage above threshold | Protection state | Load disconnected | 🔴 Overvoltage |

## 🧠 Key Learning Outcomes

- Practical understanding of voltage sensing circuits.
- Comparator-based threshold detection.
- MOSFET/NMOS electronic switching.
- Battery protection concepts for EV applications.
- Circuit simulation using KiCad SPICE.
- Translating an EV safety requirement into an electronic protection circuit.
- Understanding how hardware protection circuits respond to abnormal operating conditions.

## 🚀 Applications

The concept can be adapted for:

- EV battery protection systems
- Battery management applications
- DC power protection
- Electronic load protection
- Overvoltage monitoring circuits
- Automotive and embedded power electronics

## 🔮 Future Improvements

- Integration with a microcontroller for voltage monitoring and logging.
- Addition of overcurrent and short-circuit protection.
- Temperature monitoring.
- Fault-status communication through CAN or UART.
- Integration with a complete Battery Management System (BMS).
- PCB implementation for practical EV applications.

## 🛠️ Tools & Technologies

- KiCad
- KiCad SPICE
- LM393 Comparator
- MOSFET / NMOS
- Voltage Sensing
- Embedded Electronics
- EV Power Electronics

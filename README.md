# Smart Water Tank Monitoring & Control System

## Overview

The Smart Water Tank Monitoring & Control System is a Digital Logic Design project developed for the IFT 211 (Digital Logic Design) Mid-Semester Laboratory Assessment at Miva Open University.

The system monitors the water level in a residential or industrial water tank using four water level sensors. It automatically controls the water pump, stores the current water level, detects overflow conditions, and displays the tank level on a 7-segment display.

This project was designed and simulated using **Logisim Evolution** and implements **pure digital logic** without the use of microcontrollers or programmable devices.

---

## Features

- Water level monitoring using four sensors
- 2-bit binary encoding of water level
- Automatic pump control
- Full tank detection
- Overflow detection after 3 clock cycles
- 2-bit register for storing the current water level
- 2-bit synchronous counter
- 7-segment display output
- Reset and Clock control

---

## Water Level Encoding

| Sensor | Water Level | Binary |
|---------|-------------|--------|
| S0 | Empty | 00 |
| S1 | 25% | 01 |
| S2 | 50% | 10 |
| S3 | Full | 11 |

---

## Boolean Expressions

### Encoder

```
L1 = S2 + S3
L0 = S1 + S3
```

### Full Detection

```
FULL = L1 · L0
```

### Pump Control

```
Pump = ¬FULL
```

### Alarm

```
ALARM = Q1 · Q0
```

---

## Digital Logic Components Used

- Logic Gates (AND, OR, NOT)
- Boolean Algebra
- Karnaugh Maps (K-Map)
- Encoder
- Comparator
- D Flip-Flops
- Register
- Synchronous Counter
- 7-Segment Display
- Clock
- Reset

---

## Software Used

- Logisim Evolution

---

## Project Structure

```
WaterTankSystem
│
├── Sensor Encoder
├── Comparator
├── Pump Control
├── Register
├── Overflow Counter
├── Alarm Logic
└── 7-Segment Display
```

---

## Functional Requirements

- Monitor the water level.
- Display tank level (0–3) on a 7-segment display.
- Turn the pump ON while the tank is not full.
- Turn the pump OFF when the tank becomes full.
- Store the latest valid tank level.
- Trigger an alarm if the tank remains full for three consecutive clock cycles.

---

## Simulation

To run the project:

1. Install Logisim Evolution.
2. Open the `.circ` file.
3. Toggle the sensor inputs (S0–S3).
4. Use the clock to update the register and counter.
5. Observe:
   - Pump operation
   - FULL signal
   - Alarm
   - 7-segment display

---

## Learning Outcomes

This project demonstrates the practical application of:

- Combinational Logic
- Sequential Logic
- Boolean Simplification
- Digital System Design
- Register Design
- Counter Design
- Digital Circuit Simulation

---

## Author

**Ayomide Ojo**

IFT 211 – Digital Logic Design

Miva Open University

2026

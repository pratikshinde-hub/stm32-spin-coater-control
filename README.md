# STM32 Spin Coater Control System

Embedded control and validation platform built using STM32, BLDC motor control, encoder feedback, and PID-based speed regulation for high-speed spin coating applications.

The project focuses on closed-loop motor control, hardware debugging, signal validation, and structured testing workflows for stable and repeatable high-speed operation.

---

## Project Overview

This project was developed to design and validate a closed-loop spin coater platform capable of maintaining controlled high-speed rotation using encoder feedback and PID regulation.

The system integrates STM32-based motor control, PWM signal generation, encoder RPM monitoring, and hardware validation workflows to improve rotational stability and response consistency during operation.

---

## System Architecture

The system consists of:

- STM32 microcontroller for motor control and feedback processing
- BLDC motor with motor driver interface
- Quadrature encoder for RPM feedback
- PWM-based speed control
- PID control loop for speed stabilization
- Validation and monitoring workflow using oscilloscope and signal analysis tools

---

## Hardware Components

- STM32 Development Board
- BLDC Motor
- Motor Driver Module
- Quadrature Encoder
- Oscilloscope
- Logic Analyzer
- Power Supply Unit
- Signal Conditioning Components

---

## Features

- Closed-loop PID motor speed control
- Real-time encoder feedback monitoring
- PWM-based motor actuation
- High-speed rotational stability testing
- Encoder signal validation and waveform inspection
- Hardware debugging and fault isolation
- Structured calibration and validation workflow

---

## Control System Workflow

1. Desired RPM value is provided to the STM32 controller
2. STM32 generates PWM signals for motor control
3. Encoder feedback is continuously captured through timer interfaces
4. Actual RPM is compared against target RPM
5. PID controller adjusts PWM duty cycle dynamically
6. Validation measurements are recorded during operation

---

## Debugging & Validation

### Encoder Signal Validation

Encoder output signals were inspected using oscilloscope measurements during high-speed operation.

Observed issues:
- Noise on quadrature encoder lines
- Irregular pulse edges at high RPM
- Signal instability during rapid acceleration

Resolution:
- Applied hardware filtering
- Improved grounding and signal routing
- Stabilized encoder pulse capture before STM32 timer processing

---

### PWM Timing Debugging

Waveform inspection identified PWM timing mismatches and dead-time conflicts during motor direction transitions.

Validation involved:
- Oscilloscope waveform inspection
- PWM duty-cycle verification
- Motor response analysis during speed transitions

---

### PID Tuning

PID gains were tuned iteratively using measured RPM response.

Parameters evaluated:
- Rise time
- Speed stability
- Overshoot behaviour
- Steady-state error

---

## Results

- Improved rotational stability during continuous operation
- Reduced steady-state speed error through PID tuning
- Stable encoder feedback capture at higher RPM ranges
- Improved repeatability across iterative test cycles

---

## Engineering Tools Used

- STM32CubeIDE
- Oscilloscope
- Logic Analyzer
- Proteus
- MATLAB
- Embedded C

---

## Repository Structure

```text
stm32-spin-coater-control/

│── README.md
│── firmware/
│── hardware/
│── images/
│── docs/
│── results/
```

---

## Future Improvements

- RTOS-based task scheduling
- GUI-based RPM monitoring
- Wireless telemetry integration
- Advanced motor control algorithms
- Automated calibration workflow

---

## Author

Pratik D. Shinde  
Embedded Systems & Hardware Engineering Student

GitHub: github.com/pratikshinde-hub

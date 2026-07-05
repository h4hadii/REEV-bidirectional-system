# REEV-bidirectional-system
# Bidirectional DC-DC Converter for Range-Extended EVs (REEV)

## Overview
This project provides a robust solution for energy management in Range-Extended Electric Vehicles. By implementing a high-fidelity 3kW bidirectional power stage, this system facilitates efficient energy transfer between a 72V traction battery and a 96V bus, optimized for APU cranking and regenerative power balancing.

## Engineering Challenges Solved

- **Inrush Current Management:** Eliminated destructive >400A current spikes during bus-motor coupling by implementing series-impedance soft-start logic.

- **Transient Stability:** Resolved bus voltage collapse during transition states using a Cascaded Current-Mode control architecture (Voltage-Loop + Current-Loop), replacing inefficient single-loop models.

- **Synchronous Buck-Boost Logic:** Achieved seamless bidirectional power flow using interleaving topology, allowing the battery to power the APU and vice-versa without hardware short-circuiting.

## Technical Specifications

- **Architecture:** 3-Phase Interleaved Bidirectional DC-DC.
- **Control Scheme:** Cascaded PI-Control (Outer Voltage Loop, Inner Current Loop).
- **Switching Frequency:** 40 kHz.
- **Bus Targets:** 96V (Traction), 76V (Engine Cranking/Charging).
- **Software:** MATLAB/Simulink (Discrete solver, 1µs step).

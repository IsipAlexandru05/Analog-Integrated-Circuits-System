# Analog Signal Interface System

## Overview
This project consists of an analog signal processing interface designed and simulated in **LTspice**. The system is composed of four cascaded stages designed to condition a sensor signal for an Analog-to-Digital Converter (ADC).

The project was developed for the **SCIA (Analog Integrated Circuits Systems)** course at the **Technical University of Cluj-Napoca**.

## System Architecture
[cite_start]The interface follows a 4-stage cascaded topology:
1. **Inverting Amplifier:** Provides an initial voltage gain of 9 V/V with offset adjustment.
2. **Sallen-Key Low-Pass Filter:** A 2nd order Butterworth filter with a 7 kHz cutoff frequency for noise rejection.
3. **Programmable Gain Amplifier (PGA):** Digitally controlled gain stages (8, 10, 12, 14 dB) using NMOS switches.
4. **Precision Full-Wave Rectifier:** Dual op-amp configuration for accurate signal rectification with a gain of 2 V/V.

## Technical Specifications & Performance
| Stage | Parameter | Target | Obtained (Simulated) |
| :--- | :--- | :--- | :--- |
| **Amplifier** | Gain | 9 V/V | 9 V/V (19.08 dB) |
| **Filter** | Cut-off Freq (fc) | 7.00 kHz | 7.25 kHz |
| **PGA** | Gain Range | 8 - 14 dB | 7.8 - 14.9 dB |
| **Rectifier**| Gain | 2 V/V | 2 V/V |

*The system uses high-performance **AD8065** operational amplifiers to ensure high linearity (THD < 1%) and wide bandwidth.*

## Repository Contents
* `src/`: LTspice simulation files (`.asc`).
* `docs/`: Full technical report in PDF format.
* `assets/`: Simulation waveforms (Bode plots, Transient analysis).

## Documentation
For a deep dive into calculations, component dimensioning (E12/E24 series), and error analysis, please see the full report:
👉 **[View Technical Documentation (PDF)](Documentation/SAIC_Project_IsipAlexandru.pdf)**

## Tools Used
* **Simulation:** LTspice XVII
* **Op-Amps:** Analog Devices AD8065
* **Components:** Standard E12/E24 Resistor and Capacitor series 

---
*Developed by **Isip Alexandru**, 3rd Year Student, Applied Electronics (ETTI, UTCN).*

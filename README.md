# Analog Signal Interface System

## Overview
This project consists of an analog signal processing interface designed and simulated in **LTspice**. [cite_start]The system is composed of four cascaded stages designed to condition a sensor signal for an Analog-to-Digital Converter (ADC)[cite: 44, 48].

[cite_start]The project was developed for the **SCIA (Analog Integrated Circuits Systems)** course at the **Technical University of Cluj-Napoca**.

## System Architecture
[cite_start]The interface follows a 4-stage cascaded topology[cite: 44]:
1. [cite_start]**Inverting Amplifier:** Provides an initial voltage gain of 9 V/V with offset adjustment[cite: 59, 61, 118].
2. [cite_start]**Sallen-Key Low-Pass Filter:** A 2nd order Butterworth filter with a 7 kHz cutoff frequency for noise rejection[cite: 71, 72, 75, 137].
3. [cite_start]**Programmable Gain Amplifier (PGA):** Digitally controlled gain stages (8, 10, 12, 14 dB) using NMOS switches[cite: 79, 82, 84, 166].
4. [cite_start]**Precision Full-Wave Rectifier:** Dual op-amp configuration for accurate signal rectification with a gain of 2 V/V[cite: 92, 93, 94].

## Technical Specifications & Performance
| Stage | Parameter | Target | Obtained (Simulated) |
| :--- | :--- | :--- | :--- |
| **Amplifier** | Gain | 9 V/V | [cite_start]9 V/V (19.08 dB) [cite: 354] |
| **Filter** | Cut-off Freq (fc) | 7.00 kHz | [cite_start]7.25 kHz [cite: 354] |
| **PGA** | Gain Range | 8 - 14 dB | [cite_start]7.8 - 14.9 dB [cite: 354] |
| **Rectifier**| Gain | 2 V/V | [cite_start]2 V/V [cite: 354] |

[cite_start]*The system uses high-performance **AD8065** operational amplifiers to ensure high linearity (THD < 1%) and wide bandwidth[cite: 96, 256, 290, 320].*

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
* [cite_start]**Components:** Standard E12/E24 Resistor and Capacitor series [cite: 358]

---
*Developed by **Isip Alexandru**, 3rd Year Student, Applied Electronics (ETTI, UTCN).*

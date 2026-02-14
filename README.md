# Analog Computer Project - Team Hypertronics

## 📖 Overview
[cite_start]**Team Hypertronics** developed this project for the **EN2091 - Laboratory Practice and Projects** module[cite: 1, 3]. [cite_start]It demonstrates the functionality of operational amplifier (op-amp) circuits in performing fundamental analog computations[cite: 12]. [cite_start]The system is designed to process signals within the **1 Hz to 10 kHz** frequency range[cite: 18].

[cite_start]The analog computer features a dual-channel input interface, adjustable gain control mechanisms, and a modular, stable power supply system[cite: 18].

---

## 🧮 Key Functionalities
[cite_start]The device performs the following mathematical operations using analog circuitry[cite: 12]:
* [cite_start]**Addition** [cite: 13]
* [cite_start]**Subtraction** [cite: 14]
* [cite_start]**Multiplication** [cite: 15]
* [cite_start]**Integration** [cite: 16]
* [cite_start]**Differentiation** [cite: 17]

---

## 🛠 Technical Specifications
[cite_start]The device parameters achieved during the final implementation are as follows[cite: 347]:

| Parameter | Value |
| :--- | :--- |
| **Supply Voltage** | [cite_start]$\pm 12V$ (Recommended), Max $\pm 18V$ [cite: 348] |
| **Bandwidth** | [cite_start]$1\text{ kHz} - 10\text{ kHz}$ [cite: 351] |
| **Input Current** | [cite_start]Max $10\text{ mA}$ [cite: 349] |
| **Output Voltage** | [cite_start]$\pm 12V$ [cite: 350] |
| **Maximum Noise Level** | [cite_start]$100\text{ mV}$ [cite: 352] |
| **Accuracy** | [cite_start]$\pm (1-10)\%$ [cite: 353] |
| [cite_start]**Maximum Gain** | x10 [cite: 354] |

---

## 🔌 Circuit Design & Components

### Component Selection
* **Op-Amp (UA741):** Selected for affordability and stability. [cite_start]Its bandwidth (~1 MHz) is sufficient for the project's target signal range[cite: 28, 30, 31].
* [cite_start]**Resistors (1 kΩ):** * Chosen over smaller values (e.g., $100\Omega$) to reduce current draw and power consumption[cite: 68].
    * [cite_start]Chosen over larger values (e.g., $100\text{ k}\Omega$) to prevent filtering of the input signal and bandwidth reduction[cite: 69, 70].
* **Diodes:**
    * [cite_start]**1N4148:** Used for small signals due to low junction capacitance, fast switching, and thermal stability[cite: 41, 42, 43].
    * [cite_start]**1N4007:** Used in the power supply rectifier for its high Peak Reverse Voltage ($1000V$) and 1A current handling[cite: 47, 48, 49].

### Mathematical Modules
1.  [cite_start]**Adder & Subtractor:** Implemented using standard inverting op-amp configurations with $1\text{ k}\Omega$ resistors for optimal bandwidth/power balance[cite: 67, 114].
2.  **Multiplier (Log-Antilog):**
    * [cite_start]**Issue:** Initially attempted using a Gilbert Cell, but mismatches in BJTs caused non-linear behavior[cite: 343].
    * [cite_start]**Solution:** Replaced with a Log-Antilog multiplier circuit using diodes and op-amps[cite: 344]. [cite_start]This improved linearity and generated the correct mathematical output ($V_{out} = V_1 \cdot V_2$)[cite: 345].
    * [cite_start]**Design Note:** Larger input resistors were used here to ensure small currents for a predictable log function[cite: 163, 164].
3.  [cite_start]**Power Supply:** A dedicated module providing a fixed $\pm 12V$ using **LM7812** and **LM7912** voltage regulators[cite: 35, 36].

---

## 💻 Simulation & Tools
The project utilized a combination of simulation software and hardware implementation:
* [cite_start]**Simulink:** Used for initial block-level simulation and verifying mathematical logic[cite: 175].
* [cite_start]**LTSpice:** Used for circuit-level simulation[cite: 204].
* [cite_start]**PCB Design:** Custom PCBs designed for the computing modules and power supply[cite: 326].

---

## ⚠️ Challenges & Solutions
* [cite_start]**Challenge:** Non-linearity in the multiplier circuit due to BJT mismatches in the Gilbert cell architecture[cite: 343].
* [cite_start]**Solution:** Transitioned to a **Log-Antilog multiplier** design with specific modifications, which successfully linearized the output[cite: 344, 345].

---

## 👥 Team Hypertronics
* [cite_start]**Wijesinghe U.G.S.K.D:** Simulation, Component Selection, PCB Schematic Design [cite: 367, 368]
* [cite_start]**Dilhara D.S:** PCB Design, Breadboard Implementation [cite: 370, 371]
* [cite_start]**Wijesekara W.A.G.S:** Power Supply Design, Soldering [cite: 373, 374]
* [cite_start]**Upekshani T.S:** Enclosure Design, Breadboard Implementation [cite: 376, 377, 378]

---
*University of Moratuwa - Dept. of Electronic & Telecommunication Engineering*

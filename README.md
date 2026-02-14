# Analog Computer Project - Team Hypertronics

## 📖 Overview
**Team Hypertronics** developed this project for the **EN2091 - Laboratory Practice and Projects** module. It demonstrates the functionality of operational amplifier (op-amp) circuits in performing fundamental analog computations. The system is designed to process signals within the **1 Hz to 10 kHz** frequency range.

The analog computer features a dual-channel input interface, adjustable gain control mechanisms, and a modular, stable power supply system.

---

## 🧮 Key Functionalities
The device performs the following mathematical operations using analog circuitry:
* **Addition**
* **Subtraction**
* **Multiplication**
* **Integration**
* **Differentiation**

---

## 🛠 Technical Specifications
The device parameters achieved during the final implementation are as follows:

| Parameter | Value |
| :--- | :--- |
| **Supply Voltage** | $\pm 12V$ (Recommended), Max $\pm 18V$ |
| **Bandwidth** | $1\text{ kHz} - 10\text{ kHz}$ |
| **Input Current** | Max $10\text{ mA}$ |
| **Output Voltage** | $\pm 12V$ |
| **Maximum Noise Level** | $100\text{ mV}$ |
| **Accuracy** | $\pm (1-10)\%$ |
| **Maximum Gain** | x10 |

---

## 🔌 Circuit Design & Components

### Component Selection
* **Op-Amp (UA741):** Selected for its affordability and stability. The ~1 MHz bandwidth is sufficient for the project's target signal range.
* **Resistors (1 kΩ):** * Chosen over smaller values (e.g., $100\Omega$) to reduce current draw and power consumption.
    * Chosen over larger values (e.g., $100\text{ k}\Omega$) to prevent filtering of the input signal and bandwidth reduction.
* **Diodes:**
    * **1N4148:** Used for small signals due to low junction capacitance, fast switching, and thermal stability.
    * **1N4007:** Used in the power supply rectifier for its high Peak Reverse Voltage ($1000V$) and 1A current handling.

### Mathematical Modules
1.  **Adder & Subtractor:** Implemented using standard inverting op-amp configurations with $1\text{ k}\Omega$ resistors for optimal bandwidth/power balance.
2.  **Multiplier (Log-Antilog):**
    * **Issue:** Initially attempted using a Gilbert Cell, but mismatches in BJTs caused non-linear behavior.
    * **Solution:** Replaced with a Log-Antilog multiplier circuit using diodes and op-amps. This improved linearity and generated the correct mathematical output ($V_{out} = V_1 \cdot V_2$).
    * **Design Note:** Larger input resistors were used here to ensure small currents for a predictable log function.
3.  **Power Supply:** A dedicated module providing a fixed $\pm 12V$ using **LM7812** and **LM7912** voltage regulators.

---

## 💻 Simulation & Tools
The project utilized a combination of simulation software and hardware implementation:
* **Simulink:** Used for initial block-level simulation and verifying mathematical logic.
* **LTSpice:** Used for circuit-level simulation.
* **PCB Design:** Custom PCBs designed for the computing modules and power supply.

---

## ⚠️ Challenges & Solutions
* **Challenge:** Non-linearity in the multiplier circuit due to BJT mismatches in the Gilbert cell architecture.
* **Solution:** Transitioned to a **Log-Antilog multiplier** design with specific modifications, which successfully linearized the output.

---

## 👥 Team Hypertronics
* **Wijesinghe U.G.S.K.D:** Simulation, Component Selection, PCB Schematic Design
* **Dilhara D.S:** PCB Design, Breadboard Implementation
* **Wijesekara W.A.G.S:** Power Supply Design, Soldering
* **Upekshani T.S:** Enclosure Design, Breadboard Implementation

---
*University of Moratuwa - Dept. of Electronic & Telecommunication Engineering*

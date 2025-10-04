# VSDBabySoC – Fundamentals

## 📌 Introduction
The **VSDBabySoC** project is an open-source **System on Chip (SoC)** designed with the **RVMYTH** core, a RISC-V processor.  
It integrates two main modules:  
- **Phase-Locked Loop (PLL):** Provides synchronized, stable clock signals.  
- **10-bit Digital-to-Analog Converter (DAC):** Converts digital data into analog signals.  

With these, BabySoC can interface with analog devices such as televisions or mobile phones, generating audio or video signals.  
Built using **Sky130 technology**, it serves as a learning platform for **digital–analog interfacing** and SoC experimentation.  

---

## ⚙️ What is an SoC?
A **System on Chip (SoC)** is essentially a computer fabricated on a single chip.  
It can include:
- CPU  
- Memory  
- I/O Ports  
- GPU  
- DSP  
- Power management  

### ✅ Advantages:
- Compact size  
- High performance  
- Energy efficiency  
- Cost-effectiveness  

### ⚠️ Challenges:
- Heat dissipation  
- Limited flexibility  

---

## 🧩 Types of SoCs
1. **Microcontroller-based SoCs** → Simple control and low-power devices  
2. **Microprocessor-based SoCs** → Multitasking and OS execution (e.g., smartphones)  
3. **Application-Specific SoCs** → High-performance domains (AI, graphics, networking)  

---

## 🔑 Core Components of VSDBabySoC
- **RVMYTH (RISC-V Core):**  
  - Executes instructions and processes data  
  - Uses register `r17` to store values for the DAC  

- **Phase-Locked Loop (PLL):**  
  - Generates a stable synchronized clock  
  - Prevents issues like jitter, skew, and frequency mismatch  

- **Digital-to-Analog Converter (DAC):**  
  - Converts RVMYTH’s digital outputs into analog signals  
  - Enables audio/video output for external devices  

---

## 🛠️ System Operation
1. **PLL** starts and produces a synchronized clock.  
2. **RVMYTH** executes digital instructions and refreshes register values.  
3. **DAC** converts the digital values into analog signals.  
4. Output is saved in a file called **`OUT`**, representing digital-to-analog conversion.  

---

## 📚 Supporting Theory

### 🔄 PLL
- Aligns phase and frequency of output with a reference signal  
- Components: **Phase Detector, Loop Filter, Voltage-Controlled Oscillator (VCO)**  
- On-chip PLL reduces timing errors vs. external clocks  

### 🎚️ DAC
- Converts binary values → continuous analog voltages  
- Common architectures:  
  - Weighted Resistor DAC  
  - R-2R Ladder DAC  

BabySoC implements a **10-bit R-2R Ladder DAC**, giving **1024 discrete analog levels**.  

---

## 🎯 Conclusion
The **VSDBabySoC** project demonstrates the integration of **digital computation with analog interfacing** on a compact open-source chip.  
It provides a **hands-on educational platform** to learn about:  
- RISC-V processor integration  
- PLL-based clock domains  
- DAC-driven analog conversion  

> ⚡ An excellent experimental SoC for understanding both digital and analog system design.  


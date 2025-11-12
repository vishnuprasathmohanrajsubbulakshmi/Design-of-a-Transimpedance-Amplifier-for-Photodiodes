# Design of a Transimpedance Amplifier (TIA) for Photodiodes

## Overview
This project presents the **design, simulation, and PCB layout** of a high-sensitivity Transimpedance Amplifier (TIA) optimized for use with photodiodes.  
Two photodiode models were evaluated: **BPW 21** and **SFH 229**, with a focus on DC performance, frequency response, and noise characteristics.

---

## Objective
The primary goal was to design a low-noise, high-gain transimpedance amplifier capable of accurately converting photodiode current into a measurable voltage signal, suitable for optical sensing applications.

---

## Photodiodes Used
- **BPW 21** – High responsivity photodiode
- **SFH 229** – Silicon photodiode with low capacitance

---

## Circuit Design
- **Topology:** Op-amp based TIA
- **Feedback Resistors:** Tested at **5 MΩ** and **50 MΩ**
- **Simulation Tools:** Pspice and AutoDesk Eagle
- **PCB Layout:** Designed for low parasitics and minimal noise pickup

---

## Simulation & Analysis Results

### DC Sweep
- BPW 21 and SFH 229 tested with **R1 = 5 MΩ**
- Output voltage shows expected linear relationship with photodiode current

### AC Sweep (Frequency Response)
- Frequency response measured for both photodiodes
- Performance optimized for target bandwidth

### Noise Analysis
- **Integrated Noise:**
  - BPW 21: 36.6 µV
  - SFH 229: 4.1 µV
- **Peak-to-Peak Noise (50 MΩ feedback):**
  - BPW 21: 34.54 mV (Effective Noise: 5.76 mV)
  - SFH 229: 7.36 mV (Effective Noise: 1.23 mV)

### Offset Measurements
- BPW 21: −1.228 mV
- SFH 229: −524 µV

---

## PCB Design
- Compact, low-noise PCB layout
- Photodiode mounted close to TIA input to minimize parasitic capacitance
- Ground plane used for shielding

---

## Key Learnings
- Feedback resistor value directly impacts gain and noise
- Photodiode capacitance strongly influences bandwidth
- Layout and grounding are critical for low-noise operation

---

## Future Improvements
- Use of ultra-low bias current op-amps for further noise reduction
- Temperature drift compensation
- Integration with ADC for digital readout

---

## License


---

## How to Use
1. Clone this repository:
   ```bash
   git clone https://github.com/username/TIA-photodiode.git

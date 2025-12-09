# RESOLINK DC-DC Wireless Transfer System

RESOLINK is a compact and portable **wireless DC‑to‑DC power transfer system** designed to deliver regulated power across air gaps using inductive coupling. The project demonstrates how DC input can be converted into high‑frequency AC, transmitted wirelessly through coupled coils, and then rectified and regulated back to a stable DC output suitable for powering low‑power electronic devices.

This system was designed as an Electrical Network Analysis project with the goal of creating a **portable wireless power bank** capable of operating during travel, emergencies, and power outages.

---

## 1. Overview

Traditional wired charging systems fail during disasters, line faults, or when grid availability becomes limited. RESOLINK overcomes this by enabling **contactless power transfer** using a simple LC‑oscillator‑based transmitter and a regulated receiver. Inspired by early work from Nikola Tesla and modern commercial systems like Powermat, this project delivers wireless 5V power using low‑cost, discrete components.

---

## 2. System Architecture

The system consists of two main blocks:

### **Transmitter Module**
- Powered by rechargeable DC batteries.
- Uses an **LC tank oscillator** to convert DC into alternating current.
- Drives a **copper transmission coil** to generate a magnetic field.
- The transistor repeatedly switches ON/OFF to sustain oscillations.

### **Receiver Module**
- A secondary coil picks up the alternating magnetic field.
- Output is rectified using a **full‑bridge diode rectifier**.
- A smoothing capacitor reduces voltage ripple.
- A **voltage regulator** ensures the output stays fixed at **5V DC**.

---

## 3. Working Principle

RESOLINK operates on **inductive coupling**:

1. The LC oscillator generates a high‑frequency AC signal.
2. The alternating current in the transmitter coil produces a changing magnetic field.
3. The receiver coil, placed within this field, has an EMF induced in it.
4. The induced AC is:
   - Rectified
   - Filtered
   - Regulated  
   before powering the load.

The resonance frequency is calculated using:

\[
f = rac{1}{2\pi\sqrt{LC}}
\]

With \( L = 3.71 mH \) and equivalent \( C \), the operating frequency is approximately **4 kHz**.

---

## 4. Coil Specifications

Both coils were constructed using:

- **30 SWG enameled copper wire**
- **6 cm diameter**
- **30 turns** per coil (primary and secondary)

This geometry provides suitable coupling for short‑range wireless transfer.

---

## 5. Simulation Results (Multisim)

The following voltages were obtained during simulation:

- **Primary Coil:** 10.1 VAC  
- **Secondary Coil:** 17.15 VAC  
- **Regulated Output:** 5 VDC

These results confirm correct resonance and energy transfer between coils.

---

## 6. Hardware Implementation

### **Transmitter Circuit**
- LC Tank Oscillator
- BJT transistor for switching
- Battery‑powered DC input
- Air‑core transmitting coil

### **Receiver Circuit**
- Induction coil
- Diode bridge rectifier
- Smoothing capacitor
- 5V voltage regulator (e.g., 7805)
- Output terminal for load connection

Images of the completed circuits are included in the project report.

---

## 7. Conclusion

RESOLINK successfully demonstrates a functional **DC‑to‑DC wireless power transfer system** based on inductive coupling principles. The project validates that:

- LC oscillators can convert DC to AC efficiently.
- Wireless transmission works effectively over short distances.
- Rectification and regulation restore a stable DC supply.
- The system can power 5V electronic devices as long as the receiver remains near the transmitter.

This makes RESOLINK a useful model for portable wireless charging, emergency electronics, and foundational research in contactless power delivery.



## 🎯 Project Overview

- **Objective**: Move parts on a conveyor belt and apply a press at defined locations, all managed by a PLC program with HMI monitoring.

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/3595773b-9a15-48c5-8eea-c96a4fc0ca96" width="500px" alt="Conveyor Layout">
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/bc9f4d71-e1bf-4366-9bce-8c292e810ae7" width="500px" alt="Press Mechanism">
    </td>
  </tr>
</table>

- **Key Features**:  
  - Synchronized conveyor and press motion  
  - **Photoelectric sensors** for precise part‑position detection  
  - **Limit switches** for press‑completion and start detection  
  - HMI screens for status, manual overrides, and alarms  

---

## ⚙️ PLC Logic

1. **Conveyor Control**  
   - Start/stop motor with level‑1 interlock (E‑Stop).  

2. **Press Control**  
   - Detect part arrival via **photoelectric sensor** at the press station.  
   - Trigger press solenoid valve; wait for press‑complete feedback via limit switch.  
   - Retract press and resume conveyor motion.

3. **Repeat**  

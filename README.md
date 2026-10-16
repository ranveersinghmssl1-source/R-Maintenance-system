# R-Maintenance-system# 🚨 Real-time Industry Andon System

Ek cloud-based, real-time Role-Based Maintenance Andon System jise factory floor control aur breakdown tracking ke liye design kiya gaya hai. Ye project **GitHub Pages** par hosted hai aur data sync karne ke liye **Firebase Realtime Database** ka use karta hai.

---

## 📂 Project Structure & Navigation
System me alag-alag modules ke liye separate links aur features hain:
* `index.html` — Common Central Login Screen.
* `lpc-form.html` — LPC Operator Form (C&C Machines ke liye detailed data log dropdown ke sath).
* `lpc-dash.html` — LPC Maintenance Team Dashboard (Live Table View + Sound Alert).
* `assy-form.html` — ASSY Operator Panel (CKT & Conveyor ke liye instant One-Click Buttons).
* `assy-dash.html` — ASSY Maintenance Andon Board (Visual Red/Green Status Grid + Loop Siren).
* `history.html` — Central Breakdown History Log (Purana sara analytics data tracking ke liye).

---

## 🔑 Login Access Credentials (Role IDs)
`index.html` page par login karne ke liye niche diye gaye testing credentials ka use karein (Sabhi ke liye default password **`12345`** hai):

| Target Screen / Module | User Role ID | Action / Responsibility |
| :--- | :--- | :--- |
| **LPC Operator Form** | `lpc_op` | C&C Machine select karke issue data submit karna. |
| **LPC Maintenance Dash** | `lpc_maint` | Live active breakdown table dekhna aur clear karna. |
| **ASSY Operator Form** | `assy_op` | CKT ya Conveyor stop ke liye ek click me alarm bajana. |
| **ASSY Maintenance Dash** | `assy_maint` | Red/Green blinkers aur live continuous siren alert check karna. |

---

## ⚙️ Core Technical Features
1. **Zero Refresh Sync:** Operator ke click karte hi maintenance dashboard automatic bina page reload kiye instant update ho jata hai.
2. **Asynchronous History Log:** Koi bhi alarm reset hone se pehle automatic `history_logs` database me time-stamp ke sath safe save hota hai.
3. **Sound Notifications:** Machine down hone par chhotey alerts aur continuous loop industrial siren audio activate ho jate hain.

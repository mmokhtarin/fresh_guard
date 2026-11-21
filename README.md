# FreshGuard: Intelligent Cold Storage Diagnostics (FG-ICSD)

**Group:** G01_T11 – Byte 67  
**Motto:** *"Precision Engineering, Zero Waste"*  
**Course:** TMA3084 Software Engineering Laboratory (Semester 1, 2026/2027)  
**Faculty:** Faculty of Computer Science and Information Technology (FCSIT), Universiti Malaysia Sarawak (UNIMAS)  
**Lecturer:** Ts. Nurfauza Jali  
**Lab Group 1 Demonstrator:** Mr. Md. Aminul Islam Rakib  
**Client Organisation:** FreshGuard IoT (FEAST 2.0, UNIMAS) - Cik Nur Najla Maisarah Binti Norman & Encik Naim Bin Kamaruzaman  

---

## Project Overview
**FreshGuard (FG-ICSD)** is a mobile-first Android decision-support application built with **Flutter 3.19+ / Dart 3.3+**, **Provider** state management, **Google Firebase** and the **Google Gemini 1.5 Flash API** (via a serverless backend proxy).

It replaces manual twice-daily paper temperature logbooks in regional cold storage facilities with:
- **Real-time 4-sensor telemetry streaming** (Temperature °C, Relative Humidity %RH, Ethylene $\text{C}_2\text{H}_4$ ppm, Ammonia $\text{NH}_3$ ppm).
- **Automated threshold breach alerts** (in-app visual banners + Android OS push notifications) and persistent incident audit logs.
- **Cloud Generative AI spoilage diagnostics** distinguishing mechanical compressor failure from fruit ripening ($\text{C}_2\text{H}_4$) or protein decay ($\text{NH}_3$), backed by a **`<200ms` offline heuristic fallback**.
- **Dynamic FEFO (First-Expiring-First-Out) inventory queue** that automatically recalculates remaining shelf-life when a cold room experiences a breach (`-6 hours` per `15 minutes` of critical breach).

---

## Documentation Links
- **Project Proposal (PRD v1.0):** [`/docs`](./docs)
- **Software Requirements Specification (IEEE 830 SRS):** [`/docs/G01_T11_Byte67_SRS.pdf`](./docs/G01_T11_Byte67_SRS.pdf)
- **TSPi Process Logs & Meeting Minutes:** [`/process_forms`](./process_forms)

---

## Team Roster & Module Ownership (Byte 67)

| No. | Name | Matric No. | Primary TSPi Role | Owned Functional Module |
| :-: | :--- | :-: | :--- | :--- |
| 1 | Muhammad Mokhtarin Bin Dawari | 105256 | Team Leader | `FR-01`: Identity & Facility Setup (`UI-01`, `UI-02`) |
| 2 | Nur Damia Syazana Binti Sulaili | 102833 | Development Manager | `FR-AI-01` – `FR-AI-04`: Gemini AI Diagnostics & Fallback (`UI-05`) |
| 3 | Fernandez Rugu | 104184 | Support Manager | `FR-04`: Dynamic FEFO Inventory Queue (`UI-06`) |
| 4 | Danial Naseem Iman Bin Zamizan | 103768 | Quality & Test Manager | `FR-03`: Threshold Breach Alerting & Audit Log (`UI-04`) |
| 5 | Ahmad Haziq Irfan Bin Aidi | 103121 | Planning Manager | `FR-02`: Live Telemetry Dashboard (`UI-03`) |

---

## Repository Structure

```text
fresh_guard/
├── docs/                  # Proposal PRD, IEEE 830 SRS, IEEE 1016 SDD, User Manual
├── process_forms/         # TSPi Master & Member Workbooks, Signed Meeting Minutes
├── src/                   # Flutter/Dart Mobile Application Source Code & Tests
├── .gitignore             # Excludes build artifacts & secrets (NFR-02)
└── README.md              # Project overview & setup guide

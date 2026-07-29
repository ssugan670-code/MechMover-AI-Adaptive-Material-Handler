<div align="center">

# 🤖 MechMover
### AI-Adaptive Material Handler for Smart Factories

*A compact, low-cost Autonomous Mobile Robot (AMR) built for real-world MSME factory deployment*

![Status](https://img.shields.io/badge/status-restricted--access-red)
![License](https://img.shields.io/badge/license-proprietary-lightgrey)
![Platform](https://img.shields.io/badge/platform-embedded--robotics-blue)
![Event](https://img.shields.io/badge/Pragyan%202026-1st%20Prize-gold)

</div>

---

## ⚠️ Access & Usage Notice

> **This repository is published strictly for portfolio, demonstration, and evaluation purposes.**
> No source code, firmware, wiring schematics, or design files are shared publicly.
> Reproduction, redistribution, reverse-engineering, or commercial/academic reuse of this project
> — in whole or in part — is **not permitted** without explicit written consent from the team.
> This repository exists to **showcase** the system, not to enable rebuilding it.

---

## 📌 Overview

**MechMover** is a task-specific Autonomous Mobile Robot designed to solve a real, unglamorous factory problem: moving 10–20 kg loads through narrow indoor aisles, safely, without the cost of LiDAR-based commercial AMRs.

Manual material handling is slow and unsafe. Fixed-path AGVs can't adapt to obstacles. Commercial AMRs are priced out of reach for small and medium manufacturers. MechMover was built to close that gap — with intelligent local navigation instead of expensive global mapping, and mechanical design robust enough for daily industrial use.

🏆 **1st Prize — Pragyan 2026, NIT Trichy** (Industrial Automation Theme, SAE India Guided)

<div align="center">
  <img src="assets/mechmover-prototype.jpg" alt="MechMover prototype robot" width="720">
  <p><em>MechMover physical prototype — six-wheel chassis with dual-layer sensor suite</em></p>
</div>

---

## 🎯 Problem Statement

- Manual material handling is time-consuming and unsafe
- Narrow factory aisles restrict the use of large robots
- Existing AGVs follow fixed paths and cannot adapt to obstacles
- Commercial AMRs using LiDAR are too expensive for MSMEs

**Need:** A compact, safe, and low-cost autonomous material handling solution.

---

## ✅ Objectives

- Design a low-cost autonomous mobile robot
- Navigate narrow indoor factory aisles
- Operate safely around humans and machinery
- Transport 10–20 kg payloads reliably
- Implement obstacle avoidance and basic path planning
- Prioritize stability, simplicity, and reliability over raw complexity

---

## 🧠 System Architecture

MechMover follows a **Brain–Body separation** architecture across four independently optimized layers:

| Layer | Role |
|---|---|
| **Mechanical Platform** | Six-wheel, center-drive chassis with low center of gravity |
| **Perception Layer** | Proximity and IR-based sensing for obstacle detection & docking |
| **Control & Intelligence Layer** | Raspberry Pi (decision-making) + Arduino Mega (real-time motor control) |
| **Power & Energy Layer** | Single high-capacity battery with regulated supply for electronics |

<div align="center">

| Raspberry Pi — *Brain* | Arduino Mega — *Body* |
|---|---|
| High-level decision making | Real-time motor control |
| Processes navigation logic | Reads sensors continuously |
| Selects movement direction | Executes motion commands |
| Interfaces with fleet manager | Generates precise PWM signals |

</div>

---

## ⚙️ Key Features

- 🔄 Real-time adaptive obstacle avoidance (no fixed paths)
- 💰 Low-cost sensor system — no LiDAR required
- 🧭 Memory-based path optimization (avoids previously blocked routes)
- 📦 20 kg payload capacity with uniform load distribution
- 🎯 Precision IR-based docking, accurate to **±5 cm**
- 🏭 Fleet-ready architecture — scales from single unit to multi-robot deployment
- 🔧 Compact footprint — no factory layout modification required

---

## 🛠️ Navigation Logic (High-Level)

1. Continuously sense the environment (front/left/right clearance)
2. If front distance ≥ 30 cm → move forward
3. If front distance < 30 cm → compare left/right clearance and select the safer path
4. Avoid previously blocked directions (adaptive memory)
5. On approaching a target station, IR docking markers guide precision alignment
6. Repeat continuously for autonomous, unsupervised operation

*Implementation details, sensor calibration values, and control firmware are intentionally not included in this repository.*

---

## 🏗️ Mechanical Design

- Rigid chassis suitable for continuous factory-floor operation
- Six-wheel configuration for stability under load
- Center-drive propulsion mechanism
- Flat payload deck supporting bins, trays, and small pallets
- Design optimized for safe acceleration and braking, not top speed

---

## 🌐 Fleet Manager (Software Layer)

- Centralized task allocation across multiple robots
- Multi-robot coordination and congestion avoidance
- Status monitoring and operational logging
- Designed for scalability: single robot → fleet deployment

---

## 📍 Deployment Scenarios

- Inter-workstation material transfer
- Assembly line logistics
- In-plant transport for MSMEs
- Educational and research lab environments

---

## 🎥 Demo Video

<div align="center">

*(Video demo added below)*

</div>

<!-- 
  ⬇ Paste your GitHub-hosted video embed here once uploaded.
  See "How to Add the Demo Video" section further down for the exact steps.
-->

---

## 🧾 Compliance with Problem Statement

| Requirement | Status |
|---|---|
| Compact design | ✅ |
| Low cost | ✅ |
| Indoor navigation | ✅ |
| 10–20 kg payload | ✅ |
| Basic path planning | ✅ |
| Docking capability | ✅ |
| Simplicity & reliability | ✅ |

---

## 🚀 Future Scope

- Vision-based navigation
- Advanced fleet analytics dashboard
- Autonomous charging docks
- Integration with MES/ERP systems

---

## 👥 Team — MIT Spartans

| Name | Department |
|---|---|
| Tharun A | Mechanical Engineering |
| Prabhakaran R | Mechanical Engineering |
| Sakthivel L | Mechanical Engineering |
| Yokeshwaran S | Mechanical Engineering |
| Nishanth M | Electronics & Communication Engineering |

**Department of Mechanical Engineering, Mahendra Institute of Technology, Namakkal**

---

## 📄 License

This project is released under a **restricted, all-rights-reserved license**. No part of this repository — including design concepts, documentation structure, or visual assets — may be copied, forked for reuse, or repurposed for another project or submission without prior written permission from the team.

See [`LICENSE`](LICENSE) for full terms.

---

<div align="center">

*MechMover — proving that industrial automation doesn't need expensive sensors, just intelligent design decisions.*

**Pragyan 2026 · MIT Namakkal · MechMover Team**

</div>

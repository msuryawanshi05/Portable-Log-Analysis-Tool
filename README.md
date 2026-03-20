<div align="center">

# 🛡️ Portable Log Analysis Tool
### Offline-Capable Threat Detection for Isolated & Air-Gapped Networks

[![SIH 2025](https://img.shields.io/badge/Smart%20India%20Hackathon-2025-orange?style=for-the-badge)](https://www.sih.gov.in/)
[![NTRO](https://img.shields.io/badge/Organization-NTRO-blue?style=for-the-badge)](https://ntro.gov.in/)
[![Prize](https://img.shields.io/badge/🥈%20Second%20Prize-Internal%20Hackathon-silver?style=for-the-badge)](#achievements)
[![Theme](https://img.shields.io/badge/Theme-Smart%20Automation-green?style=for-the-badge)](#)
[![Status](https://img.shields.io/badge/Status-Documentation%20Only-lightgrey?style=for-the-badge)](#disclaimer)

> **Problem Statement ID:** SIH-25235 &nbsp;|&nbsp; **Category:** Software &nbsp;|&nbsp; **Organization:** National Technical Research Organisation (NTRO)

</div>

---

## 📖 Table of Contents

- [About the Project](#about-the-project)
- [Demo](#demo)
- [Problem Statement](#problem-statement)
- [Proposed Solution](#proposed-solution)
- [Architecture](#architecture)
- [Key Features](#key-features)
- [Technology Stack](#technology-stack)
- [Repository Structure](#repository-structure)
- [Achievements](#achievements)
- [Impact & Use Cases](#impact--use-cases)
- [Team](#team)
- [Disclaimer](#disclaimer)

---

## About the Project

This project was developed as part of **Smart India Hackathon (SIH) 2025** in response to a real problem statement from the **National Technical Research Organisation (NTRO)**. It proposes a portable, offline-capable log analysis and threat detection system specifically designed for **isolated and air-gapped network environments** such as those found in government, defense, and critical infrastructure organizations.

The project was recognized and awarded **Second Prize** at the SIH Internal Hackathon held during **Engineer's Day** at **St. Vincent Pallotti College of Engineering & Technology, Nagpur**, and was subsequently shortlisted as an institutional submission to SIH 2025.

> **Note:** This repository is maintained for documentation and demonstration purposes. Source code is not included.

---

## Demo

<div align="center">

[![Watch Demo](https://img.shields.io/badge/▶%20Watch-Demo%20Video-red?style=for-the-badge&logo=youtube)](https://youtu.be/0CafFNWY91Q)

</div>

---

## Problem Statement

Modern Security Operations Centers (SOCs) rely on centralized log aggregation platforms and continuous cloud-connected monitoring to detect and respond to cyber threats. This approach, however, is fundamentally incompatible with **isolated or air-gapped networks** commonly found in sensitive government, defense, and research environments.

### Core Challenges

| Challenge | Impact |
|---|---|
| No real-time log forwarding | Delayed or missed threat detection |
| No cloud/centralized SOC access | Manual, error-prone analysis workflows |
| Limited forensic visibility | Incomplete incident reconstruction |
| Absence of behavioral baselines | Inability to detect anomalous activity |

These gaps leave critical infrastructure with severely limited defensive capabilities, making them vulnerable to advanced persistent threats (APTs) and insider attacks that could go undetected for extended periods.

---

## Proposed Solution

A **self-contained, offline-first Portable Log Analysis Tool** that brings full SOC-grade log monitoring and threat detection capabilities to isolated environments — without requiring any external network connectivity.

### Core Concept

```
Collect → Normalize → Store → Detect → Alert → Report
```

The system is designed to be deployed on a **portable device (USB / standalone system)** and operate entirely within an air-gapped environment, providing real-time threat detection and forensic reporting locally.

---

## Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                        LOG SOURCES                          │
│         Windows Event Logs │ Syslog │ App Logs │ USB Media  │
└──────────────────────────┬──────────────────────────────────┘
                           │
                           ▼
              ┌────────────────────────┐
              │   Local Log Collection  │
              └────────────┬───────────┘
                           │
                           ▼
              ┌────────────────────────┐
              │  Parsing & Normalization│
              │  (Common Log Schema)    │
              └────────────┬───────────┘
                           │
                           ▼
              ┌────────────────────────┐
              │   Local Secure Storage  │
              │       (SQLite DB)       │
              └────────────┬───────────┘
                           │
                           ▼
              ┌────────────────────────┐
              │    Detection Engine     │
              │  Rule-based │ Anomaly   │
              └────────────┬───────────┘
                           │
                           ▼
              ┌────────────────────────┐
              │  Correlation & Alerting │
              └────────────┬───────────┘
                           │
                           ▼
              ┌────────────────────────┐
              │  Offline Dashboard &    │
              │   Forensic Reports      │
              └────────────────────────┘
```

---

## Key Features

- **🔌 Offline-First Design** — Fully functional with zero internet or network dependency
- **📦 Portable Deployment** — Runs from USB or standalone systems; no complex installation
- **📥 Multi-Source Log Ingestion** — Supports Windows Event Logs, Syslog, application logs, and USB media
- **🔄 Log Normalization** — Unified common schema for cross-source correlation
- **🔍 Rule-Based Detection** — Predefined threat signatures and detection rules
- **📊 Anomaly-Based Analysis** — Statistical behavioral analysis to flag deviations from baselines
- **💡 Explainable Alerts** — Human-readable alert descriptions with supporting evidence
- **📝 Forensic Report Generation** — Tamper-evident offline reports exported as PDF or JSON
- **🖥️ Local Web Dashboard** — Intuitive browser-based interface, no external dependencies

---

## Technology Stack

> This stack was proposed as part of the SIH conceptual design submission.

| Component | Technology |
|---|---|
| **Language** | Python |
| **Log Sources** | Syslog, Windows Event Logs, Application Logs |
| **Parsing** | Regex / Template-based parsing |
| **Storage** | SQLite (embedded, portable) |
| **Detection Engine** | Rule-based + Statistical Anomaly Detection |
| **User Interface** | Local web-based dashboard |
| **Reporting** | Offline export — PDF / JSON |

---

## Repository Structure

```
portable-log-analysis-tool/
│
├── README.md                    # Project documentation
│
├── ppt/
│   └── SIH_presentation.pdf     # Full SIH slide deck
│
└── poster/
    └── project_poster.pdf       # SIH evaluation poster
```

> 🎥 Demo video is hosted on YouTube → [Watch here](https://youtu.be/0CafFNWY91Q)

---

## Achievements

<div align="center">

| Award | Event | Organizer |
|---|---|---|
| 🥈 **Second Prize** | SIH Internal Hackathon | St. Vincent Pallotti College of Engineering & Technology, Nagpur |
| 🎉 **Featured Project** | Engineer's Day Celebration | SVPCET, Nagpur |
| 📋 **Institutional Shortlist** | SIH 2025 Submission | Smart India Hackathon |

</div>

The project was recognized for its **practical relevance**, **security-first design**, and **applicability to real-world isolated network environments** faced by government and defense organizations.

---

## Impact & Use Cases

- 🏛️ **Government Networks** — Monitoring isolated ministry and administrative infrastructure
- 🔒 **Defense & Intelligence** — Cybersecurity operations in classified, air-gapped environments
- 🏕️ **Field Deployments** — Temporary or forward-deployed secure operational setups
- 🔬 **Forensic Analysis** — Post-incident investigation without data exfiltration risk
- 🏭 **Critical Infrastructure** — Power grids, water systems, and industrial control networks

### SIH Alignment

| Criteria | Status |
|---|---|
| Addresses real NTRO problem statement | ✅ |
| Focus on national cybersecurity needs | ✅ |
| Practical and deployable concept | ✅ |
| Emphasis on security, isolation, and resilience | ✅ |
| Clear architecture and working demonstration | ✅ |

---

## Team

> Developed by students of **St. Vincent Pallotti College of Engineering & Technology, Nagpur**
> as part of the Smart India Hackathon 2025 internal selection process.

---

## Disclaimer

This repository is intended **solely for academic documentation and demonstration** of the SIH 2025 project concept.

- 🚫 Source code is **not included** in this repository
- 🚫 This does **not** represent a production-ready or deployed system
- ✅ All materials (demo video on YouTube, poster, presentation) are for evaluation and educational reference only

---

<div align="center">

**Smart India Hackathon 2025** &nbsp;·&nbsp; **Problem ID: SIH-25235** &nbsp;·&nbsp; **NTRO**

*Building resilient cybersecurity for isolated networks*

</div>

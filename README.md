
🛡️ Portable Log Analysis Tool for Isolated Networks

Smart India Hackathon (SIH) 2025
Problem Statement ID: 25235
Organization: National Technical Research Organisation (NTRO)
Theme: Smart Automation
Category: Software



📌 Project Status

✅ Smart India Hackathon – Completed
📄 This repository is maintained for documentation and demonstration purposes only.
💻 Source code is not included in this repository.



🏆 Achievements

🥈 Second Prize – SIH Internal Hackathon

🎉 Awarded during Engineer’s Day Celebration

🏫 Organized at St. Vincent Pallotti College of Engineering & Technology, Nagpur


This project was recognized for its practical relevance, security focus, and applicability to isolated network environments, and was shortlisted as an institutional SIH submission.



🧠 Problem Overview

Modern Security Operations Centers (SOCs) depend on centralized log aggregation and continuous monitoring to detect cyber threats.
However, isolated or air-gapped networks—commonly found in government, defense, and sensitive environments—cannot rely on centralized or cloud-based SOC infrastructure.

This creates critical challenges:

No real-time log forwarding

Delayed threat detection

Manual and error-prone log analysis

Limited forensic visibility




💡 Proposed Solution (SIH Submission)

The project proposes a Portable Log Analysis Tool designed to operate in isolated network environments.

Key Idea

A self-contained, offline-capable system that:

Collects logs locally

Parses and normalizes them

Performs threat detection

Generates secure reports

Operates without internet connectivity




🧩 Conceptual Architecture

Log Sources
(Windows / Linux / Applications / USB Media)
        ↓
Local Log Collection
        ↓
Parsing & Normalization
        ↓
Local Secure Storage
        ↓
Detection Engine
(Rule-based + Anomaly-based)
        ↓
Correlation & Alerting
        ↓
Offline Dashboard & Reports




⚙️ Key Features (Conceptual)

Offline-first design

Portable deployment (USB / standalone system)

Multi-source log ingestion

Common log schema normalization

Rule-based threat detection

Anomaly-based behavioral analysis

Explainable alerts

Secure forensic report generation

Designed for isolated SOC environments




🛠️ Proposed Technology Stack (Design Level)

> Mentioned as part of SIH conceptual design



Programming Language: Python

Log Sources: Syslog, Windows Event Logs, Application Logs

Parsing: Regex / template-based parsing

Storage: Embedded database (SQLite)

Detection: Rule-based + statistical anomaly detection

UI: Local web-based dashboard

Reporting: Offline export (PDF / JSON)




🎥 Demonstration

This repository includes:

📹 Demo Video showcasing the working concept and system flow

📄 Project Poster used during SIH internal evaluation


These artifacts were presented during:

SIH Internal Hackathon

Engineer’s Day Project Showcase




📁 Repository Contents

.
├── README.md
├── demo/
│   └── demo_video.mp4
├── poster/
│   └── project_poster.pdf
└── ppt/
    └── SIH_presentation.pdf




🎯 Impact & Use Cases

Monitoring isolated government networks

Cybersecurity operations in air-gapped environments

Field-deployed or temporary secure setups

Offline forensic analysis

Strengthening SOC visibility without data exfiltration




🏆 Smart India Hackathon Alignment

✔ Addresses a real NTRO problem statement

✔ Focus on national cybersecurity needs

✔ Practical and deployable concept

✔ Emphasis on security, isolation, and resilience

✔ Clear architecture and demonstration




📜 Disclaimer

This repository is intended only for academic documentation and demonstration of the SIH project idea.
It does not represent a production-ready or deployed system.






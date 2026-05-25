# ◈ SENTRI // AI Security Threat Monitoring Agent

<div align="center">
  <img src="https://img.shields.io/badge/Hackathon_Track-07:_AI_Security_Agent-FF2D55?style=for-the-badge&logo=target&logoColor=white" alt="Hackathon Track 07" />
  <img src="https://img.shields.io/badge/Dependencies-Zero-10B981?style=for-the-badge" alt="Zero Dependencies" />
  <img src="https://img.shields.io/badge/License-MIT-00D4FF?style=for-the-badge" alt="MIT License" />
</div>

<br />

> **"The analyst that never sleeps."**
>
> SENTRI is a production-grade, single-file cybersecurity operations dashboard built for **Hackathon Track 07 (AI Security Threat Monitoring Agent)**. It addresses the critical challenge of SOC analyst alert fatigue by consolidating raw event logs, rendering interactive threat relationship graphs, and utilizing a simulated AI agent to generate human-readable breach summaries and containment recommendations in real-time.

---

## 📌 Table of Contents
* [Key Features](#-key-features)
* [Visual Identity & Design System](#-visual-identity--design-system)
* [Core Architecture](#-core-architecture)
* [Simulated Threat Narrative (INC-2847)](#-simulated-threat-narrative-inc-2847)
* [Getting Started](#-getting-started)
* [Verification & Quality Checklist](#-verification--quality-checklist)

---

## ⚡ Key Features

* **AI Threat Summary Engine**: Dynamically streams real-time, 3-sentence plain-English explanations of complex multi-stage attacks using an interactive typewriter-style console overlay.
* **Interactive Attack Chain Visualizer**: Built with **D3.js**, this physics-directed graph maps relationships between threat nodes (compromised assets, exfiltration servers, and target databases). Supports dragging, mousewheel zooming, canvas panning, and a dedicated fullscreen modal expansion view.
* **Geographic Threat Origin Tracking**: An inline stylized SVG world map depicting international attack paths (e.g., Moscow, Amsterdam) targeting internal infrastructure with pulsing ring animations.
* **Active Containment Workflows**: Integrated one-click response controls (`⚡ ISOLATE HOST` and `🔒 REVOKE TOKENS`) that trigger custom security confirmation overlay modals.
* **Incident History TIMELINE**: A vertical timeline showing chronological context and related sub-events, allowing analysts to drill down by clicking individual timeline nodes.
* **Structured Report Export**: A local data compiler that constructs and downloads a formatted `.txt` report file containing the selected threat description, intelligence statistics, and AI recommendations.

---

## 🎨 Visual Identity & Design System

The visual layout represents a high-fidelity cyberpunk war room aesthetic built using premium design tokens:

```css
:root {
  --bg-void: #03060F;       /* Deep space void background */
  --bg-surface: #080D1A;    /* Primary card and panel surface */
  --bg-elevated: #0D1526;   /* High-contrast active layers */
  --accent-electric: #00D4FF;/* Vibrant cyber blue indicators */
  --critical: #FF2D55;      /* High-visibility critical threat red */
  --high: #FF6B1A;          /* Orange high threat marker */
  --text-mono: #64D9A8;     /* Matrix console green-teal text */
}
```

* **Premium Typography**: Leverages Google Fonts `Rajdhani` for display headings/UI actions, and `JetBrains Mono` for log listings, routing metrics, and monospaced console outputs.
* **Cinematic Effects**: Features dynamic card entrance animations, glowing borders, custom cyber scrollbars, blinking status beacons, and subtle CRT monitor scanline screen effects.

---

## 🛠️ Core Architecture

SENTRI is engineered with **zero local build tools, package managers, or server frameworks**. All resources and layout segments are bundled inside a single file.

<div align="center">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
  <img src="https://img.shields.io/badge/D3.js-F9A03F?style=for-the-badge&logo=d3.js&logoColor=white" alt="D3.js" />
  <img src="https://img.shields.io/badge/Chart.js-FF6384?style=for-the-badge&logo=chart.js&logoColor=white" alt="Chart.js" />
</div>

* **Graph Physics**: Leverages D3.js v7 for simulated node positioning, link drawing, and mouse interactions.
* **Volume Sparklines**: Uses Chart.js for rendering the 6-hour incident history timeline with configured layout margins to avoid x-axis label clipping.
* **Local Run**: 100% portable. Runs instantly by double-clicking the file in any modern web browser.

---

## 📖 Simulated Threat Narrative (INC-2847)

The application comes preconfigured with a multi-stage active threat scenario to demonstrate production-grade monitoring capability:

1. **VPN Gateway Brute Force (`EVT-4488`)**: Multiple login failures detected on critical perimeter firewall.
2. **Privileged Credential Abuse (`EVT-4491`)**: Successful administrator logon from a suspicious geolocated IP address.
3. **Internal Port Sweep (`EVT-4493`)**: Reconnaissance traffic sweep mapping database environments.
4. **Data Exfiltration (`EVT-4495`)**: Persistent outbound transfer to an external backup server.
5. **Ransomware Executable (`EVT-4497`)**: File encryption signature triggered on primary file shares.

*The engine simulates background noise by dynamically injecting new authentication logs and system messages into the live feed.*

---

## 💻 Getting Started

### Clone the Repository
```bash
git clone https://github.com/norriy0u/sentri.git
cd sentri
```

### Launch the Application
Simply double-click `sentri.html` to open it in your browser, or launch it via the terminal:

**Windows PowerShell:**
```powershell
Start-Process sentri.html
```

**macOS/Linux Terminal:**
```bash
open sentri.html
```

---

## 🛡️ Verification & Quality Checklist

* [x] **Zero Dependencies**: Requires no npm installs or backend services.
* [x] **No Text Clipping**: All card descenders, graph node labels, and x-axis labels are fully visible.
* [x] **Zoom & Pan Enabled**: D3 simulation supports full interactive navigation controls.
* [x] **Functional Report Export**: Report compiler generates a fully structured log file download.

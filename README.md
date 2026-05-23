# SENTRI // AI Security Threat Monitoring Agent

> **"The analyst that never sleeps."**

SENTRI is an AI-powered Security Threat Monitoring Agent dashboard built specifically for **Track 07** of the Hackathon. It addresses the challenge of alert fatigue in security teams by filtering raw security logs, identifying critical attack chains, and using AI to explain complex attack patterns in simple, human-readable language with recommended containment actions.

It is packaged entirely as a **single, zero-dependency, production-grade HTML/CSS/JS application** that runs natively in any modern desktop browser.

---

## 🚀 Hackathon Track 07 Solution Alignment

### The Problem
Security Operations Centers (SOCs) are flooded with thousands of raw alerts and security logs daily, making it impossible to quickly isolate high-severity campaigns from background noise, leading to critical breaches being overlooked.

### The SENTRI Solution
* **Alert Noise Reduction**: Filters and groups events into an active Threat Feed, automatically highlighting high-severity indicators and allowing analysts to filter by severity levels (Critical, High, Medium, Low).
* **AI Threat Explanation**: Automatically parses multi-stage security events and outputs a clear, 3-sentence summary of the attack chain and immediate remediation steps in a typewriter terminal window.
* **Attack Chain Force Visualizer**: An interactive **D3.js force-directed physics graph** that shows relationships between compromised assets, exfiltration nodes, attacker nodes, and target databases in real-time. Supports dragging, mousewheel panning/zooming, and fullscreen overlay toggle.
* **Geographic Origin Tracking**: An inline stylized SVG map depicting attack vectors from international nodes (e.g., Moscow, Amsterdam) to local target nodes with pulsing ping animations and flowing connection vectors.
* **Active Containment Workflows**: Clickable containment buttons (`⚡ ISOLATE HOST` and `🔒 REVOKE TOKENS`) that trigger animated modal confirmations for immediate security response.
* **Data Log Export**: An `📋 EXPORT REPORT` button that compiles all event details and AI-generated reviews into a structured text report file download.

---

## 🛠️ Technology Stack

* **Structure**: Semantic HTML5.
* **Styling**: Modern Vanilla CSS containing responsive custom variables, glowing borders, custom scrollbars, staggering slide-in cards, CRT scanlines, and glow animations.
* **Graph Visualization**: [D3.js](https://d3js.org/) (via CDN) for physics-simulated node network.
* **Sparklines & Charts**: [Chart.js](https://www.chartjs.org/) (via CDN) for 6-hour security incident volume timeline.
* **Typography**: Imported display faces `Rajdhani` (for display headings) and `JetBrains Mono` (for console logs) from Google Fonts.
* **Dependencies**: None. Purely static front-end; can be launched by double-clicking the file locally.

---

## 📖 Simulated Attack Narrative (INC-2847)

SENTRI comes preloaded with a multi-stage simulated active breach narrative (**Incident INC-2847**) that triggers sequentially:
1. **Initial Access (`EVT-4488`)**: External brute-force attempts on the VPN gateway.
2. **Credential Theft (`EVT-4491`)**: Successful administrative login from a suspicious IP address.
3. **Internal Reconnaissance (`EVT-4493`)**: Port scanning across database segments.
4. **Data Exfiltration (`EVT-4495`)**: Outbound data transfers to an external server.
5. **Ransomware Deployment (`EVT-4497`)**: File encryption routine detected on internal file servers.

*New noise alerts and authentication logs are continually simulated and slide into the active feed dynamically to simulate a live war room environment.*

---

## 💻 Quick Start & Setup

1. **Clone the repository**:
   ```bash
   git clone <your-repository-link>
   cd sentri
   ```
2. **Open the Dashboard**:
   Simply open `sentri.html` in any web browser (Chrome, Firefox, Edge, Safari):
   ```bash
   # In Windows PowerShell:
   Start-Process sentri.html
   
   # In macOS Terminal:
   open sentri.html
   ```

---

## 🎬 3-Minute Demo Video Walkthrough Guide

Use this script as a guide for your 3-minute video submission to score maximum points for **UI/UX, innovation, and technical implementation**:

1. **Introduction (0:00 - 0:45)**:
   * Introduce the team/product: *"This is SENTRI, the AI Security Threat Monitoring Agent, built for Hackathon Track 7."*
   * Explain the value prop: Show the home screen, explaining how it consolidates thousands of raw logs into a single, high-fidelity cyberpunk cyber war room console.
2. **AI Typewriter & Event Feed (0:45 - 1:30)**:
   * Click on the top threat card `EVT-4488` (Critical VPN brute force).
   * Show the **typewriter animation** rendering the AI summary: *"Watch as SENTRI's AI agent parses the raw logs in real-time, explaining exactly what happened in three sentences, listing confidence rates, and providing recommended actions."*
   * Filter the feed by clicking on the `CRITICAL` or `HIGH` pills in the filter bar.
3. **D3 Network Graph & Map (1:30 - 2:15)**:
   * Show the D3 Attack Chain. Scroll the mousewheel to **zoom in/out** and drag to **pan** around the nodes.
   * Click **`⛶ FULL VIEW`** in the graph header to maximize it: *"For complex investigations, analysts can expand the canvas to full screen. We can click on a compromised node (e.g., target databases) to instantly filter related feed events."*
   * Point out the **Geographic Origin Map** in the left sidebar showing the connection path from Amsterdam and Moscow.
4. **Active Containment & Export (2:15 - 3:00)**:
   * Click **`⚡ ISOLATE HOST`** in the actions menu. Show the custom alert modal overlay confirming the network firewall block.
   * Click **`📋 EXPORT REPORT`** to download the structured threat report.
   * Conclude: *"SENTRI is a zero-dependency, single-file prototype that packs enterprise-grade SaaS aesthetics and functionality, proving that AI agents can turn security operations from chaotic to manageable."*

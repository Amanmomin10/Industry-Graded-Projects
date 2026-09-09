<h1 align="center">🛡️ PCAP Storyteller</h1>

<p align="center">
  <strong>Turning Network Traffic into an Understandable Story</strong>
</p>

<p align="center">
  Transform complex PCAP network traffic into an interactive and visual
  forensic investigation experience designed for students and educators.
</p>

---

## 🌟 Why PCAP Storyteller?

Traditional packet-analysis tools such as **Wireshark** are extremely
powerful, but beginners can easily become overwhelmed by thousands of
individual packets.

### The Problem

A PCAP containing 50,000+ packets can look like a massive spreadsheet.
Understanding the relationship between DNS queries, TCP connections,
HTTP traffic, TLS sessions, and suspicious activity can be difficult.

### Our Solution

**PCAP Storyteller** converts raw packet-level information into meaningful
network events and relationships.

Instead of focusing only on individual packets, the platform helps answer:

- Who communicated with whom?
- Which domains were contacted?
- What protocols were involved?
- Which IP addresses appear suspicious?
- Was there potential port scanning?
- Was there unusual DNS behavior?
- Where are external IP addresses located?

The goal is:

**Raw Packets → Events → Relationships → Threats → Visual Story**

---

## 🚀 Key Features

### 🕵️ The Investigator — PCAP Parser

- **Two-Pass Analysis Pipeline**
  - First identifies conversations
  - Then performs detailed protocol analysis

- **Intelligent Event Linking**
  - Correlates DNS queries with resulting network connections
  - Connects related DNS, TCP, HTTP and TLS activity

- **Unified Protocol Handlers**
  - Specialized analysis for DNS, HTTP, TLS, TCP, ICMP and more

---

### 🧠 The Security Guard — Threat Detection

PCAP Storyteller uses heuristic-based behavioral analysis to identify
potentially suspicious network activity.

Features include:

- Port scanning detection
- DNS tunneling indicators
- Suspicious communication patterns
- Behavioral analysis
- Risk scoring

### ⚠️ Risk Scoring

Each IP address can receive a severity score between:

**0 — 100**

This helps investigators prioritize potentially suspicious activity
instead of manually inspecting every connection.

---

### 🌍 The Global View — IP Geolocation

External IP addresses can be mapped geographically using a dual-API
strategy.

- `ipinfo.io`
- `ip-api.com`

The results can be displayed using interactive geographic maps.

---

### 📊 Interactive Visualization

The platform transforms forensic data into visual information that is
easier to understand.

Visualizations can include:

- Network relationships
- Communication events
- Threat indicators
- Risk scores
- IP locations
- Investigation results

---

## 🎓 Educational Curriculum

PCAP Storyteller also provides structured learning material to help
students understand network forensics step by step.

The `documentation/` directory contains modules covering:

1. **Introduction & Problem Statement**
   - Why network forensics can be difficult
   - How PCAP Storyteller addresses the problem

2. **Definitions & Terminology**
   - Packets
   - Protocols
   - DNS
   - TCP
   - IP addresses

3. **Technology Stack**
   - Flask
   - Scapy
   - Folium
   - Frontend technologies

4. **Parsing Pipeline Deep-Dive**
   - Two-pass analysis
   - Packet extraction
   - Conversation discovery
   - Protocol handling

5. **Threat Detection Heuristics**
   - Behavioral analysis
   - Port scanning
   - DNS tunneling
   - Risk scoring

6. **Teaching Flow**
   - Suggested classroom workflow
   - How educators can use the platform

> Additional curriculum modules will be added as the project develops.

---

## 🛠️ Technology Stack

| Technology | Purpose |
|------------|---------|
| **Python** | Core application development |
| **Flask** | Web application backend |
| **Scapy** | PCAP and packet analysis |
| **Folium** | Interactive geographic maps |
| **JavaScript** | Frontend functionality |
| **HTML / CSS** | User interface |
| **Leaflet** | Interactive mapping |
| **Chart.js** | Charts and data visualization |
| **vis.js** | Network/event visualization |

---

## 📁 Project Architecture

The project follows a modular architecture separating the frontend,
backend, packet parsing, threat detection and supporting services.

```text
PCAP-StoryTeller/
│
├── run.py
├── setup.py
│
├── documentation/
│   ├── 00_Introduction_and_Problem_Statement.md
│   ├── 01_Definitions_and_Terminology.md
│   ├── 02_Tech_Stack_and_Flask_Libraries.md
│   ├── 03_Parsing_Pipeline_Deep_Dive.md
│   ├── 05_Threat_Detection_Heuristics.md
│   └── 08_Teaching_Flow_Curriculum.md
│
├── frontend/
│   └── ...
│
└── backend/
    │
    ├── app.py
    │
    ├── data/
    │
    ├── parsers/
    │   ├── pcap_parser.py
    │   └── protocol_handlers.py
    │
    └── services/
        ├── threat_service.py
        ├── map_service.py
        └── report_generator.py
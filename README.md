# SET Triage Atlas

> See how each security alert is investigated and resolved — as an explorable graph.

**▶ Live demo:** https://mechmukul.github.io/set-triage-atlas/ · runs in your browser, no install.

![SET Triage Atlas screenshot](docs/screenshot.png)

## What it is
An interactive, Obsidian-style knowledge graph that maps six common security alerts to the tools,
entities, and response actions involved in handling them — and animates the full triage path for each.

## Why it's useful
New analysts learn triage by osmosis, and even experienced teams handle the same alert inconsistently.
This turns "how do we handle a phishing report / malware hit / data-exfil alert?" into a **visible,
repeatable path**: alert → right tool → entity at risk → proportionate action → close the loop.

## Who it's for / use cases
- **Onboarding / training** new SOC analysts on how alerts flow to resolution.
- **A shared reference** so a team handles each alert type the same, defensible way.
- **Playbook design** — a visual scaffold before writing formal runbooks.
- **Interviews / stakeholder briefings** — explains triage thinking to technical and non-technical audiences in seconds.

## Try it live (30 seconds)
1. Open the live demo.
2. Click a scenario chip — **Phishing**, **Malware**, **Data exfiltration (DLP)**, **Brute force**, **Unauthorised access**, or **Tool unhealthy**.
3. Click **Simulate triage** — the graph pulses along the investigation path while the panel steps through **Detect → Triage → Investigate → Contain → Recover → Close**, naming the tool and the KQL where relevant.
4. Drag nodes, hover to highlight, or click any node to explore its connections.

## How it works
- A force-directed graph (vanilla JS on canvas) links **alerts → tools → entities → actions**; shared nodes (e.g. Sentinel, User, Reset credentials) create the interconnected web.
- Each alert carries a step-by-step playbook; the simulation highlights the relevant node at each phase.
- Node colours: alert (red), tool (blue), entity (purple), action (green), the SET hub (violet).

## Run locally
```bash
python3 -m http.server 8000   # then open http://localhost:8000
```
Or open `index.html` directly.

## Tech & quality
Vanilla HTML/canvas/JS, no dependencies or build step. Playbooks are illustrative and contain no client data.

---
MIT licensed · Built by **Mukul Mech** · Companions: [set-watchtower](https://github.com/mechmukul/set-watchtower) · [gvm-triage](https://github.com/mechmukul/gvm-triage)

# SET Triage Atlas

An interactive, **Obsidian-style knowledge graph** of how a Security Engineering Team investigates
and responds to different security alerts. Pick an alert (phishing, malware, data exfiltration,
brute force, unauthorised access, or a security tool going unhealthy) and it highlights the tools,
entities, and response actions involved, then **simulates the triage** step by step: Detect →
Triage → Investigate → Contain → Recover → Close.

**Open `index.html` in a browser.** No install, no dependencies, no data leaves the page.

## Why I built it
It is the companion to my other project, **SET Watchtower**. Watchtower shows *what is broken*
across the toolkit; Triage Atlas shows *how I would think through and respond to each alert type*.
Together they cover the role's Run, Respond, and Triage loop.

## What it shows
- A force-directed graph (vanilla JS, canvas) linking **alerts &rarr; tools &rarr; entities &rarr; actions**.
- Click any alert node (or use the scenario chips) to focus its neighbourhood, the way Obsidian
  highlights a note's links.
- **Simulate triage** animates a pulse along the investigation path and steps a playbook panel
  through each phase, with the relevant tool and, where useful, the KQL you would run.
- Node types: alert (red), tool (blue), entity (purple), action (green), the SET hub (violet).

## The point I would make in an interview
Good triage is a repeatable path, not guesswork: from the alert, to the right tool, to the entity
at risk, to a proportionate action, and always closing the loop by tuning and assigning ownership.
This graph makes that thinking visible for six common alert types on this team's toolset
(SIEM, Defender, Email Gateway, IDPS, GVM, malware protection).

## Notes
Illustrative playbooks and thresholds, no client or tenant data. Built by Mukul Mech.

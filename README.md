# Detections.AI-contribution

Detections.ai Contributions

A curated collection of my detection engineering work contributed to Detections.ai — spanning Sigma rules, YARA/YARA-L signatures, and supporting detection tooling. This repo doubles as a portfolio of production-grade detection logic mapped to the MITRE ATT&CK framework.

About

I'm a threat researcher and detection engineer with 13+ years across SOC operations, SIEM engineering, and threat intelligence. This repository captures detections I've authored and refined against real datasets — the same rigor I apply to enterprise blue-team work: every rule is validated, ATT&CK-mapped, and built with an eye toward log fidelity and false-positive reduction.

What's Inside
Directory	Contents
sigma/	Platform-agnostic Sigma detection rules, ATT&CK-tagged
yara/	YARA-X pattern-matching signatures for file/memory artifacts
yara-l/	YARA-L correlation rules targeting Chronicle/SecOps UDM
tooling/	Python utilities for rule translation, enrichment, and validation
Coverage Highlights
Identity & access: Valid Accounts (T1078), including cloud-federated (T1078.004) detections for AWS CloudTrail, Azure AD, and Okta telemetry
MITRE ATT&CK mapping: Every detection carries technique/sub-technique tags for coverage tracking
Multi-platform: Rules span Windows Event Logs, Linux, macOS, and cloud/identity providers — with honest notes on telemetry gaps where they exist
Methodology

Detections here follow a consistent quality bar:

Schema first — internalize the data model (UDM, CloudTrail event structure, etc.) before writing syntax
ATT&CK-anchored — start from adversary technique, work backward to observable telemetry
Validated against real data — tested with corpora like Splunk BOTS and attack_data rather than synthetic assumptions
Tuned for signal — written to minimize false positives and account for log brittleness
Tooling

Selected utilities included in tooling/:

Sigma translation — converts detections between formats (e.g., Carbon Black → Sigma) using pySigma with custom backends and field-mapping pipelines
Threat intel enrichment — aggregates IOCs from sources including OTX, AbuseIPDB, URLhaus, ThreatFox, and CISA KEV
Contributing

Contributions, corrections, and detection improvements are welcome. If you'd like to propose a rule or refinement:

Fork the repository
Create a feature branch (git checkout -b detection/your-rule)
Ensure new detections include ATT&CK mappings and validation notes
Open a pull request with a clear description of the behavior being detected

Please keep detections vendor-neutral where possible and document any known false-positive conditions.

License

Released under the MIT License. Detection logic is provided as-is for defensive security use.

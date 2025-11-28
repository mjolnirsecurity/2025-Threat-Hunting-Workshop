# 2025-Threat-Hunting-Workshop

Created by Mjolnir Security Inc.
Part of the Threat Hunting Deep Dive: A Modern SOC Experience workshop.

Overview

This repository provides access to the forensic datasets, memory dumps, system diagnostics, and supporting artifacts used in the Mjolnir Security 2025 Threat Hunting Workshop.
These materials originate from ransomware execution inside isolated Azure VDI lab environments. They have been shared publicly to support:
- DFIR research
- Threat hunting education
- Memory forensics tooling validation
- Classroom training
- Academic studies
- Detection engineering
- Malware behavior analysis

The dataset captures real system state immediately after suspicious and malicious activity, offering investigators a realistic view of how ransomware behaviors appear across memory, OS telemetry, and third-party diagnostic tools.


What This Dataset Contains

This repository links to several forensic artifacts generated during the workshop:

1. Memory Dumps

Two Windows memory captures from live ransomware simulations:
- Memory Dump 1 (Nov 17)
https://f002.backblazeb2.com/file/mjolnirtraining/TH%202025/Nov17memdump.7z
- Memory Dump 2 (Nov 25)
https://f002.backblazeb2.com/file/mjolnirtraining/TH%202025/Nov25-TH25-2-memdump.mem

These memory images contain active processes, code injections, threads, network artifacts, and volatile malicious indicators suitable for Volatility, Rekall, and other memory forensics frameworks.


2. ESET SysInspector Diagnostics

Snapshot of processes, drivers, autostarts, registry entries, and network activity at the time of acquisition:
- SysInspector Data for Memory Dump 1
https://f002.backblazeb2.com/file/mjolnirtraining/TH%202025/SysInspector-TH25-3-251121-084851.zip

This provides heuristic scoring and system health visibility useful for DFIR triage comparisons.


3. Magnet AXIOM / Magnet Nexus Analysis

AXIOM exports allow deep OS-level and memory-level examination without needing a full AXIOM license.
- Magnet Nexus Memory Analysis (Dump 1)
https://f002.backblazeb2.com/file/mjolnirtraining/TH%202025/Threat%20Hunting%20Workshop%20-%20TH25-3%20-%20CSV.zip
- Magnet Cyber / OS Forensics Export (Dump 1)
https://f002.backblazeb2.com/file/mjolnirtraining/TH%202025/TH25-3-OS%20Forensics.zip

These exports contain:
- Parsed registry keys
- Event logs
- File system metadata
- Prefetch, Shimcache, Amcache
- Memory object summaries
- Reconstructed process trees
- Correlation-ready CSVs


4. Hard Drive Images

Disk images captured to support correlation between volatile and non-volatile artifacts:
- HDD Images for Memory Dump 1
https://f002.backblazeb2.com/file/mjolnirtraining/TH%202025/TH25-3-HD.7z

These images pair with memory dump 1 for complete disk + memory analysis.

Context: About the Workshop

These datasets were generated as part of Mjolnir Security’s 2025 Threat Hunting Deep Dive Workshop, where participants:
- Executed ransomware inside isolated Azure VDI
- Observed telemetry propagation into SIEM and XDR
- Performed memory forensics
- Built detection engineering logic (YARA/Sigma)
- Investigated malicious behavior using enterprise tools including:
	- Sumo Logic (SIEM / Dojo AI)
	- SentinelOne Purple AI / XDR
	- Nextron Thor Cloud
	- Mjolnir AI

By releasing this dataset publicly, we aim to give researchers and students access to the same evidence used in a real training exercise.

Intended Use Cases

This dataset is suitable for:
- Memory forensics (Volatility, Rekall, AXIOM)
- Timeline reconstruction
- Malware behavior profiling
- YARA rule development and testing
- DFIR training and labs
- SOC analyst skill building
- Academic courses and cyber ranges
- Evaluating forensic tool accuracy

Disclaimer

These artifacts contain malware-generated evidence, though no active malware samples are included.
All content is for educational and research purposes only.
Do not load these datasets on production systems.
Use inside isolated forensic environments or sandboxes.

Credits

Dataset produced by Mjolnir Security Inc.
Workshop led by Milind Bhargava and the Mjolnir Threat Hunting & DFIR team.
Released for public benefit to advance digital forensics science and analyst training.

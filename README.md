# PHISHBOOK

**Phishing Incident Playbook** — structured end-to-end IR reference for SOC analysts.

Part of the [H3AD-IR](https://h3ad-sec.github.io/H3AD-IR/) module under the [H3AD-SEC](https://h3ad-sec.github.io) portfolio platform.

**Live:** [h3ad-sec.github.io/PHISHBOOK](https://h3ad-sec.github.io/PHISHBOOK/)

---

## What it covers

9 investigation sections from first alert to ticket closure:

| # | Section | Focus |
|---|---------|-------|
| 01 | Overview | Severity taxonomy (P1–P4), flow summary, scope |
| 02 | Initial Triage | Envelope collection, sender auth quick-check, enrichment |
| 03 | Header Analysis | Relay chain, SPF/DKIM/DMARC interpretation, X-Originating-IP |
| 04 | URL Analysis | Defanging, domain risk signals, sandbox tooling |
| 05 | Attachment Analysis | Pre-detonation checklist, file type risk matrix, post-detonation IOC extraction |
| 06 | Identity & Impact | Okta log review, session anomaly indicators, credential compromise response |
| 07 | Containment | Ordered action sequence: recall, block, revoke, preserve |
| 08 | Escalation | L1/L2/L3 decision table, IR handoff criteria, comms template |
| 09 | Query Templates | KQL (Defender/Sentinel), SPL (Splunk/Okta), XQL (Cortex XDR) |

---

## Features

- Enrichment tool buttons per section — external tools open directly, H3AD-SEC tools copy the IOC to clipboard then launch
- Syntax-highlighted KQL, SPL, and XQL code blocks with one-click copy
- MITRE ATT&CK sub-technique tags on relevant sections
- Session progress tracker — visited sections are marked in the sidebar
- Keyboard navigation: `→` next, `←` prev, `1–9` direct jump, `P` print, `T` toggle theme, `?` shortcuts
- Print export — clean print stylesheet renders all 9 sections for offline use
- Light/dark theme with `localStorage` persistence
- Mobile responsive with fixed bottom nav bar

---

## Enrichment tools referenced

| Tool | Source | Section |
|------|--------|---------|
| X-VERDIKT | H3AD-SEC | IP enrichment (triage, headers, URLs) |
| PARSE-X | H3AD-SEC | IOC extraction from raw email body |
| DNSCOPE | H3AD-SEC | Domain/IP infra mapping |
| MAILSCOPE | H3AD-SEC | Full header block analysis |
| EmailRep | emailrep.io | Sender email reputation |
| MXToolbox | mxtoolbox.com | IP blacklist, header analysis |
| URLScan.io | urlscan.io | Safe URL rendering and screenshot |
| VirusTotal | virustotal.com | URL and hash reputation |
| URLhaus | abuse.ch | Malicious URL lookup |
| CheckPhish | checkphish.ai | Phishing page classification |
| Any.run | any.run | Interactive sandbox |
| Hybrid Analysis | hybrid-analysis.com | Static + dynamic analysis |
| MalwareBazaar | abuse.ch | Hash lookup |
| HaveIBeenPwned | haveibeenpwned.com | Breach exposure check |

---

## Related tools

- [PHISHOPS](https://h3ad-sec.github.io/PHISHOPS/) — active case tracker with live IOC aggregator (use alongside this playbook)
- [TRACERULES](https://h3ad-sec.github.io/TRACERULES/) — production-grade detection rules
- [QUICKTRACE](https://h3ad-sec.github.io/QUICKTRACE/) — daily workflow queries
- [TRACEPULSE](https://h3ad-sec.github.io/TRACEPULSE/) — campaign-tied query packs

---

## Stack

Single-file HTML/CSS/JS. No backend, no dependencies beyond Google Fonts. GitHub Pages compatible.

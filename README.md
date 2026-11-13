# Awesome-Real-Time-Threat-Hunting-IOC-Scanning

# Awesome Real-Time Threat Hunting & IOC Scanning

> A curated list of top Real-Time Threat Hunting and IOC Scanning platforms — both SaaS/Hosted commercial threat intelligence and hunting services and open-source alternatives for proactive adversary detection and indicator matching.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [CrowdStrike Falcon Overwatch](#crowdstrike-falcon-overwatch)
  - [Microsoft Defender Experts for Hunting](#microsoft-defender-experts-for-hunting)
  - [SentinelOne Threat Hunting](#sentinelone-threat-hunting)
  - [Red Canary](#red-canary)
  - [Rapid7 Threat Hunting](#rapid7-threat-hunting)
  - [Druva Threat Hunting](#druva-threat-hunting)
- [Open-Source Software](#-open-source-software)
  - [MISP](#misp)
  - [Sigma](#sigma)
  - [TheHive & Cortex](#thehive--cortex)
  - [TraceForge](#traceforge)
  - [Pulse Intelligence](#pulse-intelligence)
  - [Anubi](#anubi)
  - [GitHub IOC Scanner](#github-ioc-scanner)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Real-Time Threat Hunting and IOC Scanning platforms. These are not open-source but are included as reference points for feature comparison.

### CrowdStrike Falcon Overwatch
**Type:** Managed threat hunting with human-led adversary detection  
Falcon Overwatch is a 24/7 managed threat hunting service that combines human expertise with the Falcon platform's telemetry and AI. It proactively hunts for adversary activity that automated detections miss, with threat intelligence from CrowdStrike's adversary research.

### Microsoft Defender Experts for Hunting
**Type:** Proactive hunting service on Microsoft telemetry  
Defender Experts for Hunting provides Microsoft-led proactive threat hunting across endpoints, identities, email, and cloud apps. It surfaces human-verified findings and provides guided response recommendations, leveraging Microsoft's threat intelligence and signal depth.

### SentinelOne Threat Hunting
**Type:** Autonomous hunting with Storyline correlation  
SentinelOne provides threat hunting capabilities through its Singularity platform, with Storyline visualization connecting related events across endpoints. Its autonomous agents can isolate threats and provide forensic context for manual hunting.

### Red Canary
**Type:** Managed detection and response with threat hunting  
Red Canary is a leading MDR provider that combines automated detection with human threat hunting and response. It is known for its detection engineering depth and transparent communication of findings.

### Rapid7 Threat Hunting
**Type:** Hunting within Rapid7's security platform  
Rapid7 provides threat hunting capabilities through its InsightIDR and broader security platform, with detection rules, UEBA, and investigation workflows. It is often paired with Rapid7's vulnerability management and incident response services.

### Druva Threat Hunting
**Type:** Data protection telemetry for threat hunting  
Druva's Cyber Resiliency features include threat hunting capabilities over backup data, with ransomware detection, anomaly analysis, and audit trails. It allows SecOps teams to investigate suspicious activity across protected workloads, with view-only administrator roles for separation of duties.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Real-Time Threat Hunting and IOC Scanning tools. The open-source ecosystem is anchored by **MISP** and **Sigma** as the foundational standards, with complementary tools for case management, investigation, and specialized scanning.

### MISP
**Stack:** PHP / MySQL | **License:** AGPL-3.0  
MISP (Malware Information Sharing Platform) is the most widely deployed open-source threat intelligence platform, focused on **IOC storage, correlation, and sharing** . It provides an efficient IOC database, automatic correlation between attributes (including fuzzy hashing and CIDR block matching), flexible data models for complex objects, and built-in sharing with flexible distribution models . It supports export to IDS formats (Suricata, Snort, Zeek), STIX 1/2, OpenIOC, and more, with PyMISP for Python integration . **Best for:** Organizations needing a proven, community-standard platform for IOC collection, correlation, and intelligence sharing with partners and sector communities.

### Sigma
**Stack:** YAML rules / Python (pySigma) | **License:** Open Source (SigmaHQ)  
Sigma is a **generic signature format for SIEM systems** — "for log files what Snort is for network traffic and YARA is for files" . The SigmaHQ repository offers **more than 3,000 detection rules** across categories: Generic Detection, Threat Hunting, Emerging Threat, Compliance, and Placeholder rules . Threat Hunting rules are broader in scope, meant to give analysts a starting point to hunt for suspicious activity, while Emerging Threat rules cover specific timely campaigns and zero-days . Rules are vendor-agnostic and convertible to SIEM query languages via Sigma CLI, sigconverter.io, or pySigma . **Best for:** Detection engineers and threat hunters wanting a community-maintained, vendor-agnostic rule library for log-based hunting across any SIEM.

### TheHive & Cortex
**Stack:** Scala / Elasticsearch / Cassandra | **License:** AGPL-3.0  
TheHive is a **Security Incident Response Platform** for SOC, CSIRT, and CERT teams, offering case management, task workflows, observable management, and real-time collaboration [citation:4]. It is tightly integrated with MISP for threat intelligence sharing [citation:4]. **Cortex** provides automated enrichment and analysis of observables (IOCs) through analyzers like VirusTotal, AbuseIPDB, MISP, and OTX [citation:4][citation:9]. Together they operationalize threat intelligence: MISP/Sigma for detection logic and IOC management, TheHive for case creation and response, and Cortex for automated enrichment . **Best for:** SOC and CSIRT teams wanting to operationalize threat hunting findings with case management and automated IOC enrichment.

### TraceForge
**Stack:** Python / Go / SQLite | **License:** Open Source (PyPI)  
TraceForge is a **local CLI toolkit for investigative workflows**, explicitly built for DFIR, OSINT, and authorized security research [citation:1]. Key threat hunting features include **IOC extraction and defanging** (IPs, domains, hashes, URLs), evidence hashing with chain-of-custody, timeline processing, filesystem baselining and diffs, and **multi-format exports** including STIX 2.1 and MISP [citation:1]. It includes an external tool catalog with profile-based setup, and runs cross-platform (macOS, Linux, Termux) [citation:1]. **Best for:** DFIR analysts and investigators wanting a local, privacy-preserving toolkit for IOC extraction, evidence handling, and timeline analysis without a server dependency.

### Pulse Intelligence
**Stack:** Next.js / PostgreSQL / Redis | **License:** Open Source (GitHub)  
Pulse Intelligence is an **open-source, self-hosted threat intelligence platform** for CTI analysts and SOC teams [citation:11]. It tracks threat actors, campaigns, IOCs, CVEs, and ATT&CK mappings, with feed ingestion from CISA KEV, NVD, FIRST EPSS, abuse.ch, and OTX [citation:11]. Features include **IOC enrichment** (OTX, AbuseIPDB, VirusTotal with Redis-backed quota controls), **saved threat hunts** over indicator fields with alerting, and **export to CSV, STIX 2.1, MISP JSON, and Snort/Suricata rules** [citation:11]. It also generates scheduled Markdown reports from new indicators and hunt alerts [citation:11]. **Best for:** CTI analysts wanting a self-hosted platform that combines feed ingestion, enrichment, hunting, and export in one workspace.

### Anubi
**Stack:** Python / YARA | **License:** Open Source (GitHub)  
Anubi is a **portable IOC/hash scanner and layer-4 IDS** that combines five engines: IOC scanner (YARA rules on filesystem), hash scanner, IP checker (network monitoring), filesystem modification monitor (Voyeur), and SBOM generation [citation:12]. It uses a prepared rule set generated daily, with support for custom rules, and provides a web UI and API for interaction [citation:12]. **Best for:** Analysts wanting a lightweight, portable scanner that applies YARA and hash rules to local filesystems alongside network IP monitoring, without deploying a full SIEM.

### GitHub IOC Scanner
**Stack:** Python | **License:** Open Source (PyPI)  
GitHub IOC Scanner is a CLI tool for **scanning GitHub repositories for IOCs in package dependencies**, covering npm, pip, RubyGems, Composer, Go modules, and Cargo [citation:2]. It includes **2,900+ IOC definitions** for known malicious packages (typosquatting, dependency confusion, compromised packages), with parallel processing, intelligent caching, and real-time progress [citation:2]. It supports organization-wide, team-specific, or individual repository scanning [citation:2]. **Best for:** Security teams wanting to detect supply chain compromises (malicious packages, typosquatting) in their GitHub organizations, particularly for dependency-based attacks.

---

## 📊 Comparison at a Glance

| Software | License | Stack | IOC Scanning | Detection Rules | Case Management | Self-Hosted | Best For |
|----------|---------|-------|--------------|-----------------|-----------------|-------------|----------|
| **CrowdStrike Overwatch** | Proprietary | Cloud | ✅ | ✅ Human-led | (Platform) | ❌ | 24/7 managed hunting |
| **Microsoft Defender Experts** | Proprietary | Cloud | ✅ | ✅ | (Platform) | ❌ | Microsoft telemetry hunting |
| **Druva** | Proprietary | Cloud | ✅ | ✅ Ransomware | (Audit trails) | ❌ | Backup data threat hunting |
| **MISP** | AGPL-3.0 | PHP/MySQL | ✅ Deep | ❌ (IOC store) | ❌ | ✅ | IOC correlation + sharing |
| **Sigma** | Open Source | YAML/pySigma | ❌ (Rules) | ✅ 3,000+ rules | ❌ | ✅ | Vendor-agnostic hunting rules |
| **TheHive & Cortex** | AGPL-3.0 | Scala/Elastic | ✅ (Enrichment) | ❌ | ✅ | ✅ | Operationalize hunting findings |
| **TraceForge** | Open Source | Python/Go | ✅ Extraction | ❌ | ✅ (Local) | ✅ | DFIR IOC extraction + evidence |
| **Pulse Intelligence** | Open Source | Next.js/Postgres | ✅ Enrichment | ✅ ATT&CK | ✅ (Hunts) | ✅ | CTI feed + hunt + export |
| **Anubi** | Open Source | Python/YARA | ✅ YARA + hash | ✅ YARA rules | ❌ | ✅ | Portable filesystem/network scanning |
| **GitHub IOC Scanner** | Open Source | Python | ✅ Supply chain | ✅ 2,900+ IOCs | ❌ | ✅ | GitHub dependency compromise |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Real-Time Threat Hunting or IOC Scanning tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source. Note that the open-source ecosystem **splits** between **foundational standards** (MISP for IOC correlation and sharing, Sigma for vendor-agnostic detection rules), **operational platforms** (TheHive for case management, Pulse Intelligence for feed ingestion and hunting), and **specialized scanners** (TraceForge for DFIR IOC extraction, Anubi for portable YARA/hash scanning, GitHub IOC Scanner for supply chain compromise). **MISP** and **Sigma** are the two projects that underpin most open-source threat hunting workflows — MISP for the intelligence layer and Sigma for the detection logic . Commercial platforms like CrowdStrike Overwatch and Microsoft Defender Experts remain differentiated by human-led hunting at scale and proprietary adversary intelligence that open-source tools cannot replicate.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐

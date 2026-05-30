# horadric-archives

*Stay awhile and listen.* This repository is a consolidated collection of **open-source cyber threat intelligence** — vulnerability data, threat-actor and ransomware tracking, malware indicators, and detection rules — pulled together from across the security community into a single, reliable, regularly-refreshed download.

Security data is scattered across dozens of platforms, each with its own format and cadence. This archive aggregates the **publicly-available** sources into one place so researchers, blue-teamers, and homelab tinkerers can grab a clean snapshot without chasing 38 different feeds.

> Each release is produced automatically by a snapshot tool that takes the **latest copy of every source feed** and packages it with a machine-readable manifest. Nothing here is hand-edited after generation, so the data stays verifiable against the upstream sources.

---

## What's in the download

The latest snapshot (`cti_sources_2026-05-29.zip`) is **~535 MB compressed** (~810 MB extracted), containing **681 files across 38 sources**, organized into two top-level directories plus a manifest:

| Path | Contents | Size (extracted) |
| :--- | :--- | ---: |
| **`Vulnerability_Intelligence/`** | Vulnerabilities, IP/URL/domain blocklists, malware IOCs, ransomware tracking, and detection rules (31 sources) | ~241 MB |
| **`External_Datasets/`** | Frameworks & structured datasets — MITRE ATT&CK/CAPEC (STIX), OSV, MISP Galaxy, GitHub Advisory DB (7 sources) | ~569 MB |
| **`metadata.json`** | Machine-readable manifest: per-source bucket, origin URL, license, snapshot date, file count, and byte size | — |
| **`ATTRIBUTION.md`** | Human-readable source + license credits | — |
| **`manifest.txt`** | Flat file listing with sizes for quick inspection | — |

Inside each bucket the layout is `<source>/<feed>/<files>`, holding the **most recent fetched copy** of each feed (historical snapshots are not bundled — every release is a current-state snapshot).

> **A note on what is *not* here.** This is an **open-source-only** archive. Commercial / API-key-gated feeds (e.g. IBM X-Force, VirusTotal, Recorded Future) are **deliberately excluded** — they aren't ours to redistribute. The maintainer's own proprietary processed layer (embeddings, BM25 indices, calibration data, exploit-nickname maps) is **not part of this public source bundle** and is kept separate.

---

## Sources & attribution

This data is gathered from the open security community, and it matters that credit is given where it's due. Every source below is included under its own terms — `metadata.json` and `ATTRIBUTION.md` in each release carry the per-source license. **The underlying data belongs to its original publishers**; this project only curates and packages it.

### Vulnerabilities & exploit research
| Source | Data | License | Reference |
| :--- | :--- | :--- | :--- |
| CISA | Known Exploited Vulnerabilities (KEV) | US Gov public domain | [cisa.gov](https://www.cisa.gov/known-exploited-vulnerabilities-catalog) |
| NIST NVD | NVD API 2.0 vulnerability data | US Gov public domain | [nvd.nist.gov](https://nvd.nist.gov/) |
| CVE Project | Official CVE records (JSON v5) | CVE Program Terms | [github.com/CVEProject](https://github.com/CVEProject) |
| FIRST.org | EPSS exploit-prediction scores | Free w/ attribution | [first.org/epss](https://www.first.org/epss) |
| Exploit-DB | Public exploit archive + CVE maps | GPLv2 | [gitlab.com/exploit-database](https://gitlab.com/exploit-database/exploitdb) |
| OSV.dev | Open-source vulnerability database | CC-BY-4.0 | [osv.dev](https://osv.dev) |
| GitHub | GitHub Advisory Database | CC-BY-4.0 | [github.com/advisories](https://github.com/advisories) |

### Network & infrastructure intelligence
| Source | Data | License | Reference |
| :--- | :--- | :--- | :--- |
| Spamhaus | DROP / EDROP malicious netblocks | Spamhaus terms | [spamhaus.org](https://www.spamhaus.org/drop/) |
| SANS ISC | DShield top attacking IPs | Free use | [dshield.org](https://www.dshield.org) |
| Blocklist.de | Aggregated attack-IP categories | Free use | [blocklist.de](https://www.blocklist.de) |
| Emerging Threats | Compromised-IP blocklists | BSD (ETOpen) | [emergingthreats.net](https://rules.emergingthreats.net) |
| Abuse.ch | Feodo Tracker (C2 IPs), URLhaus, SSL/JA3 blacklists | CC0 | [abuse.ch](https://abuse.ch) |
| Tor Project | Current Tor exit nodes | Public | [torproject.org](https://check.torproject.org) |
| Hagezi | DNS threat-intelligence feeds | GPL-3.0 | [github.com/hagezi](https://github.com/hagezi/dns-blocklists) |

### Malware research & vendor IOCs
| Source | Data | License | Reference |
| :--- | :--- | :--- | :--- |
| ESET | Malware IOCs from APT investigations | BSD (see repo) | [github.com/eset](https://github.com/eset/malware-ioc) |
| SophosLabs | Enterprise malware IOCs | See repo | [github.com/sophoslabs](https://github.com/sophoslabs/IoCs) |
| Dr.Web | Android / mobile malware IOCs | See repo | [github.com/DoctorWebLtd](https://github.com/DoctorWebLtd/malware-iocs) |
| PRODAFT | Mobile / banking-trojan IOCs | See repo | [github.com/prodaft](https://github.com/prodaft/malware-ioc) |
| executemalware | Continuously-updated malware IOCs | See repo | [github.com/executemalware](https://github.com/executemalware/Malware-IOCs) |
| Bitdefender Labs *(vendor content)* | Threat-research feed | Vendor terms | [bitdefender.com](https://www.bitdefender.com/blog/labs/) |
| Malwarebytes Labs *(vendor content)* | Threat-research feed | Vendor terms | [malwarebytes.com](https://www.malwarebytes.com/blog) |
| Microsoft MSRC *(vendor content)* | Security Update Guide | Vendor terms | [msrc.microsoft.com](https://msrc.microsoft.com/update-guide) |

### Ransomware & actor tracking
| Source | Data | License | Reference |
| :--- | :--- | :--- | :--- |
| Ransomwatch | Live ransomware group tracking + posts | MIT | [github.com/joshhighet](https://github.com/joshhighet/ransomwatch) |
| Ransomware.live | Ransomware group API tracking | Free API | [ransomware.live](https://www.ransomware.live) |
| RansomLook | Gang profiles + victim posts | Free | [ransomlook.io](https://www.ransomlook.io) |
| Orange Cyberdefense | Ransomware relationships & timelines | See repo | [github.com/cert-orangecyberdefense](https://github.com/cert-orangecyberdefense/ransomware_map) |
| DeepDarkCTI | Dark-web actors & exploit databases | See repo | [github.com/fastfire](https://github.com/fastfire/deepdarkCTI) |
| NCSC UK | National advisories | OGL v3.0 | [ncsc.gov.uk](https://www.ncsc.gov.uk) |

### Detection rules & frameworks
| Source | Data | License | Reference |
| :--- | :--- | :--- | :--- |
| MITRE | ATT&CK Enterprise/ICS + CAPEC (STIX) | Apache-2.0 / MITRE terms | [github.com/mitre/cti](https://github.com/mitre/cti) |
| MISP Galaxy | Threat-actor / malware clusters | CC-BY (see repo) | [github.com/MISP](https://github.com/MISP/misp-galaxy) |
| YARA Rules | Community malware-detection rules | See repo | [github.com/Yara-Rules](https://github.com/Yara-Rules/rules) |
| ReversingLabs | Vendor YARA rules | MIT | [github.com/reversinglabs](https://github.com/reversinglabs/reversinglabs-yara-rules) |
| ClamAV | Virus signature databases | GPLv2 | [clamav.net](https://www.clamav.net) |
| Snort | Community ruleset | GPLv2 | [snort.org](https://www.snort.org) |
| Suricata | Emerging Threats Open ruleset | BSD/MIT | [emergingthreats.net](https://rules.emergingthreats.net) |
| Bert-Jan / PyMISP | OSINT feed aggregation + CISA alerts | See repo | [github.com/Bert-JanP](https://github.com/Bert-JanP/Open-Source-Threat-Intel-Feeds) |

*Vendor-content feeds (Bitdefender / Malwarebytes / Microsoft) are syndicated research feeds; their article text remains the property of the respective vendor and is included only under each vendor's own terms.*

---

## Snapshot manifest — 2026-05-29

| Bucket | Top sources (by size) | Sources | Size (extracted) |
| :--- | :--- | ---: | ---: |
| Vulnerability_Intelligence | ClamAV (113 MB), Hagezi (72 MB), abuse.ch (13 MB), Exploit-DB (10 MB) | 31 | ~241 MB |
| External_Datasets | OSV (502 MB), MITRE ATT&CK (51 MB), MISP Galaxy (7 MB), CAPEC (4 MB) | 7 | ~569 MB |
| **Total** | | **38** | **~810 MB** (~535 MB zipped) |

The authoritative, per-file manifest ships inside every release as `metadata.json`.

---

## Usage

Data is provided in the sources' native formats (JSON, CSV, STIX, plain-text rule files), kept verbatim from upstream so it parses the same way the original feeds do.

1. Download the latest `cti_sources_*.zip` from the **Releases** page (or the mirror link).
2. Extract it; point your tooling at the `Vulnerability_Intelligence/` and `External_Datasets/` folders.
3. Cross-reference `metadata.json` for source URLs, licenses, and snapshot dates.

It's ready to feed into a SIEM (Wazuh, etc.), load into a lab, or test detection rules against. A fresh snapshot is published on a **weekly** cadence.

---

## Future plans

- An automated ingestion pipeline (in progress) keeps the snapshots current without manual steps.
- A deterministic, non-LLM expert-network layer to organize and cross-link this data without the noise of generative models.
- Documentation for using these feeds with hardware firewalls (e.g. Raspberry Pi 5 / OPNsense).

---

## License

The **curation and structure** of this repository are released under the **MIT License**. The **underlying data belongs to the original sources** listed above and is redistributed under each source's own terms — please honor those terms when you use it. All data is provided for **educational and defensive** purposes.

Accurate information is the foundation of a strong defense. Use it responsibly.

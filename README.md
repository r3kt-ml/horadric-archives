# horadric-archives

Stay awhile and listen. This repository is a collection of cyber threat intelligence that I put together for my own research and technical work. Security data is often spread across too many different platforms, so I wanted to consolidate open-source indicators, threat actor behaviors, and exploit data into a single, reliable location.

## Contents

The archive is structured for use in security monitoring and lab environments. The latest export includes several primary directories containing both raw feeds and processed intelligence:

* **Vulnerability_Intelligence**: This contains approximately 1.9 GB of raw archives. It includes data from primary sources like NIST, CISA, and various community-driven feeds such as abuse.ch, bitdefender, and emergingthreats.
* **R3KT_Refined_Models**: This folder includes embeddings, BM25 indices, and calibration datasets. I processed these for deterministic analysis without using large language models. It also features a curated list of exploit nicknames to help resolve common names like Log4Shell or PrintNightmare.
* **External_Datasets**: This section contains third-party research archives including MITRE ATT&CK STIX data, DGA datasets, and specialized threat intelligence from sources like ShinyHunters and MSSOC.
* **metadata.json**: This is a detailed manifest that lists file counts, source descriptions, and timestamps to ensure the integrity of the bulk download.

## Data Intelligence and Attribution

I gathered this information from the open-source security community. It is important to cite where this data actually originates so the archives remain transparent and verifiable. This list represents the active feeds currently ingested into the registry.

### Vulnerabilities and Exploit Research
| Source | Nature of Data | Reference |
| :--- | :--- | :--- |
| CISA | Known Exploited Vulnerabilities (KEV) | [cisa.gov](https://www.cisa.gov/known-exploited-vulnerabilities-catalog) |
| NIST | NVD API 2.0 vulnerability data | [nvd.nist.gov](https://nvd.nist.gov/) |
| CVE Project | Daily CVE deltas and official JSON V5 formats | [github.com/CVEProject](https://github.com/CVEProject) |
| FIRST.org | Exploit Prediction Scoring System (EPSS) | [api.first.org](https://api.first.org) |
| Exploit-DB | Public exploit archives and CVE mappings | [gitlab.com/exploit-database](https://gitlab.com/exploit-database) |
| OSV.dev | Open source vulnerability database | [osv.dev](https://osv.dev) |
| GitHub | GitHub Advisory Database | [github.com/advisories](https://github.com/advisories) |

### Network and Infrastructure Intelligence
| Source | Nature of Data | Reference |
| :--- | :--- | :--- |
| Spamhaus | DROP and EDROP malicious netblocks | [spamhaus.org](https://www.spamhaus.org) |
| SANS ISC | DShield top attacking IPs | [feeds.dshield.org](https://feeds.dshield.org) |
| Blocklist.de | Aggregated attack IP categories | [blocklist.de](https://www.blocklist.de) |
| Emerging Threats | Compromised IP blocklists | [emergingthreats.net](https://rules.emergingthreats.net) |
| Abuse.ch | Feodo Tracker (C2 IPs) and URLhaus (malware URLs) | [abuse.ch](https://abuse.ch) |
| Tor Project | Current Tor exit nodes | [torproject.org](https://check.torproject.org/exit-addresses) |
| Hagezi | DNS Threat Intelligence Feeds | [github.com/hagezi](https://github.com/hagezi) |

### Malware Research and Vendor Intel
| Source | Nature of Data | Reference |
| :--- | :--- | :--- |
| MalwareBazaar | Malware sample hashes and metadata | [bazaar.abuse.ch](https://bazaar.abuse.ch) |
| SSL Blacklist | Malicious SSL and JA3 fingerprints | [sslbl.abuse.ch](https://sslbl.abuse.ch) |
| ESET / Sophos | Vendor malware IOCs from investigations | [github.com/eset](https://github.com/eset) / [sophoslabs](https://github.com/sophoslabs) |
| Microsoft | MSRC Security Update Guide | [api.msrc.microsoft.com](https://api.msrc.microsoft.com) |
| Bitdefender / Malwarebytes | Threat research narrative and blog feeds | [bitdefender.com](https://bitdefender.com) / [malwarebytes.com](https://blog.malwarebytes.com) |
| IBM X-Force | Commercial-grade vendor intelligence | [api.xforce.ibmcloud.com](https://api.xforce.ibmcloud.com) |

### Ransomware and Actor Tracking
| Source | Nature of Data | Reference |
| :--- | :--- | :--- |
| Ransomwatch | Live ransomware group tracking and posts | [github.com/joshhighet](https://github.com/joshhighet/ransomwatch) |
| Ransomware.live | Ransomware group API tracking | [api.ransomware.live](https://api.ransomware.live) |
| RansomLook | Ransomware gang profiles and victim posts | [ransomlook.io](https://ransomlook.io) |
| Orange Cyberdefense | Ransomware relationships and timelines | [github.com/cert-orangecyberdefense](https://github.com/cert-orangecyberdefense) |
| DeepDarkCTI | Dark web actor and exploit databases | [github.com/fastfire](https://github.com/fastfire/deepdarkCTI) |

### Detection Rules and Frameworks
| Source | Nature of Data | Reference |
| :--- | :--- | :--- |
| MITRE | ATT&CK Enterprise/ICS and CAPEC | [github.com/mitre/cti](https://github.com/mitre/cti) |
| YARA Rules | Community malware detection rules | [github.com/Yara-Rules](https://github.com/Yara-Rules) |
| ClamAV | Virus signature databases | [database.clamav.net](https://database.clamav.net) |
| Snort / Suricata | Community rulesets and ETOpen rules | [snort.org](https://www.snort.org) / [emergingthreats.net](https://emergingthreats.net) |

### Update Manifest (Generated: 2026-05-13)

| Dataset Name | Description | Size (MB) | Date Pulled |
| :--- | :--- | :--- | :--- |
| Vulnerability Intelligence | Raw archives of NVD, CISA KEV, and threat feeds. | 1848.2 | 2026-05-13 19:38:35 |
| R3KT Refined Models | Embeddings and indices for the Knowledge Graph. | 29.85 | 2026-05-13 19:09:37 |
| DGA_domains_dataset | External cybersecurity dataset archive. | 7.17 | 2026-05-13 18:00:33 |
| attack-data-model | External cybersecurity dataset archive. | 0.6 | 2026-05-13 17:59:22 |
| attack-stix-data | External cybersecurity dataset archive. | 223.58 | 2026-05-13 17:58:52 |
| cti-master | External cybersecurity dataset archive. | 48.49 | 2026-05-13 17:58:24 |
| Security-Datasets | External cybersecurity dataset archive. | 532.96 | 2026-05-11 12:15:44 |
| mssocarchive | External cybersecurity dataset archive. | 513.3 | 2026-05-11 12:14:53 |
| shinyhuntersarchive | External cybersecurity dataset archive. | 397.09 | 2026-05-11 10:40:35 |
| nvdcve-2.0-2026 | External cybersecurity dataset archive. | 8.01 | 2026-05-13 18:02:12 |
| whoisdb-master | External cybersecurity dataset archive. | 0.01 | 2026-05-09 22:28:14 |

All data is for educational and defensive use. Please follow the terms of service for each source when you use this data.

## Usage

The data is provided in JSON and CSV formats to keep it consistent and easy to parse. You can download the full dataset from the releases page. These files are ready to be pulled into a SIEM like Wazuh or used for testing detection rules in a lab environment.

## Future Plans

I am working on an automated pipeline to handle live data ingestion. My next goal is to use the deterministic expert networks I have been building to help organize this data without the noise of traditional AI. I also plan to add documentation for using this data with hardware firewalls like the Raspberry Pi 5.

## License

This collection is shared under the MIT license. This covers the curation and structure of the repository. The underlying data belongs to the original sources listed in the attribution table. I believe that having access to accurate information is the best way to build a strong defense. Use this information responsibly.

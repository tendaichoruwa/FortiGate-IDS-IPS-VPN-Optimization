# 🛡️ FortiGate IDS/IPS & VPN Optimization — Strengthening Network Resilience and Visibility

![FortiGate](https://img.shields.io/badge/FortiGate-NGFW-red)
![VPN](https://img.shields.io/badge/SSL_VPN-MFA-green)
![Security](https://img.shields.io/badge/Security-IDS%2FIPS-blue)
![Efficiency](https://img.shields.io/badge/Tickets-↓80%25-lightgrey)

> **Objective:** Redesign network security infrastructure to enhance visibility, control, and VPN reliability across multiple mining and remote operations.

---

## 📑 Table of Contents
1. [Overview](#overview)
2. [Challenges](#challenges)
3. [Solution Design](#solution-design)
4. [Implementation Highlights](#implementation-highlights)
5. [Results](#results)
6. [Technical Details](#technical-details)
7. [Lessons Learned](#lessons-learned)
8. [Next Steps](#next-steps)
9. [Author](#author)

---

## 🌍 Overview

As part of the infrastructure modernization initiative, the existing firewall and VPN setup required a complete redesign.  
Remote connectivity was unreliable, intrusion alerts were inconsistent, and the lack of centralized visibility made it difficult to track and respond to threats efficiently.

By deploying and tuning **FortiGate IDS/IPS** and optimizing both **SSL VPN** and **IPsec site-to-site tunnels**, the goal was to create a stable, secure, and transparent network backbone that could support high-availability virtual workloads under **vSphere replication**.

---

## ⚠️ Challenges

- **Fragmented visibility** — Multiple sites using different firewall rules and outdated firmware.  
- **Unreliable VPN performance** — Frequent disconnects and inconsistent throughput on legacy SSL VPNs.  
- **Limited intrusion detection** — No real-time correlation or logging beyond basic traffic statistics.  
- **User experience issues** — Authentication challenges and manual reconfiguration during failover events.  

These issues led to frequent helpdesk tickets and reactive rather than proactive security operations.

---

## 🧩 Solution Design

The new design prioritized *security without complexity*, combining Fortinet’s **FortiGate NGFW** features with **vSphere replication** network requirements for continuity.

**Core principles:**
1. Centralized firewall management and consistent policy enforcement  
2. Layered intrusion prevention integrated with real-time monitoring  
3. Resilient VPN architecture with redundancy and MFA enforcement  
4. Automation for configuration, backup, and reporting  

---

## ⚙️ Implementation Highlights

### 🧠 1. FortiGate IDS/IPS Deployment
- Implemented **FortiGate NGFW cluster** with unified firmware across sites  
- Tuned **IDS/IPS signatures** to reduce false positives by 40%  
- Integrated logs into FortiAnalyzer for long-term visibility and SIEM correlation  
- Defined policies for critical subnets and vSphere replication traffic

**Result:** Clear intrusion visibility and 70% reduction in false alarms and threat noise.

---

### 🔐 2. VPN Optimization (SSL & IPsec)
- Rebuilt **SSL VPN profiles** with enforced **MFA (FortiToken Mobile)**  
- Configured **split tunneling** for better bandwidth efficiency  
- Deployed **IPsec tunnels** between production and DR sites with dynamic failover  
- Tuned MTU and DPD intervals for stable throughput under replication workloads  

**Result:** 80% fewer VPN-related tickets and seamless vSphere replication across WAN links.

---

### 📡 3. Performance and Monitoring Enhancements
- Introduced **Zabbix** monitoring for FortiGate CPU/memory and tunnel states  
- Automated backup and log exports with **PowerShell + FortiAPI** scripts  
- Standardized reports for uptime, intrusion trends, and VPN session analytics  

**Result:** Proactive maintenance with real-time visibility and zero unplanned VPN downtime in six months.

---

## 📊 Results

| Metric | Before | After |
|--------|---------|-------|
| Intrusion Attempts | High, unfiltered | **↓ 70%** |
| VPN Incident Tickets | 50+ / quarter | **↓ 80%** |
| Mean Time to Detect | ~2 hours | **Under 15 minutes** |
| vSphere Replication Stability | Inconsistent | **99.9% uptime** |
| Firewall Policy Drift | Manual edits | **Fully standardized** |

---

## 🧰 Technical Details

| Component | Description |
|------------|-------------|
| **Firewall Platform** | FortiGate NGFW Cluster (HA, v7.x) |
| **Monitoring** | FortiAnalyzer + Zabbix |
| **VPN** | SSL VPN (MFA via FortiToken) + IPsec tunnels (IKEv2) |
| **Automation** | PowerShell scripts using FortiAPI & scheduled tasks |
| **Virtualization Backbone** | VMware vSphere Replication |
| **Reporting** | Daily IDS/IPS summaries, VPN uptime reports, SIEM integration |

---

## 💡 Lessons Learned

- **Tuning beats defaults.** IDS/IPS accuracy depends heavily on tuning signatures to your environment.  
- **Visibility builds confidence.** When operations can *see* real-time activity, support tickets drop naturally.  
- **User-centric security scales.** MFA and clear VPN policies improved both security posture and user satisfaction.  
- **Automation keeps compliance honest.** Scheduled configuration backups and API-driven reports reduce drift and audit pain.

---

## 🔭 Next Steps

- Deploy **FortiAnalyzer Cloud** for cross-site analytics  
- Integrate **Sentinel SIEM** for unified SOC visibility  
- Expand **Zero-Trust VPN** (ZTNA) for remote teams  
- Create Power BI dashboards for security KPI visualization  

---

## 👤 Author

**Tendai Choruwa**  
Senior Infrastructure & Cloud Architect  
🔗 [linkedin.com/in/tendaichoruwa](https://www.linkedin.com/in/tendaichoruwa)  
💻 [github.com/tendaichoruwa](https://github.com/tendaichoruwa)

---

## 🧱 Repository Details

This work forms part of the  
👉 [**tendaichoruwa/vSphere-Replication**](https://github.com/tendaichoruwa/vSphere-Replication)  
initiative to ensure secure, stable, and replicable hybrid infrastructure environments.

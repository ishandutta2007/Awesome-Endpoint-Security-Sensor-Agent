# Awesome-Endpoint-Security-Sensor-Agent

# Awesome-Endpoint-Security-Sensor-Agent
**Top Endpoint Security Sensor Agent (Opensource) 🌟 Star if you like it! 🌟**

**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on Lightweight Telemetry, Kernel-Level Visibility, Fleet Management & Self-Hosted Agents*
**Last updated: November 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Endpoint Security Sensor & Agent**. These tools are the software installed on endpoints—laptops, servers, and cloud workloads—that collect telemetry, detect threats, and enforce policy. The category spans full EDR agents with kernel drivers to lightweight telemetry shippers, and the open-source landscape offers viable alternatives for teams wanting control over their sensor code and data pipeline.

**Examples** include CrowdStrike Falcon Agent, SentinelOne Agent, Microsoft Defender for Endpoint, Carbon Black Sensor, Tanium Client, Trellix Agent, Sophos Agent, Datadog Agent, Cybereason Sensor, and Elastic Agent (the category leaders in commercial space).

**Open-source emphasis**: This section is expanded with every relevant project for self-hosted endpoint sensors, telemetry collection, and open agent infrastructure. **Critical note**: Open-source endpoint agents fall into two camps—**security-focused agents** (Wazuh, Velociraptor, OpenEDR) that detect and respond to threats, and **observability-focused agents** (Elastic Agent, Grafana Alloy, OpenTelemetry Collector) that ship telemetry for monitoring. Neither category fully replaces a commercial EDR agent's kernel-level prevention, but for detection, compliance, and telemetry, the open-source options are production-proven.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **CrowdStrike Falcon Agent**
  **Lightweight endpoint sensor** with kernel-level visibility and threat graph. **Pricing**: **Falcon Go $59.99/device/month** (billed annually, 100-device max); **Pro $99.99/device/month**; **Enterprise $184.99/device/month** . **Free tier**: Falcon Go includes core EDR for up to 100 devices. **Best for**: enterprises wanting the most mature detection with minimal agent footprint—**trade-off**: premium pricing; per-device costs scale with fleet size. **Supported OS**: Windows (including legacy XP/2003 via Falcon for Legacy Systems), Linux (RHEL, Ubuntu, SLES, Amazon Linux, ARM64), macOS (Sonoma through Golden Gate 27), ChromeOS (agentless, event ingestion) .

- **SentinelOne Agent**
  **Autonomous EDR agent** with AI-driven prevention and response. **Pricing**: **Singularity Complete $179.99/endpoint/year** (AI-driven endpoint and cloud workload protection, 14-day data retention); **Commercial $229.99/endpoint/year** (adds identity detection, 90-day retention, managed threat hunting); **Enterprise** quote-only . **Free tier**: None. **Best for**: organizations wanting autonomous response—**trade-off**: agent resource usage varies by workload. **Supported OS**: Windows (Server 2012 R2 through 2025, Windows 10/11 including 365), Linux (RHEL, Ubuntu, Debian, SLES, Amazon Linux, ARM64 Graviton), macOS .

- **Microsoft Defender for Endpoint**
  **EDR agent** integrated with Microsoft 365 and Defender XDR. **Pricing**: **Plan 1** included in M365 E3; **Plan 2** included in M365 E5 or via **E5 Security add-on $12/user/month list** (median negotiated $8–$10, top quartile $6–$8) . **Free tier**: Limited trial. **Best for**: Microsoft-centric organizations wanting native integration—**trade-off**: persona-based licensing is complex; flat Plan 2 coverage is a common overspend . **Supported OS**: Windows, macOS, Linux (server-focused), Android, iOS.

- **Carbon Black Sensor** (Broadcom)
  **Enterprise EDR sensor** with behavioral detection. **Pricing**: Quote-only; **3-year commitments** preferred with **5–10% additional discount** . **Free tier**: None. **Best for**: organizations with existing Broadcom relationships—**trade-off**: **42% of 2024–2026 renewals resulted in partial or full migration**; 3-year license totals frequently **25–40% higher** than Falcon, SentinelOne, or Defender at equivalent scope . **Supported OS**: Windows, macOS, Linux.

- **Tanium Client**
  **Unified endpoint management and security agent** with real-time visibility. **Pricing**: **Microsoft Marketplace: $12,000/month for 1,500 endpoints** ($144,000/year) for Tanium Core Plus, Endpoint Management Plus, Risk & Compliance Plus, and Incident Response . **Free tier**: None. **Best for**: large enterprises wanting a single agent for management and security—**trade-off**: six-figure entry for modest fleets; annual subscription. **Supported OS**: Windows, macOS, Linux .

- **Trellix Endpoint Security Agent**
  **Enterprise endpoint security agent** (formerly McAfee/FireEye). **Pricing**: Quote-only. **Free tier**: None. **Best for**: enterprises with existing Trellix investments.

- **Sophos Endpoint Agent**
  **Endpoint protection agent** with Intercept X. **Pricing**: Quote-only. **Free tier**: Trial available. **Best for**: mid-market organizations wanting integrated endpoint security.

- **Datadog Agent**
  **Observability agent** for metrics, logs, and traces. **Pricing**: Consumption-based; no per-agent fee. **Free tier**: Limited. **Best for**: teams wanting telemetry alongside security—**trade-off**: not a security agent; no threat detection. **Supported OS**: Linux, Windows, macOS .

- **Cybereason Sensor**
  **EDR sensor** with behavioral detection. **Pricing**: Quote-only. **Free tier**: None. **Best for**: SOC teams wanting MITRE ATT&CK coverage.

- **Elastic Agent**
  **Unified telemetry shipper** for Elastic Security and Observability. **Pricing**: Free (open source); Elastic Cloud consumption-based. **Free tier**: Yes, self-managed. **Best for**: teams wanting a single agent for logs, metrics, and security data—**trade-off**: not a prevention agent; detection relies on SIEM rules. **Supported OS**: Linux (x86_64, aarch64), Windows, macOS .

## Open-Source GitHub Projects

- **Wazuh Agent**
  **Open-source security agent** (GPLv2) — **the most complete open-source endpoint security agent**, part of the Wazuh SIEM/EDR platform. **Features**: **File integrity monitoring** (FIM); **log analysis** and **rootkit detection**; **vulnerability detection**; **security configuration assessment** (CIS, PCI DSS, HIPAA, NIST); **active response**—firewall-drop, host-deny, disable-account; **MITRE ATT&CK mapping**; container security for Docker and Kubernetes. **Tech stack**: C, Python. **Deploy**: Self-hosted (agent on endpoints, manager server). **Trade-off**: **No kernel-level prevention**—detection is log-based; requires manager infrastructure. **Best for**: organizations wanting a free, comprehensive endpoint agent with compliance mapping—especially those already running Wazuh SIEM.

- **Velociraptor Agent**
  **Endpoint visibility and DFIR agent** (Apache 2.0) — **the most powerful open-source agent for threat hunting and forensics at scale**. **Features**: **VQL (Velociraptor Query Language)** for interrogating endpoints; **real-time monitoring** for process execution, network connections, and bash instrumentation; **hunts across thousands of endpoints** in minutes; **offline collectors** for field forensics; **low resource consumption**. **Tech stack**: Go. **Deploy**: Self-hosted (server + agents). **Trade-off**: **Not continuous EDR**—no real-time prevention; requires VQL expertise. **Best for**: DFIR teams and threat hunters wanting deep endpoint interrogation without commercial EDR licensing.

- **OpenEDR Agent**
  **Open-source EDR agent** (open source, Xcitium) — **the most dedicated open-source EDR codebase**. **Features**: **Analytic detection with MITRE ATT&CK visibility**; event correlation and root cause analysis; real-time detection; **fully open source**—inspect, audit, and improve. **Tech stack**: Per repository. **Deploy**: Self-hosted. **Trade-off**: **Limited independent validation**—claims are vendor-reported; smaller community than Wazuh or Velociraptor. **Best for**: organizations wanting a dedicated open-source EDR agent to evaluate or contribute to.

- **Elastic Agent (Open Source)**
  **Unified telemetry shipper** (Elastic License 2.0/SSPL) — **the most capable open-source observability agent**, usable for security telemetry collection. **Features**: **Single agent for logs, metrics, and traces**; **Elastic Defend** integration for endpoint protection (paid tier); **OpenTelemetry Collector binary included**; **fleet management** for centralized policy. **Tech stack**: Go. **Deploy**: Self-hosted or Elastic Cloud. **Trade-off**: **Source-available, not OSI open source**—Elastic License 2.0/SSPL restrictions apply; **Elastic Defend** requires paid tier. **Best for**: teams already on Elastic Stack wanting a single agent for observability and security data.

### Additional Strong Open-Source Options

- **Grafana Alloy** — OpenTelemetry Collector distribution (Apache 2.0). Vendor-neutral telemetry agent for metrics, logs, and traces. **Note**: **Observability agent, not security**—no threat detection. **Best for**: teams wanting a vendor-neutral telemetry shipper.
- **OpenTelemetry Collector** — Vendor-neutral telemetry pipeline (Apache 2.0). The standard for collecting and exporting telemetry. **Note**: **Building block, not a security agent**—you configure receivers, processors, and exporters. **Best for**: organizations building custom telemetry pipelines.
- **OSQuery** — SQL-powered endpoint visibility agent (Apache 2.0). Query endpoints like a database for compliance and threat hunting. **Note**: **Visibility only**—no prevention or real-time detection. **Best for**: security teams wanting SQL-based endpoint interrogation.

**Frameworks for building custom systems**: Combine **Wazuh Agent** for detection and compliance with **Velociraptor Agent** for DFIR and hunting, and **OpenTelemetry Collector** for telemetry shipping—creating a layered open-source endpoint agent stack. **None of these match CrowdStrike's kernel-level prevention or SentinelOne's autonomous response**, but for detection, investigation, and telemetry, the options are production-capable.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Endpoint agents handling system telemetry must comply with data protection regulations (GDPR, CCPA, etc.) and implement appropriate access controls for collected data.
- **The "prevention agent" vs. "detection agent" vs. "telemetry shipper" distinction is critical.** **CrowdStrike, SentinelOne, Defender, and Carbon Black** are **prevention agents**—they block threats at the kernel level . **Wazuh, OpenEDR, and Velociraptor** are **detection/investigation agents**—they collect and analyze, but do not prevent execution . **Datadog Agent, Elastic Agent, Grafana Alloy, and OpenTelemetry Collector** are **telemetry shippers**—they collect observability data, not security events . **Choose based on whether you need prevention, detection, or observability.**
- **Carbon Black's migration risk is material.** 42% of 2024–2026 renewals resulted in partial or full migration; 3-year license totals are 25–40% higher than competitors . **If evaluating Carbon Black, run an RFP with credible alternatives—even staying, you save 10–15 points** .
- **Microsoft Defender's persona-based licensing is a trap.** Flat Plan 2 coverage across all users is the most common overspend; persona-aligned mixes cut the Defender line **20–30%** . **License Plan 2 only for privileged users, developers, executives, and high-risk roles.**
- **Tanium's entry price is six figures.** **$144,000/year for 1,500 endpoints** . **Do not evaluate without enterprise budget approval.**
- **CrowdStrike Falcon Go is the most accessible commercial entry point**—$59.99/device/month, 100-device max, includes core EDR . **Pro and Enterprise add features but quadruple the per-device cost** .
- **Wazuh Agent is the most complete open-source security agent**—FIM, vulnerability detection, active response, and compliance mapping . **The trade-off**: no kernel-level prevention; requires manager infrastructure.
- **Velociraptor Agent is unmatched for DFIR**—VQL hunts across thousands of endpoints in minutes . **The trade-off**: not continuous EDR; requires expertise.
- Self-hosted open-source solutions require proper infrastructure (manager servers, fleet management), security hardening, and ongoing maintenance. **Endpoint agents have deep system visibility**—ensure your deployment meets your organization's security and privacy requirements before installing on production endpoints.

---

**Made for security engineers, IT operations teams, and organizations building transparent endpoint agent solutions.**
Let's make Endpoint Security Sensor & Agents more open, data-driven, and telemetry-aware.

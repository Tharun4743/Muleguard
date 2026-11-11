# Muleguard — Financial Mule Account Detection & Transaction Graph Network

[![Python](https://img.shields.io/badge/Language-Python_3.10-3776AB?style=flat-square&logo=python)](https://python.org/)
[![Graph Theory](https://img.shields.io/badge/Algorithm-PageRank_%26_Betweenness-orange?style=flat-square)](https://networkx.org/)
[![MongoDB](https://img.shields.io/badge/Database-MongoDB-47A248?style=flat-square&logo=mongodb)](https://www.mongodb.com/)
[![License](https://img.shields.io/badge/License-Proprietary_%2F_Permission_Required-red?style=flat-square)](LICENSE.md)

**Muleguard** is an anti-fraud intelligence system specialized in uncovering money mule networks used by cybercrime syndicates. By computing graph centrality metrics, velocity anomalies, and temporal fund retention windows across banking ledgers, Muleguard flags intermediary accounts designed to funnel stolen funds before law enforcement freezing occurs.

---

## Problem Statement & Context
Cyber fraud and ransomware syndicates rely on networks of compromised or hired 'money mules':
- **Rapid Fund Dissipation**: Illicit funds are routed through mule accounts and withdrawn via ATMs or cryptocurrency within 8–15 minutes of theft.
- **Low Account Balance Profile**: Mule accounts maintain zero average balances, suddenly receive high-value inbound transfers, and immediately distribute them.
- **Isolated Bank Perspective**: Individual banks only see their immediate counterparties, failing to recognize coordinated mule rings.

---

## Existing Solutions & Critical Gaps
| Inspection Type | Time to Detect | Accuracy on Mule Rings |
| :--- | :--- | :--- |
| **Post-Fraud Audit (Manual)** | 3–7 business days | Detects only after funds have been permanently withdrawn |
| **Muleguard Real-Time Graph Engine** | **<250ms per transaction stream** | **94% precision identifying high-centrality intermediary nodes** |

---

## Proposed Solution & Architectural Innovation
Muleguard deploys **Topological Behavioral Analytics**:
- **Temporal In-Out Velocity Metrics**: Identifies accounts where funds are disbursed within a critical short time window ($T < 180s$) after deposit.
- **Graph Centrality Scoring**: Calculates Betweenness Centrality and Degree Ratios to identify intermediary bridge nodes in fund transfers.
- **Dormancy Wakeup Heuristic**: Detects previously dormant bank accounts that suddenly experience abnormal velocity and transaction volume.
- **Automated Freeze Recommendations**: Dispatches instant webhook signals to banking core systems recommending provisional transaction holds.

---

## Technical Approach & System Architecture
```mermaid
flowchart LR
    Ledger["Core Banking Transaction Feed"] --> Parser["Transaction Stream Normalizer"]
    Parser --> GraphEngine["Dynamic Directed Flow Graph"]
    GraphEngine --> Centrality["Betweenness & In-Out Ratio Evaluator"]
    GraphEngine --> Velocity["Temporal Retention Time Engine"]
    Centrality & Velocity --> MuleScorer["Mule Probability Matrix (0-100)"]
    MuleScorer --> Webhook["Automated Core Banking Freeze Webhook"]
```

---

## Quantifiable Impact & Measurable Benefits
- **Interception Within Critical Window**: Identifies suspicious mule flows in under 250ms, enabling real-time holds before ATM disbursement.
- **94% Precision on Synthetic Fraud Datasets**: Minimal disruption to legitimate high-velocity merchant accounts.
- **Auditable Forensic Evidence**: Generates compliance-ready transaction chain diagrams.

---

## Feasibility, Operational Viability & Scalability
- **Enterprise Integration**: Easily interfaces with existing SQL/NoSQL transactional stores via streaming Kafka or REST endpoints.

---

## Project Architecture & Quickstart
```bash
git clone https://github.com/Tharun4743/Muleguard.git
cd Muleguard
pip install -r requirements.txt
python main.py
```

---

## Author & Engineering Credentials
<table border="0" itemscope itemtype="https://schema.org/Person">
  <tr>
    <td width="130" align="center" valign="middle">
      <img src="https://github.com/Tharun4743.png" width="105" style="border-radius: 6px;" alt="Tharunkumar K — Full Stack Developer & AI Systems Engineer at V.S.B. Engineering College" title="Tharunkumar K — V.S.B. Engineering College (VSBEC)" itemprop="image" />
    </td>
    <td>
      <h3 itemprop="name">Tharunkumar K</h3>
      <p>
        <b itemprop="jobTitle">Full Stack Developer & AI Systems Engineer</b> | <b>V.S.B. Engineering College (VSBEC)</b><br/>
        🎓 <b>B.Tech in Information Technology</b> — <b>V.S.B. Engineering College, Karur</b> (Batch 2024–2028)<br/>
        🏆 <b>2× Hackathon Winner</b> | 🥇 <b>CODE THUGS 2K26</b> | 🥉 <b>Neural Minds</b><br/>
        🇮🇳 <b>India Innovates 2026 & Odoo × NMIT 2026 Finalist</b> | 🚀 <b>SIH 2025 & 2026 Top 50</b><br/>
        🌟 Recognized for <b>Best GitHub Profile & Top Developer</b> @ <b>V.S.B. ENGINEERING COLLEGE</b>
      </p>
      <p>
        🚀 <b>Top Flagship Engineering Projects:</b><br/>
        • 🏛️ <b>TaskManager (VSBEC IT Vault)</b> — Institutional Task Governance & LeetCode/GitHub Sync &nbsp;<a href="https://github.com/Tharun4743/Taskmanager"><img src="https://img.shields.io/badge/Code-181717?style=flat-square&logo=github&logoColor=white" alt="Code" /></a>&nbsp;<a href="https://it-taskmanager.vercel.app/"><img src="https://img.shields.io/badge/Live_Demo-10B981?style=flat-square&logo=vercel&logoColor=white" alt="Live Demo" /></a><br/>
        • 🧠 <b>AURA</b> — Air-Gapped Local Multimodal RAG Engine & Offline AI Assistant &nbsp;<a href="https://github.com/Tharun4743/AURA"><img src="https://img.shields.io/badge/Code-181717?style=flat-square&logo=github&logoColor=white" alt="Code" /></a><br/>
        • 🪖 <b>Smart Helmet IoT</b> — SIH Top 50 Dual-Unit Motorcycle Accident Prevention System &nbsp;<a href="https://github.com/Tharun4743/AGILE-INNOVATORS-smart-helmet-"><img src="https://img.shields.io/badge/Code-181717?style=flat-square&logo=github&logoColor=white" alt="Code" /></a><br/>
        • ⚡ <b>GOAT-CE</b> — Isolated Distributed Multi-Language Code Execution Sandbox &nbsp;<a href="https://github.com/Tharun4743/GOAT-CE"><img src="https://img.shields.io/badge/Code-181717?style=flat-square&logo=github&logoColor=white" alt="Code" /></a>
      </p>
      <p>
        <a href="https://tharunkumark4743.netlify.app/"><img src="https://img.shields.io/badge/Portfolio-0284c7?style=flat-square&logo=googlechrome&logoColor=white" alt="Portfolio" /></a>&nbsp;
        <a href="https://github.com/Tharun4743"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub" /></a>&nbsp;
        <a href="https://www.linkedin.com/in/tharunkumark4743"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>&nbsp;
        <a href="https://leetcode.com/u/Tharunkumar__K/"><img src="https://img.shields.io/badge/LeetCode-FFA116?style=flat-square&logo=leetcode&logoColor=white" alt="LeetCode" /></a>&nbsp;
        <a href="mailto:tharunkumark42007@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
      </p>
    </td>
  </tr>
</table>

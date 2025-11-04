# 🧩 Process Change Impact Automation (PCIA)

## 📘 Overview
**Process Change Impact Automation (PCIA)** is a demo-level tool designed and developed to meet **personal and professional needs** arising from day-to-day challenges in SDLC environments — particularly those involving **frequent process updates**, **permission changes**, and **compliance documentation**.

The main goal is to build a reusable framework that automatically captures and documents **rule**, **control**, and **permission** changes during deployments, bridging the gap between **Business Analysis**, **Change Management**, and **Technical Documentation**.

---

## 🎯 Objective
To design and demonstrate an intelligent automation framework that:
1. Logs all process-related changes (rules, permissions, controls, and new functionalities).  
2. Performs automatic **Change Impact Analysis** within Jira.  
3. Creates or updates **Usage Guide pages** in Confluence automatically.  
4. Documents **permission/role changes** for audit and traceability.  
5. Addresses real-world documentation gaps in the **Software Development Life Cycle (SDLC)**.

---

## 💡 Motivation
This tool is being developed as a **personal initiative** — a practical response to the documentation and change-tracking challenges experienced in real-life enterprise environments.

The intention is to create a prototype that:
- Reflects the documentation needs observed across **CRM**, **Core Banking**, and **Insurance** systems.  
- Demonstrates how automation can keep SDLC documentation continuously synchronized.  
- Serves as an open demo for other professionals who face similar difficulties managing constant process evolution.  

Ultimately, PCIA aims to cover SDLC requirements related to:
- Change impact visibility  
- Role and permission traceability  
- End-user documentation governance  
- Continuous improvement and audit readiness  

---

## ⚙️ Key Features
| # | Feature | Description |
|---|----------|-------------|
| 1 | **Automated Confluence Page Generation** | A new Confluence page is created automatically when a Jira “Process Change” issue is deployed. |
| 2 | **Impact Analysis Fields** | Jira custom fields capture affected processes, rules, and actors. |
| 3 | **Permission Change Table** | Before/after permission details are inserted automatically into the generated page. |
| 4 | **Traceability Links** | Every Jira issue links directly to its corresponding Confluence guide. |
| 5 | **Notifications** | Alerts notify impacted users or teams when a new guide is published. |
| 6 | **Version Control & Audit Trail** | Confluence manages revision history for compliance and governance. |
| 7 | **Optional Power BI Connector** | ETL script exports change logs for data visualization and trend analysis. |

---

## 🧠 Business Value
- Ensures **regulatory and audit compliance** through transparent change tracking.  
- Reduces **manual documentation effort** and errors.  
- Keeps **operational guides and permissions up to date** after every deployment.  
- Strengthens alignment between **Business Analysts**, **Developers**, and **Operations teams**.  
- Creates a living **SDLC documentation ecosystem** that evolves with the system.

---

## 🏗 Architecture Overview
┌─────────────────────┐
│ Jira Cloud │
│ Issue Type: Change │
└─────────┬───────────┘
│
│ Automation Trigger (on “Deployed”)
▼
┌────────────────────────┐
│ Confluence Cloud │
│ Template: Usage Guide │
│ Auto-Update via REST │
└─────────┬──────────────┘
│
▼
┌────────────────────────┐
│ Power BI / Dashboard │
│ Trend Analysis (ETL) │
└────────────────────────┘

---

## 🧩 Technology Stack
| Component | Technology | Purpose |
|------------|-------------|----------|
| **Jira Cloud** | Custom Issue Type + Automation Rules | Change capture and triggers |
| **Confluence Cloud** | Page Templates + REST API | Documentation and publishing |
| **Atlassian Forge SDK** | Plugin logic / custom integration | Extended automation |
| **Python or Node.js** | ETL scripts for dashboards | Export and analytics |
| **Power BI** | Visualization | SDLC trend and audit tracking |
| **GitHub** | Repository | Version control & knowledge sharing |

---

## 📁 Repository Structure
📦 process-change-impact-automation
┣ 📜 README.md
┣ 📂 docs
┃ ┣ BRD.md
┃ ┣ FRD.md
┃ ┣ UseCases.md
┃ ┗ ArchitectureDiagram.png
┣ 📂 templates
┃ ┗ ConfluenceTemplate.md
┣ 📂 automation-scripts
┃ ┗ jira-confluence-automation.json
┗ 📂 demo-data
┗ sample-jira-issues.csv


---

## 🚀 Getting Started (Demo)
1. **Create a “Process Change” issue type in Jira.**  
2. **Add custom fields** for Process Name, Change Type, and Roles Affected.  
3. **Configure an Automation Rule:**  
   - Trigger: When status = “Deployed”.  
   - Action: Create a Confluence page using a pre-defined template.  
4. **Customize the Confluence Template** (found in `/templates/ConfluenceTemplate.md`).  
5. (Optional) **Run the ETL Script** to export and visualize change logs.

---

## 📊 Example Use Case
> **Scenario:** During a CRM deployment, a new field “Risk Exposure Category” is added.  
>  
> **Flow:**  
> 1. Jira issue CHG-2025-1104 is logged with change details.  
> 2. When deployed, automation triggers Confluence update.  
> 3. A new “Usage Guide” page is generated with:  
>    - Rule and permission details,  
>    - Impact summary,  
>    - Linked Jira issue.  
> 4. Notification is sent to relevant operational teams.

---

## 🧭 Roadmap
- [ ] Prototype the Jira → Confluence automation workflow.  
- [ ] Add version comparison for permission tables.  
- [ ] Build ETL for Power BI visualizations.  
- [ ] Extend to a full Forge plugin with UI.  
- [ ] Publish project demo and video walkthrough.

---

## 🧑‍💻 Author
Developed by **Robotiyee** — a personal SDLC-driven initiative with conceptual and documentation assistance from **ChatGPT (GPT-5)**.  
The project aims to demonstrate how automation can simplify documentation and compliance management across dynamic enterprise systems.

---

## 🪪 License
MIT License — free for educational and demonstration purposes.  
Atlassian® Jira and Confluence® are trademarks of Atlassian Pty Ltd.


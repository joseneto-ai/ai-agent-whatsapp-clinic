# 🤖 AI WhatsApp Agent — Premium Clinic Automation

> An LLM-powered conversational agent that handles patient triage,
> lead qualification, and appointment scheduling autonomously via
> WhatsApp — ensuring zero leads are lost and 24/7 clinic coverage
> without human dependency.

---

## 📌 The Problem

Premium healthcare and aesthetic clinics face a critical operational gap:

- **reception operates 8–10 hours/day** while patient inquiries arrive 24/7
- **high-intent leads abandon** when they don't receive an immediate response
- **front-desk staff waste 60–70% of their time** on repetitive triage 
  and scheduling tasks instead of in-clinic VIP care
- **no lead scoring system** — staff treat urgent surgical inquiries and
  casual questions with the same priority

The result: lost revenue, degraded patient experience, and burned human capital.

---

## ✅ The Solution

A fully autonomous AI agent deployed over WhatsApp that acts as a 
24/7 intelligent digital concierge — triaging patients, qualifying leads, 
collecting intake data, and routing high-intent contacts to the clinical team.


**Key capabilities:**
- Instant response to any incoming message, at any hour
- Intelligent triage separating high-intent patients from casual inquiries
- Automated appointment scheduling integrated with clinic calendar
- Contextual conversation memory across the entire patient interaction
- Seamless handoff to human staff for complex or urgent cases

---

## 🏗️ System Architecture
````
Patient (WhatsApp)
       │
       ▼
[WhatsApp Business API]
       │
       ▼
[n8n Webhook Trigger] ──── receives incoming message
       │
       ▼
[Context Manager] ──────── retrieves conversation history
       │
       ▼
[LLM Triage Engine] ─────── classifies intent & urgency
   (OpenAI GPT-4o)          └─ HIGH INTENT → priority queue
                             └─ LOW INTENT  → nurture flow
                             └─ URGENT      → instant staff alert
       │
       ▼
[Response Generator] ────── crafts personalized reply
       │
       ▼
[WhatsApp Business API] ─── delivers response to patient
       │
       ▼
[CRM Logger] ────────────── logs interaction + lead score
````

*Full architecture diagram: [`architecture/flow-diagram.md`](./architecture/flow-diagram.md)*

---

## ⚙️ Tech Stack

| Layer | Technology |
|---|---|
| Automation Orchestration | n8n (self-hosted) |
| AI Engine | OpenAI GPT-4o via API |
| Messaging Channel | WhatsApp Business API (Meta) |
| Backend Logic | Python · Node.js |
| Data Persistence | JSON context store / CRM webhook |
| Infrastructure | Cloud VPS · Linux |

---

## 📁 Repository Structure
````
ai-agent-whatsapp-clinic/
├── README.md                  # Project overview (this file)
├── docs/
│   └── business-case.md       # Problem, solution & measured outcomes
├── architecture/
│   └── flow-diagram.md        # Full system architecture breakdown
├── prompts/
│   └── triage-agent.md        # LLM system prompt (sanitized)
└── n8n-workflows/
    └── main-flow.json         # n8n workflow export (importable)
````

---

## 📊 Business Outcomes

| Metric | Before | After |
|---|---|---|
| Response time (off-hours) | 8–14 hours | < 90 seconds |
| Lead capture rate (off-hours) | ~30% | ~95% |
| Staff time on triage tasks | ~65% of shift | < 15% |
| Missed appointment follow-ups | Frequent | Zero (automated) |

---

## 🔐 Privacy & Compliance

- Patient data handled in compliance with **LGPD** (Brazilian data protection law)
- No sensitive medical data stored in plain text
- Conversation logs encrypted at rest
- Human escalation protocol for any clinical decision

---

## 📂 Explore the Project

- 📄 [Business Case & ROI Analysis](./docs/business-case.md)
- 🏗️ [Architecture Deep Dive](./architecture/flow-diagram.md)
- 🧠 [AI Triage Agent Prompt](./prompts/triage-agent.md)
- ⚙️ [n8n Workflow Export](./n8n-workflows/main-flow.json)

---

## 👤 Author

**José Neto** — AI Automation Engineer & Founder @zNeto.AI

[![LinkedIn](https://img.shields.io/badge/LinkedIn-José%20Neto-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/jos%C3%A9-neto-b88558398)
[![GitHub](https://img.shields.io/badge/GitHub-joseneto--ai-181717?style=flat&logo=github)](https://github.com/joseneto-ai)

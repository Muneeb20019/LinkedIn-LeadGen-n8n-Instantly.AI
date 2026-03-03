# 🚀 Agentic-AI-Autopilot: LinkedIn Lead-Gen & Warm Outreach

![n8n](https://img.shields.io/badge/Workflow-n8n-FF6C37?style=flat&logo=n8n&logoColor=white)
![Apify](https://img.shields.io/badge/Scraping-Apify-97ca00?style=flat&logo=apify&logoColor=white)
![Instantly](https://img.shields.io/badge/Outreach-Instantly.ai-blue?style=flat)
![GHL](https://img.shields.io/badge/CRM-GoHighLevel-2563eb?style=flat)
![Pinecone](https://img.shields.io/badge/VectorDB-Pinecone-000000?style=flat&logo=pinecone&logoColor=white)

---

## 🚀 Project Overview
This project is an **End-to-End Autonomous Sales Intelligence Pipeline**. It manages the full B2B sales cycle by scraping high-intent leads from LinkedIn via **Apify**, enriching them with AI-generated icebreakers, and pushing them into **Instantly.ai** for high-deliverability warm email campaigns. 

The system acts as a digital SDR, using **RAG-powered negotiation** to handle replies and **GoHighLevel** to manage the final CRM stages.

---

## 📝 The Workflow Lifecycle

### 1️⃣ Lead Extraction & Verification
The process begins with **Apify LinkedIn Scrapers** to extract targets based on specific job titles and industries. I implemented a cleaning layer that normalizes company names and performs real-time email verification before data persistence.

<div align="center">
  <img src="https://raw.githubusercontent.com/Muneeb20019/LinkedIn-LeadGen-n8n-Instantly.AI/main/(1)%20LinkedIn%20lead%20generation.png" width="100%" alt="LinkedIn Scraping"/>
</div>

### 2️⃣ Agentic Personalization (Icebreakers)
For every verified lead, an **AI Agent (GPT-4o)** generates a hyper-personalized icebreaker based on their profile data. This information is then synced with **Instantly.ai** to trigger the warm outreach campaign.

<div align="center">
  <img src="https://raw.githubusercontent.com/Muneeb20019/LinkedIn-LeadGen-n8n-Instantly.AI/main/2%20personalized%20icebreaker.png" width="100%" alt="Personalization Phase"/>
</div>

### 3️⃣ AI SDR Brain (Negotiation & RAG)
When a prospect replies, the **AI SDR Agent** takes over. It utilizes **Pinecone Vector Store** for Retrieval-Augmented Generation (RAG) to provide factually accurate answers about company services and book discovery calls.

<div align="center">
  <img src="https://raw.githubusercontent.com/Muneeb20019/LinkedIn-LeadGen-n8n-Instantly.AI/main/3%20AI%20Sdr%20Agent.png" width="100%" alt="AI SDR Agent"/>
</div>

### 4️⃣ Persistence & Follow-up Tracking
Every interaction is logged into a centralized **Persistence Layer**. This node manages the state of each lead, identifying which prospects are active and which require a transition to the follow-up sequence.

<div align="center">
  <img src="https://raw.githubusercontent.com/Muneeb20019/LinkedIn-LeadGen-n8n-Instantly.AI/main/4%20Add%20to%20follow%20up%20sheet.png" width="100%" alt="Follow-up Sheet Logic"/>
</div>

### 5️⃣ Warm Follow-up Agent
If a lead goes cold, the **Warm Follow-up Agent** triggers. It analyzes the previous conversation history and generates a context-aware nudge to restart the conversation, ensuring a 100% closed-loop sales process.

<div align="center">
  <img src="https://raw.githubusercontent.com/Muneeb20019/LinkedIn-LeadGen-n8n-Instantly.AI/main/5%20Warm%20follow%20up%20agent.png" width="100%" alt="Follow-up Agent"/>
</div>

### 6️⃣ Intent Classification & HITL Notifications
Finally, the system classifies lead intent. If a lead is "Disqualified" or "Unsubscribed," the system triggers a **Notification Node** to update the CRM and alert the admin, preserving sender reputation and saving human time.

<div align="center">
  <img src="https://raw.githubusercontent.com/Muneeb20019/LinkedIn-LeadGen-n8n-Instantly.AI/main/6%20disqualified%20lead%20notification.png" width="100%" alt="Notification Logic"/>
</div>

---

## ✨ Advanced Features (Production Grade)
- **🛡️ DNR Detection:** Autonomous filtering of "Out of Office" and "Unsubscribe" intents to protect email deliverability.
- **⚡ Async Polling:** Recursive loops for status verification and data enrichment.
- **🏷️ Automated Tagging:** AI-driven classification of leads into "Qualified," "Interested," or "General Inquiry" for CRM mapping.

---

## 🛠️ Technical Stack
| Layer | Technology |
| :--- | :--- |
| **🔄 Automation** | n8n Orchestration |
| **🔎 Ingestion** | **Apify** (LinkedIn Scrapers) |
| **🧠 Intelligence** | OpenAI GPT-4o & GPT-4o-mini |
| **📧 Outreach** | **Instantly.ai** |
| **🗄️ Vector DB** | **Pinecone** (RAG) |
| **📊 CRM** | **GoHighLevel** |

---

## ✍️ Author
**Muneeb Ali Khan**
- **GitHub:** [@Muneeb20019](https://github.com/Muneeb20019)
- **LinkedIn:** [Muneeb Ali Khan](https://www.linkedin.com/in/muneeb-ali-khan-2a1675365)

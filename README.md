# 🤖 Smart Support Triage (AI-Powered n8n Automation)

**Smart Support Triage** is an intelligent automation system built with [n8n](https://n8n.io/) that leverages AI to classify, score, and route incoming support messages. It assesses message complexity, assigns categories (Billing, Account, Bug, etc.), and decides whether to create a **Jira ticket**, post a **Slack** alert, or send an **email** summary—while logging every event to **Google Sheets** (or **PostgreSQL** in the advanced version).

> This project showcases real-world **AI + workflow orchestration** patterns used by Applied AI and Automation teams to cut manual triage and boost response times.

---

## 🔑 Key Features

🔍 **AI-Powered Categorization**  
  Classifies messages (e.g., Billing, Account, Bug) and extracts key entities.

🧮 **Complexity Scoring**  
  Applies rules and/or an LLM to assign a score and prioritize escalation.

🚦 **Automated Routing**  
  - High complexity → **Create Jira ticket**  
  - Medium complexity → **Notify Slack channel**  
  - Low complexity → **Email summary only**

🗂️ **Centralized Logging**  
  Logs every triaged message to **Google Sheets** (V1) or **PostgreSQL** (advanced).

🧰 **Modular & Extensible**  
  Separates steps (classification, scoring, routing, logging) for easy upgrades (RAG, Docker, CI/CD).

## 🧠 Glossary (Plain English)

- **Webhook**: A URL that receives data (JSON) when another system “pushes” it—like a doorbell that rings with new info.  
- **LLM (Large Language Model)**: An AI that understands and generates text (OpenAI, Claude, local models via Ollama).  
- **Vector DB & RAG (future)**: Store docs as vectors (numbers). At runtime, retrieve relevant chunks and give them to the LLM for more accurate answers (**R**etrieval-**A**ugmented **G**eneration).  
- **Docker (future)**: Package everything into a portable container that runs anywhere with one command.  
- **Kubernetes (future)**: Orchestrates many containers on servers (scale, restart, monitor).

---

## 🧰 Tech Stack

| Layer | Tools / Services | Purpose |
|------|-------------------|---------|
| Automation | **n8n** | Orchestration & workflow engine |
| AI / LLM | **OpenAI** or **Ollama** (local) | Classification, entity extraction, reasoning |
| Routing | **Jira**, **Slack**, **Email (SMTP/Gmail)** | Actions based on complexity |
| Storage | **Google Sheets** (V1) → **PostgreSQL** (V2) | Logging, analytics |
| Deployment | **Docker** (future) | Reproducible local/runtime environment |
| Vector Search | **Chroma / Pinecone** (future) | RAG upgrades |
| CI/CD | **GitHub Actions** (future) | Tests, linting, deploys |

---

## 🔐 Security & Privacy
	-	Do not commit real credentials or tokens.
	-	Use environment variables and n8n’s encrypted credential store.
	-	If using real customer data, sanitize or mock in public repos.

  ---

##  🧾 License
MIT License © 2025 — free to use and modify.

---

## 👤 Author

Jonathan Barnette
Data Automation / AI Automation Engineer
GitHub: https://github.com/
LinkedIn: https://www.linkedin.com/in/jonathan-barnette

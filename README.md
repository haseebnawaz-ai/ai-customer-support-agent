# ⚡ AI Customer Support Agent (Groq & PostgreSQL Integration)

An ultra-fast, enterprise-grade autonomous customer support system built with **n8n**, **Groq AI (Llama-3)**, **PostgreSQL**, **Slack**, and **Webhook/SMTP integrations**. This workflow catches customer inquiries in real time, classifies customer intent using low-latency LLMs, queries live order data from a PostgreSQL database, handles automated returns, escalates edge cases to human agents via Slack, and returns context-aware responses.

---

## 🎯 Key Capabilities

- **Instant Intent Classification:** Leverages Groq's high-throughput Llama-3 model to categorize incoming inquiries (e.g., Order Tracking, Return Request, Escalation).
- **Automated Database Enrichment:** Directly queries PostgreSQL databases (`Get Order Details`) to fetch real-time order and shipping context.
- **Human-in-the-Loop Escalation:** Automatically routes complex queries or low-confidence requests to team channels via Slack.
- **Automated Returns & Communications:** Triggers automated return instructions via Email while generating personalized AI draft replies for standard inquiries.
- **Multi-Channel Dispatch:** Extracts finalized AI responses and sends them back instantly through direct API response webhooks or email.

---

## 📐 Workflow Architecture

![System Architecture](./AI%20Customer%20Support%20Agent%20%28Groq%29.jpg)

---

## 🛠️ Tech Stack & Integrations

- **Orchestration:** n8n Workflow Engine
- **LLM Engine:** Groq API (Llama-3 Models for Sub-Second Latency)
- **Database:** PostgreSQL (Order & Customer Lookup)
- **Notifications:** Slack API (Team Escalation)
- **Communication:** Webhooks, SMTP Email

---

## 🚀 How to Import & Run

1. Clone this repository or download the workflow `.json` file.
2. Open your n8n workspace dashboard.
3. Click **Workflows** ➔ **Import from File** and select the `.json` file.
4. Configure required credentials in n8n:
   - **Groq API Key**
   - **PostgreSQL Database Connection Details**
   - **Slack OAuth Token**
   - **SMTP Email Credentials**
5. Save and switch the trigger status to **Active**.

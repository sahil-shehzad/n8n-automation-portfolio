# AI Automation & Agentic Workflows (n8n)

**Author:** Sahil Shehzad  
**Role:** AI Automation Engineer  
**Contact:** sahil.shehzad@outlook.com

## 🚀 Overview

This repository showcases my expertise in building self-healing, intelligent automation architectures. I specialize in bridging business logic with Large Language Models (LLMs) to create autonomous agents that handle sales, productivity, and data processing.

## 🛠️ Tech Stack & Integrations

* **Orchestration:** n8n (Webhooks, Code Nodes, Error Handling)
* **AI & LLMs:** OpenAI API, Anthropic Claude, Vapi (Voice AI), Tavily (AI Search)
* **Vector Database:** Pinecone (RAG Pipelines)
* **Frontend/Tools:** Lovable.dev, Telegram API, Google Workspace (Sheets, Calendar, Gmail)

---

## 📂 Project Breakdown

### 1. B2B Inbound Voice Sales Agent (Vapi + n8n)
* **Description:** A fully autonomous voice agent acting as a 24/7 Sales Development Representative (SDR).
* **Key Features:**
    * Handles inbound calls and naturally qualifies leads using Vapi.
    * Checks real-time availability and books appointments via Google Calendar.
    * **Workflow Logic:** Logs booking details to CRM, triggers Slack notifications to the team, and sends confirmation emails to the user.

### 2. "Friday" - Agentic Personal Assistant (Telegram + Tavily)
* **Description:** A central command center bot for personal productivity, accessible via Telegram.
* **Key Features:**
    * **Multi-Modal Input:** Processes text and Voice Notes (via Whisper API).
    * **Agentic Capabilities:** Autonomously manages Google Calendar events.
    * **Deep Research:** Uses Tavily AI to perform web research, summarize findings, and log data into a structured Google Sheet.

### 3. RAG Knowledge Base Chatbot (n8n + Pinecone)
* **Description:** A customer support expert pipeline using Retrieval-Augmented Generation (RAG).
* **Key Features:**
    * **Vectorization:** Ingests PDF books/documentation and creates vector embeddings in Pinecone.
    * **Context Retrieval:** Retrieves strict context to answer queries accurately, minimizing hallucinations and grounding answers in source material.

### 4. Full-Stack ATS Resume Optimizer (n8n + Lovable)
* **Description:** A consumer-facing web app backend that analyzes resumes against job descriptions.
* **Key Features:**
    * Extracts text from PDF/Docx files.
    * Uses LLMs to generate an ATS Compatibility Score and a "Missing Keywords" list.
    * Frontend built with Lovable; Backend logic handled by n8n.

### 5. Automated Financial Document Processing (AI + OCR)
* **Description:** An accounts receivable automation system.
* **Key Features:**
    * Ingests paid invoice PDFs and uses AI/OCR to extract unstructured data (Line Items, Tax, Dates).
    * Organizes data into a clean Google Sheet database and triggers email reports to the billing department.

---

## ⚠️ Usage Note
These workflows are exported as JSON. To use them:
1.  Import the JSON file into your n8n instance.
2.  Configure your own credentials (API keys for OpenAI, Vapi, Google, etc.) in the n8n credential manager.

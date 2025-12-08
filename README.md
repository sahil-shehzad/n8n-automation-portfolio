# AI Automation & Agentic Workflows (n8n)

**Author:** Sahil Shehzad  
**Role:** AI Automation Engineer  
**Contact:** sahil.shehzad@outlook.com

## 🚀 Overview

This repository showcases my expertise in building self-healing, intelligent automation architectures. I specialize in bridging business logic with Large Language Models (LLMs) to create autonomous agents that handle sales, productivity, and data processing.

## 🛠️ Tech Stack & Integrations

* **Orchestration:** n8n (Webhooks, Code Nodes, Error Handling)
* **AI & LLMs:** OpenAI API, Anthropic Claude, Vapi (Voice AI), Tavily (AI Search), Gemini 3-pro
* **Data & Scraping:** Firecrawl, Apify, Hunter.io, People Data Labs (PDL)
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

### 2. Automated Lead Gen & Enrichment Pipeline (n8n + Firecrawl + People Data Labs)
* **Description:** A "Headhunter" agent that autonomously monitors startup directories (Y-Combinator), replacing hours of manual lead research.
* **Key Features:**
    * **Smart Ingestion:** Utilizes Firecrawl to scrape dynamic web pages into Markdown.
    * **AI Qualification:** Leverages Gemini 3-pro to parse unstructured data and strictly qualify leads based on "B2B SaaS" criteria.
    * **Enrichment Loop:** Integrates People Data Labs API to enrich validated companies with CEO contact details and firmographics, automatically pushing high-value leads to a Google Sheet CRM.

### 3. Local Business Scraper & Enrichment Pipeline (n8n + Apify + Hunter.io)
* **Description:** A "Local Hunter" pipeline designed to target offline industries by solving the "missing email" problem in Google Maps data.
* **Key Features:**
    * **Scraping & Enrichment:** Orchestrates Apify to scrape Google Maps business data, then pipes domains into Hunter.io to identify decision-maker emails.
    * **Idempotent CRM Sync:** Implements a "Search-First" logic for HubSpot/Google Sheets that checks for existing leads before creation, ensuring 100% data hygiene and zero duplicates.

### 4. Smart Cold Email Outreach Sequencer (n8n + Gmail)
* **Description:** A serverless, state-aware drip campaign manager that runs entirely from Google Sheets, replacing tools like Lemlist.
* **Key Features:**
    * **State-Aware Logic:** Custom JavaScript calculates precise sending windows (Day 0, 3, 8) and enforces rules like "No Weekend Sending."
    * **Thread Context:** Queries the Gmail API to identify existing conversations, ensuring follow-ups are threaded correctly.
    * **Stop-on-Reply:** Automatically terminates the sequence if a lead replies, protecting domain reputation.

### 5. Advanced Voice Receptionist & RAG Agent (n8n + Vapi + Pinecone)
* **Description:** A "Full-Stack" voice assistant capable of handling complex customer support scenarios via a RAG pipeline.
* **Key Features:**
    * **Tool Orchestration:** Uses Vapi "Server URLs" to trigger n8n workflows for checking Calendar availability and performing vector DB lookups.
    * **RAG Integration:** Retrieves context from a Pinecone vector store to answer specific policy/pricing questions accurately without hallucinating.
    * **Context Preservation:** Maintains conversation state to handle multi-turn booking scenarios seamlessly.

### 6. "Friday" - Agentic Personal Assistant (Telegram + Tavily)
* **Description:** A central command center bot for personal productivity, accessible via Telegram.
* **Key Features:**
    * **Multi-Modal Input:** Processes text and Voice Notes (via Whisper API).
    * **Agentic Capabilities:** Autonomously manages Google Calendar events.
    * **Deep Research:** Uses Tavily AI to perform web research, summarize findings, and log data into a structured Google Sheet.

### 7. RAG Knowledge Base Chatbot (n8n + Pinecone)
* **Description:** A customer support expert pipeline using Retrieval-Augmented Generation (RAG).
* **Key Features:**
    * **Vectorization:** Ingests PDF books/documentation and creates vector embeddings in Pinecone.
    * **Context Retrieval:** Retrieves strict context to answer queries accurately, minimizing hallucinations and grounding answers in source material.

### 8. Full-Stack ATS Resume Optimizer (n8n + Lovable)
* **Description:** A consumer-facing web app backend that analyzes resumes against job descriptions.
* **Key Features:**
    * Extracts text from PDF/Docx files.
    * Uses LLMs to generate an ATS Compatibility Score and a "Missing Keywords" list.
    * Frontend built with Lovable; Backend logic handled by n8n.

### 9. Automated Financial Document Processing (AI + OCR)
* **Description:** An accounts receivable automation system.
* **Key Features:**
    * Ingests paid invoice PDFs and uses AI/OCR to extract unstructured data (Line Items, Tax, Dates).
    * Organizes data into a clean Google Sheet database and triggers email reports to the billing department.

---

## ⚠️ Usage Note
These workflows are exported as JSON. To use them:
1.  Import the JSON file into your n8n instance.
2.  Configure your own credentials (API keys for OpenAI, Vapi, Google, Apify, etc.) in the n8n credential manager.

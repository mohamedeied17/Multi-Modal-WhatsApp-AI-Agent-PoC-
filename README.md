# Multi-Modal WhatsApp AI Agent (PoC) 🤖

An autonomous, multi-modal WhatsApp AI assistant designed to eliminate context-switching by executing real-time tasks directly from the chat interface. 

This Proof of Concept (PoC) leverages **n8n** for workflow automation and **Evolution API** to bypass the rigid template restrictions of the official WhatsApp Cloud API, enabling unstructured conversational freedom and a critical "Human-in-the-Loop" safeguard.

## 🚀 Key Features

* **🎙️ Voice-to-Calendar:** Automatically transcribes voice notes and schedules Google Calendar events dynamically.
* **📸 Image-to-Email (Vision):** Extracts text from uploaded images/screenshots to format and dispatch professional emails via Gmail.
* **🔍 Text-to-Search:** Executes live web research based on text commands and returns summarized, hallucination-free insights.

## 🏗️ System Architecture & "Human-in-the-Loop"

Standard WhatsApp bots rely on the official Cloud API, which restricts interactions to pre-approved templates and blocks real-time visibility on the primary WhatsApp application. 

By architecting this solution with **Evolution API**, the system achieves two critical business advantages:
1. **Unstructured Multi-modal Inputs:** The AI can process and respond to free-flowing text, voice, and images naturally.
2. **Real-time Monitoring:** Every AI interaction is visible on the linked WhatsApp Web/Mobile app. If the AI misunderstands a user intent, a human operator can instantly step in and take over the conversation, ensuring a fail-safe "Human-in-the-Loop" mechanism.

## ⚙️ Tech Stack

* **Workflow Engine:** [n8n](https://n8n.io/)
* **WhatsApp Gateway:** [Evolution API](https://evolution-api.com/)
* **Database / Cache:** PostgreSQL, Redis
* **Infrastructure:** Docker & Docker Compose
* **External Integrations:** Google Workspace (Calendar, Gmail)

## 📂 Repository Contents

* `docker-compose.yml`: Infrastructure configuration to spin up n8n, Evolution API, Postgres, and Redis containers.
* `Multi_Modal_AI_Agent.json`: The exported n8n workflow file ready for import.

## 🛠️ How to Deploy (Local Environment)

1. Clone this repository.
2. Spin up the infrastructure using Docker Compose:
   ```bash
   docker compose up -d

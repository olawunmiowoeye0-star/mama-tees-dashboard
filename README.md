# 🍲 Mama Tee's Kitchen — AI WhatsApp Chatbot

> An AI-powered WhatsApp chatbot built for Mama Tee's Kitchen, a fictional Nigerian food delivery brand based in Lagos. Built as a capstone project for the AI Automation Bootcamp.

---

## 🔴 Live Demo

| What | Link |
|------|------|
| 💬 WhatsApp Bot | Send `join [your-sandbox-code]` to **+1 415 523 8886** (Twilio sandbox) |
| 📊 Live Dashboard | [https://olawunmiowoeye0-star.github.io/mama-tees-dashboard/dashboard_v3.html](https://olawunmiowoeye0-star.github.io/mama-tees-dashboard/dashboard_v3.html) |

---

## 📌 Project Overview

Mama Tee's Kitchen is a fictional Nigerian restaurant in Lagos that receives customer orders and enquiries via WhatsApp. This project automates the entire customer interaction flow using AI — from answering menu questions to placing orders and escalating unresolved conversations to a human agent.

The system includes:
- A **WhatsApp chatbot** powered by AI that handles customer messages 24/7
- A **RAG (Retrieval-Augmented Generation)** pipeline so the bot answers from the restaurant's actual menu and FAQs
- An **Airtable database** storing all messages, orders, and customer records
- A **live operations dashboard** for the restaurant team to monitor conversations and handle escalations

---

## 🛠 Tech Stack

| Tool | Purpose |
|------|---------|
| **n8n** | Workflow automation — connects all tools together |
| **Twilio** | WhatsApp Business API integration |
| **Groq (llama-3.1-8b)** | AI chat responses (fast, free inference) |
| **Pinecone** | Vector database for RAG (menu & FAQ retrieval) |
| **Airtable** | Stores messages, conversations, orders, and users |
| **HTML / JavaScript** | Live operations dashboard (this repo) |

---

## 🏗 Architecture

```
Customer (WhatsApp)
        ↓
    Twilio API
        ↓
     n8n Workflow
     ├── Pinecone (retrieve relevant menu/FAQ context)
     ├── Groq AI (generate response using context)
     ├── Airtable (log message + conversation)
     └── Handoff logic (escalate to human if needed)
        ↓
  Reply sent back to customer via Twilio
        ↓
  Dashboard reads from Airtable in real time
```

---

## 📁 Repository Structure

```
mama-tees-dashboard/
│
├── README.md               ← You are here
├── dashboard_v3.html       ← Live operations dashboard (open in browser)
└── workflows/              ← n8n exported workflow JSON (coming soon)
```

---

## 🚀 How to Run the Dashboard

1. Download `dashboard_v3.html`
2. Open it in any browser — it works without a server
3. Click **⚙ Settings** and enter your Airtable credentials:
   - Personal Access Token
   - Base ID
4. Click **Connect** — the dashboard loads your live data

> No Airtable? The dashboard works in **Demo Mode** out of the box with sample Nigerian restaurant conversations pre-loaded.

---

## 💡 Key Features

- ✅ Real-time conversation monitoring
- ✅ Auto-detects Airtable field names (no manual mapping needed)
- ✅ Filter conversations by Active / Handoff / Resolved
- ✅ Human agent can reply directly from the dashboard
- ✅ One-click handoff resolution
- ✅ Auto-refreshes every 30 seconds
- ✅ Works in Demo Mode for presentations

---

## 👩🏾‍💻 Built By

**Group 13** — AI Automation Bootcamp Capstone Project, 2025

# 🍲 Mama Tee's Kitchen — AI WhatsApp Chatbot

## Project Overview
An AI-powered WhatsApp chatbot built for Mama Tee's Kitchen, 
a fictional Nigerian food delivery brand. Built as a capstone 
project for the AI Automation Bootcamp.

## Live Demo
- 📱 WhatsApp Bot: Send "join [your-sandbox-code]" to +1 415 523 8886
- 📊 Dashboard: https://olawunmiowoeye0-star.github.io/mama-tees-dashboard

## Tech Stack
| Tool | Purpose |
|------|---------|
| n8n | Workflow automation |
| Twilio | WhatsApp integration |
| Groq (llama-3.1-8b) | AI chat responses |
| Pinecone | Vector database for RAG |
| Google Gemini | Text embeddings |
| Airtable | Users, messages, conversations |
| GitHub Pages | Dashboard hosting |

## System Architecture
<img width="1513" height="886" alt="image" src="https://github.com/user-attachments/assets/2d484fcf-816d-4889-936a-a5b1d9ae790c" />

## Workflows
1. **Inbound Message Handler** — receives and responds to WhatsApp messages
2. **Knowledge Base Loader** — uploads menu and FAQ documents to Pinecone
3. **Human Handoff Handler** — escalates conversations to human agents

## Setup Instructions
1. Import the 3 JSON files from `/workflows` folder into n8n
2. Add these credentials in n8n:
   - Twilio Account SID and Auth Token
   - Airtable Personal Access Token
   - Groq API Key
   - Pinecone API Key
   - Google Gemini API Key
3. Run the Knowledge Base Loader workflow once
4. Activate Inbound Message Handler workflow
5. Activate Human Handoff Handler workflow
6. Join Twilio sandbox — send "join [code]" to +1 415 523 8886
7. Open the dashboard at the link above

## Knowledge Base
The `/knowledge-base` folder contains 5 documents uploaded to Pinecone:
- `menu.txt` — full menu with prices
- `faqs.txt` — frequently asked questions
- `delivery.txt` — delivery zones and fees
- `policies.txt` — business policies
- `about.txt` — brand story and contact details

## Features
- ✅ 24/7 automated WhatsApp responses
- ✅ RAG-powered accurate menu and FAQ answers
- ✅ Conversation memory and user profiles
- ✅ Human handoff when needed
- ✅ Live monitoring dashboard
- ✅ Auto-saves all messages to Airtable


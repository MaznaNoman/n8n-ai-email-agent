# Autonomous AI Email Agent & Lead Engagement Workflow (n8n)

An automated AI-powered email outreach and lead processing system built with **n8n**, **Google Gemini**, **Gmail**, and **Google Sheets**. 

This workflow automatically fetches business leads on a scheduled basis, uses an AI Agent equipped with Google Gemini to generate structured email messages, sends personalized outreach via Gmail, and logs/updates the outreach status back into Google Sheets.

---

## Workflow Architecture

The workflow consists of the following pipeline:

1. **Schedule Trigger**: Periodically triggers the execution pipeline.
2. **Get_Business_Leads (Google Sheets Node)**: Reads target leads/contacts from a master Google Sheet.
3. **AI Agent Core**:
   * **Language Model**: `Google Gemini Chat Model` for natural language understanding and content generation.
   * **Structured Output Parser**: Enforces a strict JSON format for generated responses.
4. **Send a Message (Gmail Node)**: Dispatches the customized email to the targeted lead.
5. **Append or Update Row in Sheet (Google Sheets Node)**: Updates the leads database with outreach records, timestamp, or response statuses.

---

## Prerequisites

* [n8n](https://n8n.io/) installed locally (via npm or Docker) or hosted on cloud.
* Google Cloud Console Project with the following APIs enabled:
  * **Gmail API**
  * **Google Sheets API**
* **Google Gemini API Key** (from Google AI Studio).

---

## Setup & Installation

### 1. Clone the Repository
```bash
git clone [https://github.com/MaznaNoman/AI_Email_Agent_n8n.git](https://github.com/MaznaNoman/AI_Email_Agent_n8n.git)
cd AI_Email_Agent_n8n
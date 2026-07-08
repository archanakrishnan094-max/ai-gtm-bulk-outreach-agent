# 🚀 AI GTM Bulk Outreach Automation Agent

## Overview

AI GTM Bulk Outreach Automation Agent is an end-to-end workflow built using **n8n** that automates the Go-To-Market (GTM) outreach process.

The workflow performs company research, generates structured GTM insights using AI, creates personalized cold emails, sends emails through Gmail, and logs all research and outreach activities into Google Sheets.

---

## Features

* Multi-company processing
* AI-powered company research
* Business summary generation
* Target customer identification
* Pain point analysis
* AI opportunity identification
* Personalized cold email generation
* Gmail integration
* Google Sheets integration
* JSON data transformation
* Automated outreach logging

---

## Workflow Architecture

### AI GTM Bulk Outreach Automation Agent

```
🚀 Manual Trigger
        │
        ▼
📄 Read Company Queue (Google Sheets)
        │
        ▼
🔁 Loop Over Companies
        │
        ▼
🌐 HTTP Request (Company Research)
        │
        ▼
⏳ Wait (Rate Limiting)
        │
        ▼
🤖 AI GTM Research Agent
        │
        ▼
🛠️ Research JSON Parser (Code Node 1)
        │
        ├────────────► 📊 Google Sheets (Research Repository)
        │
        └────────────► ✉️ AI Personalized Email Generator
                              │
                              ▼
                    🛠️ Email JSON Parser (Code Node 2)
                         │                  │
                         │                  └────────► 📧 Gmail
                         │
                         ▼
                    🔀 Merge Research + Email
                         ▲
                         │
               Research JSON Parser
                  (Code Node 1)
                         │
                         ▼
                📝 Google Sheets (Outreach History)

```

### Workflow Summary

1. Reads multiple companies from Google Sheets.
2. Processes each company individually.
3. Collects company information through an HTTP request.
4. Uses AI to generate structured GTM research.
5. Converts the research into structured JSON.
6. Stores research in Google Sheets.
7. Generates personalized cold emails using AI.
8. Converts the email into structured JSON.
9. Sends personalized emails through Gmail.
10. Merges company research with email data.
11. Logs the complete outreach history in Google Sheets.

---

## Technology Stack

* n8n
* Google Sheets
* Gmail
* Groq LLM
* HTTP API
* JavaScript
* JSON

---

## Input

Google Sheet 1

| Company Name | Website | Email |
| ------------ | ------- | ----- |

---

## Output

### Research Repository

* Company Name
* Industry
* Business Summary
* Target Customers
* Pain Points
* AI Opportunities

### Outreach Log

* Company Name
* Email Subject
* Greeting
* Cold Email
* Closing
* CTA
* Status
* Timestamp

---

## Project Screenshots

### Workflow Overview

(https://github.com/archanakrishnan094-max/ai-gtm-bulk-outreach-agent/blob/main/screenshots/01-workflow-overview.png.png)

### Company Research Output

(https://github.com/archanakrishnan094-max/ai-gtm-bulk-outreach-agent/blob/main/screenshots/02-ai-research-output.png.png)

### AI Cold Email

(Add screenshot)

### Gmail Output

(Add screenshot)

### Google Sheet Research

(Add screenshot)

### Google Sheet Outreach Log

(Add screenshot)

---

## Skills Demonstrated

* AI Workflow Automation
* Prompt Engineering
* GTM Automation
* Sales Automation
* JSON Processing
* JavaScript
* Google Workspace Automation
* API Integration
* Workflow Design
* Multi-step AI Pipelines

---

## Future Improvements

* HubSpot CRM Integration
* Clay Integration
* Lead Scoring
* Revenue Intelligence
* Follow-up Email Automation
* Reply Tracking
* Meeting Scheduling
* Slack Notifications

---

## Author

**Archana Krishnan**

AI Automation | GTM Engineering | Workflow Automation | AI Solutions

LinkedIn: (Add your LinkedIn URL)

Portfolio: (Add your Portfolio URL)

---

## License

MIT License

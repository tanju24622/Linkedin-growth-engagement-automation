# 🚀 LinkedIn Growth & Engagement Automation Suite

An end-to-end **AI-powered LinkedIn automation project** built with **n8n, Google Sheets, Google Gemini, Gmail, and the LinkedIn API**.

## 📌 Project Overview

This project automates important parts of a LinkedIn growth and engagement process:

- ✨ AI-powered LinkedIn content generation
- 🔗 LinkedIn API publishing
- 🎯 AI lead scoring and qualification
- 💬 LinkedIn comment analysis
- 🧠 Sentiment, intent, and priority detection
- ✍️ Suggested reply generation
- 📧 Gmail notifications
- 📊 Automated analytics and reporting

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| **n8n** | Workflow automation |
| **Google Gemini** | AI generation and analysis |
| **Google Sheets** | Data storage |
| **LinkedIn API** | Post publishing |
| **Gmail** | Notifications |
| **JavaScript** | Data transformation |
| **GitHub** | Documentation |

## 🔄 Main Workflows

### 1. LinkedIn Content Generator

`Manual Trigger → Google Sheets → Google Gemini → Generated Posts → IF → LinkedIn API → Update Sheet`

The workflow reads content ideas, generates professional LinkedIn posts with Gemini, publishes approved content through the LinkedIn API, and updates the Google Sheet status.

### 2. LinkedIn Lead Scoring & Qualification

`Manual Trigger → Read Sheet → Google Gemini → JavaScript → Update Sheet`

The AI evaluates lead information and generates an **AI Score, AI Reason, Qualification, and Status**.

Example results:

| Lead | Position | AI Score | Qualification |
|---|---|---:|---|
| Sarah Johnson | CEO | 95 | Hot |
| David Wilson | Marketing Manager | 78 | Warm |
| Emily Brown | Operations Lead | 85 | Hot |

**Analytics:** 3 total leads, 2 Hot, 1 Warm, 0 Cold, average AI Score **86**.

### 3. LinkedIn Comment Engagement

`Read Comments → Google Gemini → JavaScript → IF → Gmail / Engagement Action`

The workflow analyzes comments for:

- 😊 Sentiment
- 🎯 Intent
- 🚨 Priority
- ✍️ Suggested Reply

Example:

**Comment:** `Can you share more about n8n?`

**Result:** Positive sentiment · Question intent · Medium priority.

The system generates a context-aware suggested reply and can send Gmail notifications when attention is required.

### 4. LinkedIn Analytics & Reporting

The reporting workflow summarizes the project data.

**Current results:**

- 📈 Total Posts: **8**
- 🟢 Published Posts: **1**
- 🎯 Total Leads: **3**
- 🔥 Hot Leads: **2**
- 🟡 Warm Leads: **1**
- ⚪ Cold Leads: **0**
- 📊 Average AI Score: **86**
- 💬 Total Comments: **2**
- 😊 Positive Comments: **2**
- 🟠 Medium Priority: **1**
- 🟢 Low Priority: **1**

## 🧠 AI Capabilities

Google Gemini is used for:

- Content generation
- Lead scoring
- Lead qualification
- Comment sentiment analysis
- Intent detection
- Priority classification
- Suggested reply generation
- Analytics/report preparation

## 📊 Data Structure

Google Sheets is used as a lightweight database for:

- **Content Ideas:** ID, Topic, Status, Date, Post
- **Generated Posts:** generated content and publishing status
- **Lead Scoring:** Name, Company, Position, AI Score, AI Reason, Qualification, Status
- **Comments:** Name, Comment, Reply, Sentiment, Intent, Priority, Suggested Reply, Status

## 🔐 Security

API keys, LinkedIn access tokens, OAuth credentials, client secrets, and passwords should **never** be committed to GitHub. Sensitive credentials should remain in n8n Credentials or secure environment variables.

## 📸 Screenshots

Recommended screenshots to include:

1. Content Generator workflow
2. Successfully published LinkedIn post
3. Lead Scoring workflow
4. Lead scoring Google Sheet result
5. Comment Engagement workflow
6. Comment analysis result
7. Analytics & Reporting workflow
8. Final analytics output

## 🚀 Workflow Architecture

```text
Google Sheets
     │
     ▼
    n8n
     │
 ┌───┼──────────────┐
 ▼   ▼              ▼
AI Content     AI Lead       AI Comment
Generation     Scoring       Analysis
 │              │              │
 ▼              ▼              ▼
LinkedIn      Google        Gmail /
API           Sheets        Engagement
     └──────────┬───────────┘
                ▼
        Analytics & Reporting

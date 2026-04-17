# AI Lead Intelligence Pipeline

## Overview
This project processes lead data using n8n workflows. It includes:
- Webhook-based lead intake
- Automated email reporting
- Data analysis workflow

---

## Setup Instructions

### 1. Import Workflows
- Open n8n
- Import JSON files:
  - webhook_email_workflow.json
  - analysis_workflow.json

---

### 2. Configure Credentials
- Add Gmail OAuth2 credentials
- Connect Google Sheets (if used)

---

### 3. Run Webhook Workflow
- Click "Listen for Test Event"
- Send POST request using Hoppscotch

Example:
{
  "company": "Test AI",
  "lead_score": 50
}

---

### 4. Expected Output
- Email report is sent
- Data processed successfully

---

## Technologies Used
- n8n
- Google Sheets
- Gmail API
- Hoppscotch

📊 ✅ 4. Sample Dataset

Create a file: sample_data.json

[
  { "company": "OpenAI", "lead_score": 80 },
  { "company": "Google", "lead_score": 90 },
  { "company": "StartupX", "lead_score": 60 }
]
📸 ✅ 5. Evidence of Successful Runs

Include screenshots of:

✅ Webhook success (200 OK)
✅ Gmail sent message
✅ n8n execution green path

👉 Name files:

success_webhook.png
success_email.png
workflow_execution.png
❌ ✅ 6. Failure Test Examples

Show wrong inputs:

Example 1:
{ "company": "", "lead_score": null }
Example 2:
{ "company": "Test" }

👉 Capture:

Error handling OR incorrect output
📁 ✅ 7. Output Dataset

If using Sheets or output JSON:

[
  {
    "company": "OpenAI",
    "lead_score": 80,
    "total_leads": 1,
    "avg_score": 80
  }
]
📧 ✅ 8. Generated Report (Email)

Example:

Subject: Lead Report

New Lead Received:

Company: OpenAI
Lead Score: 80

Total Leads: 1
Average Score: 80

👉 Include screenshot of email

🏁 Final Folder Structure
project/
│
├── workflows/
│   ├── webhook_email_workflow.json
│   ├── analysis_workflow.json
│
├── docs/
│   ├── architecture.png
│   ├── README.md
│
├── data/
│   ├── sample_data.json
│   ├── output_data.json
│
├── screenshots/
│   ├── success_webhook.png
│   ├── success_email.png
│   ├── failure_test.png
│
└── report/
    └── email_output.png
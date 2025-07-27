# 📄 Notion Auto-Entry with n8n Webhook

A robust automation solution for inserting structured data into a **Notion database** using **n8n** Webhooks. This project streamlines task and contact management by connecting external inputs (e.g., forms, Postman, or APIs) to Notion with dynamic data formatting.

---

## 🚀 Features

- **Webhook-Driven Input**: Accepts structured JSON data from external sources like Postman, forms, or APIs.
- **Dynamic Data Formatting**: Uses n8n's Function node to transform input into Notion’s strict database structure.
- **Notion Integration**: Creates rows in a Notion database with support for `title`, `rich_text`, `select`, and `date` fields.
- **Batch Support**: Handles single or multiple entries via array-based JSON payloads.
- **Flexible Use Cases**: Ideal for logging tasks, leads, contacts, or form submissions directly into Notion.

---

## 🧩 Tech Stack

- **n8n**: Open-source, self-hosted workflow automation platform.
- **Notion API**: For seamless database interaction and row creation.
- **Webhook Trigger**: Captures JSON input from external tools or apps.
- **JavaScript (Function Node)**: Dynamically formats input to match Notion’s schema.

---

## 📥 Sample JSON Input

Below is an example JSON payload to send via Postman or other tools:

```json
{
  "Employee Name": "Saad Tahir",
  "Department": "Automation",
  "Current Project": "CRM Integration",
  "Progress Status": "Responded",
  "Deadline": "2025-08-10",
  "Notes": "Webhook automation test"
}
```

For batch processing, send an array:

```json
[
  {
    "Employee Name": "Saad Tahir",
    "Department": "Automation",
    "Current Project": "CRM Integration",
    "Progress Status": "Responded",
    "Deadline": "2025-08-10",
    "Notes": "Webhook automation test"
  },
  {
    "Employee Name": "Ayesha Khan",
    "Department": "Marketing",
    "Current Project": "Campaign Launch",
    "Progress Status": "In Progress",
    "Deadline": "2025-08-15",
    "Notes": "Social media integration"
  }
]
```

---

## 🔁 Workflow Overview

1. **Webhook Trigger**: Receives JSON input from external sources.
2. **Function Node**: Transforms raw input into Notion-compatible format.
3. **Notion Node**: Inserts formatted data as a new row in the specified Notion database.
4. **Output**: Confirms successful entry with a response or logs errors for debugging.

---

## 🧪 Use Cases

- **Form Integration**: Send Typeform, Tally, or custom form submissions directly to Notion.
- **CRM Automation**: Log leads, tasks, or contacts from tools like HubSpot or Salesforce.
- **Task Management**: Automate task logging from Telegram, Slack, or other apps.
- **Replace Legacy Workflows**: Swap Google Sheets + Zapier with a lightweight, custom n8n solution.

---

## 🖼️ Screenshots

To showcase this project in your portfolio, include these visuals:

- **n8n Workflow**: Screenshot of the full workflow in n8n.
- **Postman Request**: Sample Webhook request with JSON payload.
- **Notion Database**: Before and after views of the Notion database.
- **Function Node Output**: JSON transformation from raw input to Notion format.

---

## 📁 Repository Structure

```bash
/workflows
  └── notion-auto-entry.json       # n8n workflow export
/images
  ├── workflow-screenshot.png      # n8n workflow screenshot
  ├── notion-entry-preview.png     # Notion database screenshot
  └── postman-request.png          # Postman webhook request
README.md                          # Project documentation
```

---

## 🛠️ Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   ```

2. **Import Workflow**:
   - Open your n8n instance.
   - Import `notion-auto-entry.json` from the `/workflows` folder.

3. **Configure Notion Credentials**:
   - In n8n, set up a Notion API key and connect it to the Notion node.
   - Specify the target Notion database ID in the node settings.

4. **Copy Webhook URL**:
   - Activate the Webhook node in n8n and copy the provided URL.

5. **Test with Postman**:
   - Send a sample JSON payload (like the one above) to the Webhook URL.
   - Verify the new entry appears in your Notion database.

6. **Deploy and Scale**:
   - Use the workflow in production with forms, CRMs, or other apps.
   - Monitor n8n logs for errors or performance issues.

---

## 📣 Author

- **Name**: Ahmad Raza
- **Fiverr**: [nitrola](https://www.fiverr.com/sellers/nitrola/edit)
- **LinkedIn**: [Ahmad Raza](https://www.linkedin.com/in/ahmad-raza-403bbd0278)
- **Date**: July 27, 2025

---

## 🏷️ Tags

`#n8n` `#notion` `#automation` `#nocode` `#webhook` `#postman` `#integration` `#productivity` `#workflowautomation` `#javascript`

---

## 🌟 Why This Project?

This project is **portfolio-ready** and demonstrates expertise in no-code automation, API integration, and data transformation. Share it with automation communities, clients, or on LinkedIn to showcase your skills.

**Need a Video Demo or PDF Portfolio?** I can help you create a polished video walkthrough or a professional PDF version of this project. Just let me know!

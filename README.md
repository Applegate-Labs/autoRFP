# Auto-RFP Skill for Manus

A powerful, workflow-agnostic Manus skill that automates the creation of tailored consulting proposals. It extracts requirements from client RFPs, matches them against your firm's project credentials and team CVs, and injects the synthesized content directly into your standard RFP response template.

Built for the **Manus × Vibecoding: Consulting Hackathon**.

## Manus Session
View Manus Session link [here](https://manus.im/share/S8DcZhwMq76mbabQnB0G6p)



## Features

- **Template Agnostic:** Uses a dynamic discovery script to map placeholders in any PPTX template. No hardcoded shape names or slide limits.
- **Flexible Data Ingestion:** Accepts project databases in Excel, CSV, or Markdown formats. Automatically maps your columns to the required fields.
- **Multi-Workflow Support:**
  - **Project Folder (Cloud):** Upload credentials to the Manus Project Knowledge Base. 
  - **Desktop App:** Attach a local folder directly from your computer using the Manus Desktop App.
  - **Cloud Connectors:** Pull credentials directly from connected Google Drive, Notion, or SharePoint folders.
- **Smart Overflow Handling:** Automatically detects when table content (like Scope of Work) exceeds slide capacity and safely duplicates slides to prevent overflow.

## Installation

1. Download the skill file.
2. Upload the skill into Manus.

## Usage

1. Ensure your firm's credentials (PPTX template, project database, and team CVs) are accessible via one of the supported workflows in Manus.
2. Upload or paste the client RFP document into your Manus task.
3. Type the following prompt:
   > Invoke the `/auto-rfp` skill. Use the attached RFP document as the client requirement.

Manus will automatically locate your credentials, select the best-matching projects and team members, draft the content, and deliver a finalized RFP response document.

## Skill Folder Structure

```text
auto-rfp/
├── SKILL.md                 # Core agent instructions and workflow logic
├── references/
│   └── setup-guide.md       # Setup instructions for all three supported workflows
├── scripts/
│   ├── discover_template.py # Dynamically maps PPTX shapes and placeholders
│   └── pptx_helpers.py      # Safe PPTX mutation functions (replace text, add rows, etc.)
└── templates/
    └── proposal-template.pptx # A generic, bundled proposal template to get started
```

## License

This project is open-source and available under the MIT License.

# n8n Workflows

A collection of n8n automation workflows that connect AI models with everyday tools to automate real-world tasks.

Each workflow lives in its own folder with an importable JSON file, a screenshot of the flow, and a README explaining how it works.

## Tools & Integrations

I'm still learning and exploring, so this is a growing list. These are **examples** of what I've used so far, and more will be added as I build new workflows:

- **Triggers:** Chat Trigger, Form Trigger, Webhook, Schedule Trigger
- **Data & Productivity:** Google Sheets, Gmail, Airtable
- **AI & Machine Learning:** OpenAI models, Groq models, AI Agents with memory and tools

## AI Model Provider

Most of the AI models in these workflows are accessed through [SovereignEG](https://backend.sovereigneg.com), an Egyptian platform that provides an OpenAI-compatible API. It lets me use many different models from different providers through a single endpoint, by setting a custom Base URL in the OpenAI credentials in n8n.

## Projects

| Project | Description | Tools |
|---------|-------------|-------|
| [Tech Sales Bot](./tech-sales-bot) | Chatbot that answers customers using a live inventory sheet, remembers the conversation, and emails the store owner with the customer's details when they want to place an order | n8n, AI Agent, OpenAI, Google Sheets, Gmail |
| [Review Sentiment Analyze](./review-sentiment-analyze) | Collects supermarket reviews through an Arabic form, summarizes them and classifies their sentiment with AI, saves them to Google Sheets, and emails the owner on negative reviews | n8n, Form Trigger, LLM, Google Sheets, Gmail |

> More workflows are added as I build them.

## How to Import a Workflow

1. Open the workflow folder and download its `workflow.json`.
2. In n8n, click the menu (top right) then **Import from File**, and select the JSON.
3. Open each node that needs credentials and connect your own accounts (OpenAI-compatible provider, Google, Airtable, etc.).
4. Replace any placeholders such as `YOUR_API_KEY`, `YOUR_SHEET_ID`, or `owner@example.com` with your own values.
5. Run the workflow with a test execution.

## Repository Structure

```
n8n-workflows/
├── README.md
├── tech-sales-bot/
│   ├── workflow.json
│   ├── README.md
│   └── screenshots and demo images
└── review-sentiment-analyze/
    ├── workflow.json
    ├── README.md
    └── screenshots and sample data
```

## Notes

- API keys and credentials are **not** included in any exported workflow. You need to add your own.
- These workflows are built for learning and practice, and can be adapted to your own use case.

## Author

**Muhammad Nassar**
- GitHub: [@N3ssar](https://github.com/N3ssar)
- Email: n3ssar.swe@gmail.com

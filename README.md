# Jeeves Email Assistant

An n8n workflow for Jeeves, an AI email assistant built with [Letta](https://letta.com), [n8n](https://n8n.io), and [Resend](https://resend.com).

Jeeves processes forwarded emails, drafts replies using a Letta agent with persistent memory, and sends responses via Resend — with an allow list to restrict access to trusted senders.

## Contents

- `jeeves-email-assistant-workflow.json` — the complete eight-node n8n workflow, ready to import

## Usage

See the full tutorial for setup instructions: [Build an AI Email Assistant with Letta, n8n, and Resend](https://techstackups.com)

### Quick start

1. Import `jeeves-email-assistant-workflow.json` into n8n (**three-dot menu → Import from File**)
2. Assign your credentials to the relevant nodes (Resend Webhook Signing Secret, Resend API, Letta Header Auth)
3. Update the agent ID in the HTTP Request node URL and your email addresses in the Check Allow List and Send Reply nodes
4. Publish the workflow

## Requirements

- [n8n](https://n8n.io) with the [n8n-nodes-resend](https://www.npmjs.com/package/n8n-nodes-resend) community node installed
- A [Letta](https://app.letta.com) account and agent
- A [Resend](https://resend.com) account with a verified domain and webhook configured

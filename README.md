# Lead Sniper – High-Value GitHub Lead Tracker

## Overview

This project implements an automated "Lead Sniper" workflow using n8n. The system monitors GitHub repository stargazers, identifies high-value users based on defined criteria, enriches their profile data, and generates a targeted outreach message using AI. The final output is sent to a Slack or Discord channel.

---

## Objective

To build an automation that detects influential GitHub users (potential leads) and generates a personalized sales pitch for outreach.

---

## Workflow Architecture

### 1. Trigger
- Monitors new stargazers for a selected GitHub repository (e.g., `n8n-io/n8n`).
- Implemented using polling or webhook.

### 2. Data Enrichment
- Fetches detailed user profile using:- Extracts key fields such as name, bio, company, followers, and public repositories.

### 3. Filtering Logic
- Identifies high-value leads based on:
- Followers > 100 OR
- Public Repositories > 50
- Only users meeting these conditions proceed further.

### 4. AI Processing
- Uses an AI/LLM node to analyze:
- Bio
- Company
- Generates a one-sentence sales pitch explaining why the user is a valuable lead.

### 5. Output
- Sends a formatted message to Slack or Discord containing:
- Name
- Bio
- Company
- AI-generated sales pitch

---

## Sample Output

---

## Files in Repository

- `weather.json` – Exported n8n workflow file
- `output.png` – Screenshot of successful Slack/Discord message
- `logic-log.md` – Explanation of API rate limit handling
- `README.md` – Project documentation

---

## Logic Log Summary

- Controlled polling intervals were used to avoid excessive API calls.
- Early filtering reduces unnecessary processing.
- Redundant requests were minimized.
- The system can be extended with delay nodes or authentication tokens to further manage GitHub API rate limits.

---

## Demo

A demonstration video showing:
- Workflow execution
- Filtering logic
- Message delivery to Slack/Discord

(Include your Google Drive link in the submission form)

---

## Technologies Used

- n8n (workflow automation)
- GitHub API
- Slack/Discord Webhooks
- AI/LLM Node for text generation

---

## Conclusion

This workflow demonstrates how automation, API integration, and AI can be combined to identify and engage high-value leads efficiently.

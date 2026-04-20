# Pre-Call Automation Calendar and Salesforce Lookup

## Overview

A scheduled pre-call preparation workflow for the Shout About Us team. It reads upcoming Google Calendar events, extracts attendee details, enriches contacts via Apollo, looks up Salesforce interaction history via a sub-workflow, uses AI to generate company descriptions and format pre-call briefings, and updates a Google Doc with the compiled information. It filters out cancelled events and internal emails, and sorts results for easy review.

## How It Works

```
Schedule Trigger -> Get Calendar Events -> Split + Extract Attendees -> Filter cancelled + internal -> Apollo Enrichment -> Salesforce Pre-Call Lookup (sub-workflow) -> AI Company Description -> AI Content Formatter -> Update Google Doc
```

## Integrations

- **Google Calendar** - Event and attendee data
- **Apollo** - Contact enrichment
- **Salesforce** - Interaction history (via sub-workflow)
- **OpenAI** - Company description and content formatting
- **Google Docs** - Pre-call briefing document

## Setup

1. Import `Pre_Call_Automation_Calendar_and_Salesforce_lookup.json` into your n8n instance.
2. Configure all credentials (Google Calendar, Apollo, Salesforce, OpenAI, Google Docs).
3. Ensure the Salesforce Pre-Call sub-workflow is imported.
4. Activate the workflow.

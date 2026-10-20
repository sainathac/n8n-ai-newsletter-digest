# n8n-ai-newsletter-digest

n8n workflow that aggregates AI and tech news from RSS feeds and SerpAPI, generates an AI-powered newsletter digest, and emails it.

## What It Does

Combines TechCrunch RSS, BBC Business RSS, and SerpAPI search results into one aggregated feed, uses Gemini AI to create a structured daily newsletter with AI news highlights, technology updates, and upcoming events — sent to your email.

## Workflow

```
Schedule Trigger -> RSS Read -> Merge -> Aggregate -> Basic LLM Chain -> Send a message
```

## Prerequisites

- **n8n** instance (self-hosted or cloud)
- **Google account** with OAuth2 configured in n8n
- **Google Gemini API** access (via AI Gateway in n8n)
- **SerpAPI** account and API key (get one free at [serpapi.com](https://serpapi.com))
- **Gmail OAuth2** configured in n8n

## Setup

1. **Import the workflow:** Open your n8n instance, go to **Workflows > Import from File**, and select `workflow.json`
2. **Configure credentials:**
   - Set up Google Sheets OAuth2
   - Set up Gmail OAuth2
   - Set up Google Gemini (Palm) API credentials
   - Replace `YOUR_SERPAPI_KEY_HERE` in the workflow with your actual SerpAPI key
- Set up Gmail OAuth2 for sending emails
3. **Update placeholders:**
   - Replace any hardcoded email addresses with your own
   - Replace any Google Sheet IDs with your own sheets
   - Replace `YOUR_SERPAPI_KEY_HERE` with your SerpAPI key
- Update `sainathan2003@gmail.com` with your email
- Update RSS feed URLs if you want different sources
4. **Activate the workflow** and let it run!

## Author

**sainathac** — [GitHub](https://github.com/sainathac)

## License

MIT

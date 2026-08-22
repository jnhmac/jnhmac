## Jonah A.

Marketing operations and automation. Six years running GTM systems in B2B, four of them as sole owner and admin of a HubSpot platform covering automation, CRM, integrations, and pipeline reporting.

These days I don't just run the systems, I build them: Python ETL, Databricks pipelines, REST API integrations, n8n workflows, and scheduled pipelines. The work below is the part I can show publicly.

### Things I have built

**[b2b-lead-enrichment-pipeline](https://github.com/jnhmac/b2b-lead-enrichment-pipeline)**
Turns anonymous website visitors into scored, contact-ready sales leads. Six Python steps chain Leadfeeder, Hunter.io, OpenRouter, and Google Places, then write two linked HubDB tables that a HubSpot CMS page renders with no client-side API calls. Addresses and phone numbers come from regex extraction rather than the LLM, so the model never invents a plausible-looking wrong address. A manual CLI, a dashboard button, and a weekly Cloud Scheduler cron all hit the same FastAPI endpoint on Cloud Run.

**[llm-citation-tracker](https://github.com/jnhmac/llm-citation-tracker)**
Measures how often AI answer engines cite your brand, across ChatGPT, Claude, Perplexity, and Gemini. Config-driven n8n workflow: prompts, tracked domains, engines, and model choices all live in a Google Sheet, so a marketer changes what is measured without anyone touching the automation. Append-only output, per-call cost logging, and error rows that never fake a negative result.

**[market-risk-analytics-engine](https://github.com/jnhmac/market-risk-analytics-engine)**
A Databricks medallion pipeline over 53 years of daily market data, roughly 99,000 rows across 15 tickers. Bronze ingestion is idempotent and grouped by IPO era so a backfill does not waste API budget on date ranges that never existed. Gold produces twelve analytics tables covering Value at Risk, stress-period performance, drawdown, rolling volatility, correlation, and beta. Runs daily on a scheduled job.

### Stack

Python, FastAPI, TypeScript, Next.js, Astro
n8n, Databricks, PySpark, Delta Lake
HubSpot, Google Search Console, GA4, OpenRouter
Firebase, SQLite, Docker, Cloud Run, Caddy, Cloudflare

### Elsewhere

[lmfinder.ai](https://lmfinder.ai) is a directory of LLM tools I am building.

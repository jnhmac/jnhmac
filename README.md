# Jonah A.

**I run marketing operations, automate where I can, and tailor where I have to.**

Six years running GTM systems in B2B, four of them as sole owner and admin of a HubSpot platform covering automation, CRM, integrations, and pipeline reporting. Somewhere in there the job changed: instead of configuring what the tool already did, I started building what it couldn't. Python ETL, Databricks pipelines, REST API integrations, n8n workflows, scheduled jobs.

Five of those systems are public. Each one runs against real data, most of them on a schedule.

---

## 🛠 Selected work

### 🧾 [website-lead-qualifier](https://github.com/jnhmac/website-lead-qualifier)

Goes through a list of company domains, reads each website, and says whether it is a target or not.

![Python](https://img.shields.io/badge/Python-1a56c4?style=flat-square&logo=python&logoColor=white)
![Firecrawl](https://img.shields.io/badge/Firecrawl-1a56c4?style=flat-square)
![Anthropic](https://img.shields.io/badge/Anthropic-1a56c4?style=flat-square&logo=anthropic&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-1a56c4?style=flat-square&logo=pydantic&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-1a56c4?style=flat-square&logo=pytest&logoColor=white)

Six stages crawl a company's site and return a four-way verdict on whether it fits, with the sentence that justifies it. It sits directly upstream of the enrichment pipeline below: identification tells you a company visited, not whether they are worth a salesperson's time, and enrichment is priced per record. Roughly nine crawl credits and ten cents of inference per domain, and 654 tests that run offline with no keys.

> Every claim carries a verbatim quote, and the pipeline checks that quote appears in the stored page before the claim is allowed to count. Accuracy is quoted only from a dual-reader holdout, printed with its interval, 78.3% [58.1, 90.3], because on 23 domains a point estimate on its own is a claim about noise.

---

### 🎯 [b2b-lead-enrichment-pipeline](https://github.com/jnhmac/b2b-lead-enrichment-pipeline)

Anonymous website traffic, turned into scored and contact-ready leads.

![Python](https://img.shields.io/badge/Python-1a56c4?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-1a56c4?style=flat-square&logo=fastapi&logoColor=white)
![Cloud Run](https://img.shields.io/badge/Cloud%20Run-1a56c4?style=flat-square&logo=googlecloud&logoColor=white)
![HubSpot](https://img.shields.io/badge/HubDB-1a56c4?style=flat-square&logo=hubspot&logoColor=white)
![OpenRouter](https://img.shields.io/badge/OpenRouter-1a56c4?style=flat-square)

Six chained steps move a visitor through Leadfeeder, Hunter.io, OpenRouter, and Google Places, then write two linked HubDB tables. A HubSpot CMS page renders them with no client-side API calls. One FastAPI endpoint serves all three triggers: a manual CLI, a dashboard button, and a weekly Cloud Scheduler cron.

> Addresses and phone numbers come from regex extraction, not the LLM. The model never gets the chance to invent a plausible-looking wrong address.

---

### 🔍 [llm-citation-tracker](https://github.com/jnhmac/llm-citation-tracker)

How often AI answer engines cite your brand, measured across ChatGPT, Claude, Perplexity, and Gemini.

![n8n](https://img.shields.io/badge/n8n-1a56c4?style=flat-square&logo=n8n&logoColor=white)
![Python](https://img.shields.io/badge/Python-1a56c4?style=flat-square&logo=python&logoColor=white)
![Google Sheets](https://img.shields.io/badge/Google%20Sheets-1a56c4?style=flat-square&logo=googlesheets&logoColor=white)
![OpenRouter](https://img.shields.io/badge/OpenRouter-1a56c4?style=flat-square)

Prompts, tracked domains, engines, and model choices all live in a Google Sheet. A marketer changes what gets measured without anyone opening the automation.

> Append-only output, per-call cost logging, and error rows that never fake a negative result.

---

### 🔗 [hubspot-broken-link-monitor](https://github.com/jnhmac/hubspot-broken-link-monitor)

Link integrity across a HubSpot CMS site, built during a multi-subdomain to root-domain migration.

![n8n](https://img.shields.io/badge/n8n-1a56c4?style=flat-square&logo=n8n&logoColor=white)
![HubSpot](https://img.shields.io/badge/HubSpot%20CMS%20API-1a56c4?style=flat-square&logo=hubspot&logoColor=white)

It reads pages and posts through the CMS API instead of crawling them, so it sees drafts and theme-module markup a crawler never reaches.

> The useful part is what it refuses to report. The first run flagged 200 broken links. 170 of them were our own server rate-limiting concurrent requests. Throttling to one request per second took verified links from 123 to 318 and the real count to 11. Every run now logs its own false-positive counters.

---

### 📈 [market-risk-analytics-engine](https://github.com/jnhmac/market-risk-analytics-engine)

A Databricks medallion pipeline over 53 years of daily market data: roughly 99,000 rows across 15 tickers.

![Databricks](https://img.shields.io/badge/Databricks-1a56c4?style=flat-square&logo=databricks&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-1a56c4?style=flat-square&logo=apachespark&logoColor=white)
![Delta Lake](https://img.shields.io/badge/Delta%20Lake-1a56c4?style=flat-square)
![Jupyter](https://img.shields.io/badge/Jupyter-1a56c4?style=flat-square&logo=jupyter&logoColor=white)

Gold produces twelve analytics tables covering Value at Risk, stress-period performance, drawdown, rolling volatility, correlation, and beta. Runs daily on a scheduled job.

> Bronze ingestion is idempotent and grouped by IPO era, so a backfill never spends API budget on date ranges that did not exist yet.

---

## ⚙️ Stack

**Languages, frameworks**

![Python](https://img.shields.io/badge/Python-1a56c4?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-1a56c4?style=flat-square&logo=fastapi&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-1a56c4?style=flat-square&logo=typescript&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-1a56c4?style=flat-square&logo=nextdotjs&logoColor=white)
![Astro](https://img.shields.io/badge/Astro-1a56c4?style=flat-square&logo=astro&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-1a56c4?style=flat-square&logo=pydantic&logoColor=white)

**Data, automation**

![n8n](https://img.shields.io/badge/n8n-1a56c4?style=flat-square&logo=n8n&logoColor=white)
![OpenRouter](https://img.shields.io/badge/OpenRouter-1a56c4?style=flat-square)
![Databricks](https://img.shields.io/badge/Databricks-1a56c4?style=flat-square&logo=databricks&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-1a56c4?style=flat-square&logo=apachespark&logoColor=white)
![Delta Lake](https://img.shields.io/badge/Delta%20Lake-1a56c4?style=flat-square)
![Anthropic](https://img.shields.io/badge/Anthropic-1a56c4?style=flat-square&logo=anthropic&logoColor=white)
![Firecrawl](https://img.shields.io/badge/Firecrawl-1a56c4?style=flat-square)

**GTM platforms**

![HubSpot](https://img.shields.io/badge/HubSpot-1a56c4?style=flat-square&logo=hubspot&logoColor=white)
![Google Search Console](https://img.shields.io/badge/Search%20Console-1a56c4?style=flat-square&logo=googlesearchconsole&logoColor=white)
![GA4](https://img.shields.io/badge/GA4-1a56c4?style=flat-square&logo=googleanalytics&logoColor=white)

**Infrastructure**

![Firebase](https://img.shields.io/badge/Firebase-1a56c4?style=flat-square&logo=firebase&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-1a56c4?style=flat-square&logo=sqlite&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-1a56c4?style=flat-square&logo=docker&logoColor=white)
![Cloud Run](https://img.shields.io/badge/Cloud%20Run-1a56c4?style=flat-square&logo=googlecloud&logoColor=white)
![Netlify](https://img.shields.io/badge/Netlify-1a56c4?style=flat-square&logo=netlify&logoColor=white)
![Caddy](https://img.shields.io/badge/Caddy-1a56c4?style=flat-square&logo=caddy&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-1a56c4?style=flat-square&logo=cloudflare&logoColor=white)

---

## 🌐 Elsewhere

[**lmfinder.ai**](https://lmfinder.ai) - a directory of LLM tools, built and maintained by me.

---

Reach me on [**LinkedIn**](https://www.linkedin.com/in/jyakcali/).

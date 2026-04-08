# SEO Optimization Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Transform the CopiioAI GitHub repository into a keyword-rich content hub that captures functional search traffic for natural language internet data access queries.

**Architecture:** One optimized README as the main landing page + 7 topic-specific Markdown docs under `docs/`, each targeting a distinct keyword cluster with real example queries. All files cross-link to each other and to the Chrome extension install page.

**Tech Stack:** Markdown, GitHub repository metadata (description, topics, name), `gh` CLI for repo settings.

---

## Task 1: Update Repository Settings via GitHub CLI

**Files:**
- No files changed (GitHub metadata update)

- [ ] **Step 1: Rename the repository**

```bash
gh repo rename natural-language-interface-for-internet-data
```

Expected output:
```
✓ Renamed repository copiioai/copiioai to copiioai/natural-language-interface-for-internet-data
```

- [ ] **Step 2: Update repository description**

```bash
gh repo edit --description "Access live data from Reddit, financial markets, social media, news, and more — just by asking in plain English. No coding required."
```

Expected output: `✓ Edited repository`

- [ ] **Step 3: Add repository topics**

```bash
gh repo edit --add-topic api-testing --add-topic chrome-extension --add-topic natural-language --add-topic developer-tools --add-topic postman-alternative --add-topic gpt-4 --add-topic ai-tools --add-topic productivity --add-topic devtools
```

Expected output: `✓ Edited repository`

- [ ] **Step 4: Verify settings**

```bash
gh repo view --json name,description,repositoryTopics
```

Expected: name is `natural-language-interface-for-internet-data`, description matches, 9 topics listed.

- [ ] **Step 5: Commit note (no files changed)**

No commit needed for this task — metadata is stored in GitHub, not git.

---

## Task 2: Rewrite README.md

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Verify keyword targets are absent from current README**

```bash
grep -c "real-time\|natural language\|internet data" README.md
```

Expected: low count (current README lacks these phrases in context).

- [ ] **Step 2: Replace README.md with the optimized version**

Write the following content to `README.md`:

```markdown
# CopiioAI — Natural Language Interface for Real-Time Internet Data

> Access live data from Reddit, Hacker News, financial markets, social media trends, and more — just by asking in plain English. No coding required.

[Install Chrome Extension](https://chromewebstore.google.com/detail/copiioai/lejbegpfaanpcilacmakkdediinkmnne) | [Website](https://copiioai.com)

## What You Can Do

CopiioAI connects you to live internet data through natural conversation. Ask anything — get real-time results from the sources you care about.

### 📈 Financial Markets & Economic Data
- *"How much is NVDA stock price?"*
- *"What is the current gold price per ounce?"*
- *"Show me latest Federal Funds Effective Rate"*
- *"What is the exchange rate from USD to EUR?"*
- *"Show me latest US GDP data"*
- *"Show me latest PCE data"*
- *"Show me FRED releases today"*
- *"What are the latest crypto prices?"*
- *"Show me current oil price all around the world"*

### 📰 News & Current Events
- *"Show me latest Hacker News"*
- *"Show me top headlines on Google News"*
- *"Show me New York Times news today"*
- *"Show me top US congressional news"*
- *"What's the latest on CoinDesk?"*
- *"What's the latest on climate change?"*

### 📱 Social Media Trends
- *"Show me TikTok trending posts"*
- *"What's trending on YouTube?"*
- *"Show me Reddit popular posts today"*
- *"Find me Reddit threads about [topic] posted today"*
- *"Show me Spotify top songs"*
- *"Show me Spotify viral tracks"*

### 🎬 Entertainment & Sports
- *"Show me IMDb top 10 movies"*
- *"Show me IMDb top 10 TV series"*
- *"Show me NBA scoreboard"*
- *"Show me latest F1 news"*
- *"Show me latest football news"*

### 🛒 Research & E-commerce
- *"Search PS5 Pro on Amazon"*
- *"Compare price of PS5 Pro"*
- *"Show me top free apps for Android"*
- *"Show me top paid games for Android"*
- *"Show me top 10 unicorn companies"*
- *"Show me top 10 billionaires"*

## How It Works

1. **Ask** — Type your question in plain English
2. **CopiioAI understands** — AI interprets your intent and identifies the right data source
3. **Get live results** — Real-time data fetched directly from the source

No APIs to configure. No code to write. No switching tabs.

## Install

**[→ Add CopiioAI to Chrome](https://chromewebstore.google.com/detail/copiioai/lejbegpfaanpcilacmakkdediinkmnne)** — Free, no credit card required

## Data Sources Covered

**Financial** — Stock prices · Crypto · Forex · FRED · Bloomberg · Seeking Alpha · Oil prices  
**News** — Hacker News · Google News · NYT · CoinDesk · CryptoNews  
**Social Media** — Reddit · TikTok · YouTube · Spotify  
**Entertainment** — IMDb · NBA · NFL · F1 · Music charts  
**E-commerce** — Amazon · Android app rankings · Price comparison

## Documentation

- [Real-Time Financial Market Data](docs/financial-market-data.md)
- [Real-Time News Aggregation](docs/real-time-news.md)
- [Social Media Trends](docs/social-media-trends.md)
- [Entertainment & Sports Data](docs/entertainment-data.md)
- [E-commerce & Market Research](docs/ecommerce-research.md)
- [Postman Alternative](docs/postman-alternative.md)
- [Use Cases](docs/use-cases.md)
```

- [ ] **Step 3: Verify keyword density**

```bash
grep -c "natural language\|real-time\|internet data\|live data" README.md
```

Expected: 5 or more matches.

- [ ] **Step 4: Commit**

```bash
git add README.md
git commit -m "feat: rewrite README with SEO-optimized content and real usage examples"
```

---

## Task 3: Create docs/financial-market-data.md

**Files:**
- Create: `docs/financial-market-data.md`

- [ ] **Step 1: Create the docs directory**

```bash
mkdir -p docs
```

- [ ] **Step 2: Write docs/financial-market-data.md**

```markdown
# Real-Time Financial Market Data with Natural Language

CopiioAI gives you instant access to live financial market data — stock prices, crypto, forex, economic indicators, and more — without writing a single line of code. Just ask in plain English.

## Stock Prices & Market Data

> *"How much is NVDA stock price?"*  
✓ CopiioAI fetches the live NVDA price from financial data sources instantly.

> *"What are the latest crypto prices and market updates?"*  
✓ Real-time prices for Bitcoin, Ethereum, and all major cryptocurrencies.

> *"What's the live price of Ethereum?"*  
✓ Live ETH price with market context, no exchange account needed.

> *"What is the current gold price per ounce?"*  
✓ Spot price for gold, silver, and other commodities in real time.

> *"Show me current oil price all around the world"*  
✓ WTI, Brent, and global crude oil prices in a single query.

> *"What is the exchange rate from USD to EUR?"*  
✓ Live forex rates for any currency pair.

## Economic Indicators & FRED Data

> *"Show me Federal Funds Effective Rate"*  
✓ Direct access to FRED (Federal Reserve Economic Data) in plain English.

> *"Show me latest US GDP data"*  
✓ Most recent GDP figures from official economic sources.

> *"Show me latest US unemployment rate"*  
✓ Current unemployment data, updated as released.

> *"Show me latest DGS10"*  
✓ 10-Year Treasury Constant Maturity Rate, live from FRED.

> *"Show me latest PCE data"*  
✓ Personal Consumption Expenditures — the Fed's preferred inflation measure.

> *"Show me FRED releases today"*  
✓ All economic data releases scheduled for today.

## Financial News & Analysis

> *"Show me latest Bloomberg finance news"*  
✓ Top financial stories from Bloomberg, fetched in real time.

> *"Let me see Seeking Alpha's Wall Street Breakfast"*  
✓ The daily pre-market briefing from Seeking Alpha, on demand.

> *"What hot articles are on Seeking Alpha right now?"*  
✓ Live trending financial analysis and investment articles.

> *"Show me top 10 billionaires"*  
✓ Real-time net worth rankings from live financial data.

## Why CopiioAI for Financial Data

Unlike general AI assistants, CopiioAI accesses **live data sources** — not training data frozen at a cutoff date. You get real prices, current indicators, and today's news — not last year's figures.

**[→ Install CopiioAI Free](https://chromewebstore.google.com/detail/copiioai/lejbegpfaanpcilacmakkdediinkmnne)**

---

← [Back to README](../README.md) | [More Use Cases](use-cases.md)
```

- [ ] **Step 3: Verify primary keyword present**

```bash
grep -c "real-time financial\|natural language\|live.*data" docs/financial-market-data.md
```

Expected: 3 or more matches.

- [ ] **Step 4: Commit**

```bash
git add docs/financial-market-data.md
git commit -m "feat: add financial market data SEO doc covering FRED, crypto, forex, Bloomberg"
```

---

## Task 4: Create docs/real-time-news.md

**Files:**
- Create: `docs/real-time-news.md`

- [ ] **Step 1: Write docs/real-time-news.md**

```markdown
# Real-Time News Access with Natural Language AI

CopiioAI pulls live news from across the web — tech, politics, finance, crypto, climate, and more — the moment you ask. No news app switching, no RSS feeds to manage.

## Tech & Developer News

> *"Show me latest Hacker News"*  
✓ Top stories from Hacker News right now, with links and rankings.

## General News

> *"Show me top headlines on Google News"*  
✓ Breaking news across categories from Google News, live.

> *"Show me New York Times news today"*  
✓ Today's top stories from the NYT, fetched in real time.

> *"Show me top US congressional news"*  
✓ Latest political and legislative news from Capitol Hill.

> *"What's the latest on climate change?"*  
✓ Most recent climate and environmental news from major sources.

> *"Show me latest movie news"*  
✓ Box office updates, trailers, and entertainment headlines.

## Crypto & Financial News

> *"What's the latest on CoinDesk?"*  
✓ Live cryptocurrency news and market commentary from CoinDesk.

> *"What's the latest on CryptoNews?"*  
✓ Breaking crypto stories, token news, and DeFi updates.

> *"What's the latest on The Defiant?"*  
✓ DeFi-focused news and analysis from The Defiant.

## Why CopiioAI for News

Standard AI tools only know what they were trained on. CopiioAI reads **today's actual content** — the article published an hour ago, the headline that just broke. It's the difference between asking someone who read the news this morning vs. someone who hasn't read it in a year.

**[→ Install CopiioAI Free](https://chromewebstore.google.com/detail/copiioai/lejbegpfaanpcilacmakkdediinkmnne)**

---

← [Back to README](../README.md) | [Financial Data](financial-market-data.md) | [More Use Cases](use-cases.md)
```

- [ ] **Step 2: Verify primary keyword present**

```bash
grep -c "real-time\|live.*news\|natural language" docs/real-time-news.md
```

Expected: 3 or more matches.

- [ ] **Step 3: Commit**

```bash
git add docs/real-time-news.md
git commit -m "feat: add real-time news SEO doc covering Hacker News, Google News, CoinDesk"
```

---

## Task 5: Create docs/social-media-trends.md

**Files:**
- Create: `docs/social-media-trends.md`

- [ ] **Step 1: Write docs/social-media-trends.md**

```markdown
# Real-Time Social Media Trends with Natural Language

Track what's trending on Reddit, TikTok, YouTube, and Spotify — without opening each app. CopiioAI aggregates live social data in one conversational interface.

## Reddit

> *"Show me Reddit popular posts today"*  
✓ Top posts across Reddit right now, with upvotes and links.

> *"What's trending on Reddit today?"*  
✓ Rising and hot posts across all major subreddits.

> *"Find me Reddit threads about 'topic' posted today"*  
✓ Search Reddit for any topic, filtered to today's posts.

> *"Go find [anything] on Reddit"*  
✓ Natural language Reddit search — no need to know subreddit names.

## TikTok

> *"Show me TikTok trending posts"*  
✓ What's going viral on TikTok right now.

## YouTube

> *"What's trending on YouTube?"*  
✓ YouTube's trending videos, live from the platform.

## Music & Spotify

> *"Show me Spotify top songs"*  
✓ Current Spotify Global Top 50, updated daily.

> *"Show me Spotify viral tracks"*  
✓ Songs going viral on Spotify right now.

> *"Show me Spotify top 10 artists"*  
✓ Most-streamed artists on Spotify at this moment.

> *"Show me music trending"*  
✓ Cross-platform music trends from Spotify and charts.

## Why CopiioAI for Social Trends

Social media trends move fast. CopiioAI gives you a live pulse on multiple platforms at once — without logging into each one or fighting algorithmic feeds.

**[→ Install CopiioAI Free](https://chromewebstore.google.com/detail/copiioai/lejbegpfaanpcilacmakkdediinkmnne)**

---

← [Back to README](../README.md) | [News](real-time-news.md) | [Entertainment](entertainment-data.md)
```

- [ ] **Step 2: Verify primary keyword present**

```bash
grep -c "real-time\|natural language\|trending" docs/social-media-trends.md
```

Expected: 4 or more matches.

- [ ] **Step 3: Commit**

```bash
git add docs/social-media-trends.md
git commit -m "feat: add social media trends SEO doc covering Reddit, TikTok, YouTube, Spotify"
```

---

## Task 6: Create docs/entertainment-data.md

**Files:**
- Create: `docs/entertainment-data.md`

- [ ] **Step 1: Write docs/entertainment-data.md**

```markdown
# Live Entertainment & Sports Data with Natural Language

Movies, TV, sports scores, music, racing — get real-time entertainment data by simply asking CopiioAI.

## Movies & TV (IMDb)

> *"Show me IMDb top 10 movies"*  
✓ Current IMDb top-rated movies, live from the platform.

> *"Show me IMDb top 10 TV series"*  
✓ Top-rated TV shows on IMDb right now.

> *"I want to look up film news on IMDb"*  
✓ Latest movie news, casting announcements, and release updates from IMDb.

## Sports

> *"Show me NBA scoreboard"*  
✓ Live NBA game scores and results for any date.

> *"Show me latest football news"*  
✓ Breaking football news — transfers, results, and standings.

> *"Show me latest F1 news"*  
✓ Formula 1 race results, team news, and championship standings.

## Why CopiioAI for Entertainment

No more switching between IMDb, ESPN, and sports apps. Ask once, get live data from the right source automatically.

**[→ Install CopiioAI Free](https://chromewebstore.google.com/detail/copiioai/lejbegpfaanpcilacmakkdediinkmnne)**

---

← [Back to README](../README.md) | [Social Media Trends](social-media-trends.md) | [More Use Cases](use-cases.md)
```

- [ ] **Step 2: Verify primary keyword present**

```bash
grep -c "natural language\|live\|real-time" docs/entertainment-data.md
```

Expected: 3 or more matches.

- [ ] **Step 3: Commit**

```bash
git add docs/entertainment-data.md
git commit -m "feat: add entertainment & sports SEO doc covering IMDb, NBA, F1, football"
```

---

## Task 7: Create docs/ecommerce-research.md

**Files:**
- Create: `docs/ecommerce-research.md`

- [ ] **Step 1: Write docs/ecommerce-research.md**

```markdown
# Natural Language Product Research & E-commerce Data

Search Amazon, compare prices, track app rankings, and research markets — all in plain English with CopiioAI.

## Amazon & Shopping

> *"Search PS5 Pro on Amazon"*  
✓ Live Amazon search results for any product, with prices and links.

> *"Compare price of PS5 Pro"*  
✓ Price comparison across sources for any product.

> *"Can you run the VIN [number] and tell me what it's worth?"*  
✓ Vehicle valuation by VIN number, fetched in real time.

## Android App Rankings

> *"Show me top free apps for Android"*  
✓ Google Play Store top free apps, live rankings.

> *"Show me top paid apps for Android"*  
✓ Current top paid apps on Google Play.

> *"Show me top free games for Android"*  
✓ Most downloaded free games on Android right now.

> *"Show me top paid games for Android"*  
✓ Best-selling paid games on Google Play.

> *"Show me top grossing games for Android"*  
✓ Highest revenue games on the Play Store.

## Market & Business Intelligence

> *"Show me top 10 unicorn companies"*  
✓ Current list of the world's top unicorn startups by valuation.

> *"Show me top 10 billionaires"*  
✓ Real-time billionaire rankings by net worth.

## Other

> *"What does today's horoscope say for Taurus?"*  
✓ Daily horoscope for any sign, fetched fresh each day.

## Why CopiioAI for Research

Replace manual tab-switching with a single conversational interface. CopiioAI knows where to look — you just ask.

**[→ Install CopiioAI Free](https://chromewebstore.google.com/detail/copiioai/lejbegpfaanpcilacmakkdediinkmnne)**

---

← [Back to README](../README.md) | [Financial Data](financial-market-data.md) | [More Use Cases](use-cases.md)
```

- [ ] **Step 2: Verify primary keyword present**

```bash
grep -c "natural language\|live\|real-time" docs/ecommerce-research.md
```

Expected: 3 or more matches.

- [ ] **Step 3: Commit**

```bash
git add docs/ecommerce-research.md
git commit -m "feat: add e-commerce research SEO doc covering Amazon, Android rankings, unicorns"
```

---

## Task 8: Create docs/postman-alternative.md

**Files:**
- Create: `docs/postman-alternative.md`

- [ ] **Step 1: Write docs/postman-alternative.md**

```markdown
# CopiioAI as a Postman Alternative: Natural Language API Access

Postman is powerful — but it requires knowing the endpoint, parameters, authentication headers, and response structure before you can make a single request. CopiioAI flips this: describe what you want, and it handles the rest.

## The Difference

| | Postman | CopiioAI |
|---|---|---|
| Input | Endpoint URL + parameters | Plain English question |
| Auth setup | Manual | Automatic |
| Learning curve | High | Zero |
| Who can use it | Developers | Anyone |
| Data freshness | Depends on your setup | Always live |

## When to Use CopiioAI Instead of Postman

**Quick lookups** — When you need one answer fast and don't want to open a tool, configure auth, and craft a request.

**Non-technical users** — PMs, analysts, and support teams who need data access without engineering help.

**Exploratory data access** — When you're not sure which endpoint to call, CopiioAI figures it out from your question.

**Real-time public data** — Financial data, news, social trends, and more, without any API key setup.

## Example: The Same Task, Two Ways

**Postman:**
1. Open Postman
2. Create new request
3. Find the correct API endpoint
4. Add authentication headers
5. Set query parameters
6. Send request
7. Parse JSON response

**CopiioAI:**
> *"Show me latest Hacker News"*  
Done.

## Who Uses CopiioAI

- **Developers** — quick data lookups without context-switching
- **Product managers** — check data without filing engineering requests
- **Customer support** — live lookups without SQL access
- **Analysts** — financial and market data on demand

**[→ Install CopiioAI Free](https://chromewebstore.google.com/detail/copiioai/lejbegpfaanpcilacmakkdediinkmnne)**

---

← [Back to README](../README.md) | [Use Cases](use-cases.md)
```

- [ ] **Step 2: Verify primary keyword present**

```bash
grep -c "postman\|natural language\|alternative" docs/postman-alternative.md
```

Expected: 5 or more matches.

- [ ] **Step 3: Commit**

```bash
git add docs/postman-alternative.md
git commit -m "feat: add Postman alternative SEO doc with direct comparison table"
```

---

## Task 9: Create docs/use-cases.md

**Files:**
- Create: `docs/use-cases.md`

- [ ] **Step 1: Write docs/use-cases.md**

```markdown
# CopiioAI Use Cases: Natural Language Internet Data Access

CopiioAI is a Chrome extension that gives you a natural language interface to live internet data. Here's how different people use it.

## For Developers

**Problem:** Switching between browser, terminal, Postman, and documentation to look up data breaks focus.

**With CopiioAI:**
- Look up live API data without leaving the browser
- Explore financial, social, and news data sources instantly
- Replace ad-hoc scripts with plain English queries

**Example queries:**
- *"Show me FRED releases today"*
- *"What's the live price of Ethereum?"*
- *"Find me Reddit threads about [topic] posted today"*

## For Financial Analysts

**Problem:** Checking multiple dashboards (Bloomberg, FRED, Seeking Alpha) for data points takes time and context.

**With CopiioAI:**
- Pull economic indicators, stock prices, and market news in one place
- Track multiple data sources without switching tabs
- Get live data — not AI-hallucinated estimates

**Example queries:**
- *"Show me latest PCE data"*
- *"Show me Federal Funds Effective Rate"*
- *"What hot articles are on Seeking Alpha right now?"*

## For Product Managers

**Problem:** Needing data from engineering every time you want to check live metrics or market conditions.

**With CopiioAI:**
- Self-serve access to live internet data
- Check market trends, competitor activity, and news independently
- No API keys, no coding, no waiting

**Example queries:**
- *"Show me top 10 unicorn companies"*
- *"Show me top free apps for Android"*
- *"What's trending on Reddit today?"*

## For Content & Marketing Teams

**Problem:** Manually checking trending topics across platforms is slow and inconsistent.

**With CopiioAI:**
- Monitor social trends across Reddit, TikTok, YouTube, and Spotify in real time
- Track news cycles from multiple sources simultaneously
- Identify trending topics before they peak

**Example queries:**
- *"What's trending on YouTube?"*
- *"Show me TikTok trending posts"*
- *"Show me Spotify viral tracks"*

## For General Users

Anyone who wants live internet data without searching through multiple sites:

- *"Show me NBA scoreboard"*
- *"Show me IMDb top 10 movies"*
- *"What does today's horoscope say for Taurus?"*
- *"Show me latest F1 news"*

**[→ Install CopiioAI Free](https://chromewebstore.google.com/detail/copiioai/lejbegpfaanpcilacmakkdediinkmnne)**

---

← [Back to README](../README.md)
```

- [ ] **Step 2: Verify keyword and persona coverage**

```bash
grep -c "natural language\|live\|real-time\|developer\|analyst\|product manager" docs/use-cases.md
```

Expected: 8 or more matches.

- [ ] **Step 3: Commit**

```bash
git add docs/use-cases.md
git commit -m "feat: add use cases SEO doc covering developers, analysts, PMs, marketers"
```

---

## Task 10: Final Cross-Link Verification

**Files:**
- Read: all files under `docs/`
- Read: `README.md`

- [ ] **Step 1: Verify all docs/ links in README resolve**

```bash
for f in docs/financial-market-data.md docs/real-time-news.md docs/social-media-trends.md docs/entertainment-data.md docs/ecommerce-research.md docs/postman-alternative.md docs/use-cases.md; do
  [ -f "$f" ] && echo "✓ $f" || echo "✗ MISSING: $f"
done
```

Expected: all 7 lines show ✓.

- [ ] **Step 2: Verify all docs link back to README**

```bash
grep -l "\.\./README\.md" docs/*.md
```

Expected: all 7 docs files listed.

- [ ] **Step 3: Verify Chrome Web Store link present in all files**

```bash
grep -l "chromewebstore.google.com" README.md docs/*.md
```

Expected: 8 files (README + 7 docs).

- [ ] **Step 4: Final commit**

```bash
git add -A
git commit -m "feat: complete SEO content structure with cross-linked docs"
```

- [ ] **Step 5: Push to GitHub**

```bash
git push origin main
```

Expected: push succeeds, all files visible on GitHub.

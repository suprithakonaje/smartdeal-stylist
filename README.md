# SmartDeal Stylist 🛍️✨

A personal AI stylist and deal alert agent because finding great deals on women's 
apparel from trusted brands should not require hours of googling.

## The Problem

Sites like Zara, H&M, and Mango have great products but terrible deal visibility. 
Generic deal aggregators like Slickdeals are not built for fashion. I wanted one place 
that tracks deals from brands I actually trust, learns my style, and tells me when 
something I want goes on sale.

So I built it.

## What It Does

### Phase 1 - Deal Aggregation (in progress)
- Scrapes deals and catalogues from targeted, trusted fashion sites using 
  BeautifulSoup
- Aggregates everything into one place so you never miss a sale

### Phase 2 - Personal Stylist (planned)
- Ask natural language questions like "I want a dress similar to this" and get 
  recommendations from trusted sites
- RAG based recommendation system built on FAISS vector search
- Learns your style over time like body type, preferred fits, jewellery style, 
  past searches

### Phase 3 - Smart Alerts (planned)
- Email alerts via Gmail SMTP when a monitored item drops in price
- Alerts when a previously unavailable item matching your search appears
- Track items across sessions so nothing slips through

#### Price Adjustment Tracker (future consideration)
 
Many retailers offer price adjustment policies. If a price drops within a set number of days after purchase, you can claim a refund of the difference. This feature would automate that entire process.
 
**How it would work:**
 
1. User clicks a deal and is redirected to the retailer via a tracked link
2. After purchasing, user logs the order in the app with one tap (store, item, price paid, date)
3. A background watcher re-scrapes that specific product URL every 12–24 hours
4. If the price drops and the purchase is still within the store's adjustment window, the user gets an alert
5. The alert includes the savings amount and exactly how to claim like chatbot link, email address, or phone number depending on the store

**Store policies tracked:**
 
| Store | Adjustment Window | How to Claim |
|-------|------------------|--------------|
| Macy's | 10 days | Live chat or 1-800 number |
| Zara | 14 days | Online CS or in-store |
| Nordstrom | 14 days | Chat, phone, or in-store |
| H&M | No formal policy | Not eligible |
 
> Inspired by a real experience: Bought some shoe at Macy's for a price, spotted two consecutive price drops within the adjustment window, and claimed refunds both times through their CS chat. This feature would catch that automatically.

### Phase 4 - Autonomous Shopping Agent (future)
- PayPal integration for autonomous purchasing
- Smart return policy checker before placing any order
- Purchase categories: "buy now", "buy if price drops by X%"
- Never buy something you no longer need

## Tech Stack
- Python
- BeautifulSoup - web scraping and catalogue aggregation
- FAISS - vector search for recommendations
- HuggingFace / Claude API - LLM powered styling and recommendations
- Gmail SMTP - email alerts
- Jupyter Notebook - development and experimentation

## Project Status
Active development: currently building the deal scraping and catalogue 
aggregation layer

## Why I Built This
I moved to the US recently and was immediately frustrated by how hard it was to 
discover deals on the brands I love. Slickdeals exists but is not built for women's 
fashion. So I started building my own solution, one that actually knows my style, 
monitors what I care about, and does the work for me.

## Roadmap
- [x] Project setup and planning
- [ ] Scrape catalogues from target sites
- [ ] Build deal aggregation pipeline
- [ ] Add FAISS based recommendation system
- [ ] Implement email alert system
- [ ] Add autonomous purchasing agent with return policy checking

## About
Built by Supritha Konaje - AI/ML Engineer based in the San Francisco Bay Area

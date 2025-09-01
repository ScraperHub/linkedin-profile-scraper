<a href="https://crawlbase.com/signup?utm_source=github&utm_medium=readme&utm_campaign=crawling_api_banner" target="_blank">
  <img src="https://github.com/user-attachments/assets/afa4f6e7-25fb-442c-af2f-b4ddcfd62ab2" 
       alt="crawling-api-cta" 
       style="max-width: 100%; border: 0;">
</a>

# 🔗 LinkedIn Profile Scraper with Crawlbase

## 📝 Description

This repository provides a Python-based solution to scrape detailed public LinkedIn profile data using the [Crawlbase Crawling API](https://crawlbase.com/crawling-api-avoid-captchas-blocks).

It includes:

    - A scraper that sends asynchronous requests to extract profile data.
    - A retrieval script that fetches the final structured data using the request ID (RID).

📖 Read the full tutorial: [How to Scrape LinkedIn](https://crawlbase.com/blog/how-to-scrape-linkedin/)

## 🔧 Tools Used

- [`crawlbase`](https://pypi.org/project/crawlbase/) – for accessing Crawling and Storage APIs
- `json` – for working with JSON responses
- `Python 3.6+`

## 📦 Installation

Install the required package:

```bash
pip install crawlbase
```

## 🚀 Scraper: LinkedIn Profile Scraper

**File:** linkedin_profile_scraper.py

### ✅ What It Does

- Sends an asynchronous scraping request to a public LinkedIn profile URL.
- Returns a rid (request ID) used to retrieve the data later.

### ⚙️ How to Run

1. Replace YOUR_API_TOKEN with your Crawlbase token.
2. Set the LinkedIn profile URL.

```bash
python linkedin_profile_scraper.py
```

### 🧪 Sample Output

```json
{
	"rid": "1dd4453c6f6bd93baf1d7e03"
}
```

## 📄 Retrieval: Get Scraped Data

**File:** linkedin_profile_retrieve.py

### ✅ What It Does

Uses the rid from the scraper to fetch and print the structured LinkedIn profile data.

### ⚙️ How to Run

Replace `YOUR_API_TOKEN` and` RID` in the script.

```bash
python linkedin_profile_retrieve.py
```

### 🧪 Sample Output

```json
{
  "title": "Kaitlyn Owen",
  "headline": "",
  "sublines": ["Miami-Fort Lauderdale Area", "5K followers", "500+ connections"],
  "location": "Miami-Fort Lauderdale Area",
  ...
}
```

## 📌 To-Do

- Add batching for scraping multiple profile URLs
- Save scraped data to CSV or JSON
- Add command-line interface (CLI) support
- Retry mechanism for failed requests

## 💡 Why Scrape LinkedIn?

- Track hiring trends and talent movement
- Gather public profile data for market research
- Build datasets for recruitment or networking tools

# Smart_Deal_AI
SmartDeal AI is an experimental project that tracks and predicts product prices using real e-commerce data. it scrapes prices from sites like Trendyol, Hepsiburada, and Amazon, cleans and stores them, then applies machine learning models to forecast future price movements and computes RMSE for evaluation, and suggests “buy now” or “wait” decisions.

## Experimental Architecture (Training Version)
### 🎯 Objective
Build a working prototype that:
- Scrapes price/time data for selected products.
- Cleans and stores data.
- Trains and evaluates predictive models (ARIMA / Prophet / XGBoost).
- Displays trends and predictions on a minimal dashboard.

### 1. Data Pipeline
#### Step 1 — Scraping
- Tools: Python, Requests/BeautifulSoup or Selenium.
- Sources: Trendyol, Hepsiburada, Amazon (1–3 categories max).
- Data Fields: product_name, brand, category, price, rating, timestamp, url
- Storage: Raw CSVs (later PostgreSQL).
#### Step 2 — Data Cleaning
- Library: Pandas.
- Handle duplicates, convert timestamps, fill missing values.
- Normalize price units (₺ / USD).
- Export as clean_prices.csv.

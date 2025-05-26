# federal_reg_analysis
# Federal Regulation Analysis App

Analyze U.S. federal regulations by agency using modern web tools and metrics to support decision-making and potential deregulation efforts.

---

Purpose

This project analyzes the Code of Federal Regulations (eCFR) by agency to uncover trends, word counts, redundancy, and other metrics. The goal is to provide digestible insights into the large agencies of federal regulations.

---

## Features

- **Word Count per Agency**
- **Historical Change Tracker**
- **Checksums** for content verification
- **Custom Metric**: Redundancy Score
- **Top Terms & N-Grams** per agency
- **Search and Filter Agencies**
- **Export to PDF** using `react-to-print`

---

## Tech Stack

- **Backend:** FastAPI, SQLAlchemy, SQLite, Playwright
- **Frontend:** React, Axios, Recharts
- **Scraping:** Playwright + Custom Extractor
- **Data Source:** [https://www.ecfr.gov](https://www.ecfr.gov)

---

## ⚙️ Setup Instructions

### 1. Clone Repo
```bash
git clone https://github.com/YOUR_USERNAME/federal_reg_analysis.git
cd federal_reg_analysis

cd backend
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt

#Run scraper 
python scrape_and_load.py

#Start API
uvicorn app.main:app --reload

cd frontend
npm install
npm start

http://localhost:3000

federal_reg_analysis/
├── backend/
│   ├── app/
│   ├── scripts/
│   ├── ecfr.db
│   ├── scrape_and_load.py
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json


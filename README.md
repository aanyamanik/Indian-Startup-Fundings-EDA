# Indian Startup Funding EDA

## Overview
This project explores Indian startup funding data (2015-2020), identifying which cities lead in startup funding activity. It also served as practice for handling real-world data quality issues — encoding errors, inconsistent formatting, and intentionally undisclosed values — using a manually uploaded dataset (not sourced via API).

## Dataset
Indian Startup Funding dataset (Kaggle) — includes startup name, industry, city, investors, funding type, and amount for ~3000 funding deals.

## Key Findings
- **Bengaluru leads by a wide margin** — 842 funding deals, more than Mumbai (563) and New Delhi (424) combined
- **Delhi NCR's combined strength** — New Delhi and Gurugram together rival Mumbai's funding activity
- **~32% of deals have undisclosed funding amounts** — a genuine data limitation, left as missing rather than estimated

## Data Cleaning Highlights
- Parsed inconsistent date formats (day-first), dropped 8 unparseable entries
- Cleaned currency formatting (removed commas) before converting to numeric
- Fixed double-escaped encoding corruption in city names
- Standardized major city name duplicates (e.g., Bangalore → Bengaluru, Gurgaon → Gurugram)
- Identified Industry Vertical column as too inconsistent for reliable analysis within this project's scope — excluded rather than force-cleaned

## Tools Used
Python · Pandas · Matplotlib · Seaborn · Google Colab

## How to Run
1. Download the dataset from Kaggle
2. Upload `startup_funding.csv` to your Colab session
3. Run `startup_funding-EDA.ipnyb`...

# 🛒 Gamezone Orders Data Cleaning Project

This project focuses on cleaning a simulated e-commerce orders dataset ("Gamezone Orders") to prepare it for future analysis. The main goal is to ensure **data integrity, transparency, and traceability**, especially when working with incomplete or ambiguous records — a key skill in consulting and decision-making environments.

---

## 📁 Project Structure

- [README.md](README.md) – Project overview and documentation
- [data/](data/) – Dataset files
  - [gamezone_orders_raw.xlsx](data/gamezone_orders_raw.xlsx)
  - [gamezone_orders_cleaned_2025-06-19.xlsx](data/gamezone_orders_cleaned_2025-06-19.xlsx)
- [log/](log/) – Data quality logs
  - [Issue_log.xlsx](log/Issue_log.xlsx)
- [notebook/](notebook/) – Analysis notebooks (currently empty)

---

### 📁 Folder Tree
```
root/
├── README.md
├── data/
│ ├── gamezone_orders_raw.xlsx
│ └── gamezone_orders_cleaned_2025-06-19.xlsx
├── log/
│ └── Issue_log.xlsx
└── notebook/
```

---

## 📊 Dataset Overview

- **Source**: Public dataset from Christine Jiang’s YouTube course
- **Rows**: 5,797
- **Key Columns**:

  - `PURCHASE_TS`, `SHIP_TS`, `PURCHASE_TS_CLEANED`

  - `PRODUCT_NAME_CLEANED`, `PRODUCT_ID`, `USD_PRICE`

  - `PURCHASE_PLATFORM`, `MARKETING_CHANNEL_CLEANED`

  - `ACCOUNT_CREATION_METHOD_CLEANED`, `COUNTRY_CODE`, `REGION_CLEANED`

  - `ORDER_ID`, `USER_ID`

---

## 🧹 Cleaning Summary

- Timestamps were initially inconsistent in format. These were standardised into a clean dd/mm/yyyy format under the new PURCHASE_TS_CLEANED column.

- Product names contained variations in phrasing (e.g., "27 inches 4k gaming monitor" vs "27in 4K gaming monitor"). These were unified for consistency and reliable grouping.

- Marketing channel and account creation method columns included missing values. Cleaned versions were created with "Unknown" as a placeholder where necessary, preserving the distinction between known and unknown entries.

- Country codes included several blanks and non-inferable entries. These were either left missing or mapped into a new REGION_CLEANED column using a manual reference table.

- A duplicate check on ORDER_ID was conducted using a pivot table. Valid duplicates were retained; potential anomalies were flagged in the log for transparency.

📝 All issues and decisions documented in `gamezone_data_issues_log.xlsx`.

---

## ✅ Next Steps

This dataset is now ready for further analysis. Possible directions:
- Revenue & transaction trend analysis
- High-value customer segmentation
- Regional sales breakdown dashboards

---

## 📦 Requirements

- Microsoft Excel or similar spreadsheet tool
- *(Optional)* Python + `pandas` (for automation)

---

## 📚 Data Source & Attribution

Dataset used in this project was made available for public learning by **Christine Jiang** via YouTube:

- 🎥 [Watch the video](https://www.youtube.com/watch?v=y9wFFD2bXQM)  
- 📺 Channel: [@christinejiangdata](https://www.youtube.com/@christinejiangdata)

Dataset was distributed through her [Analytics Accelerator Kit](https://the-analytics-accelerator.kit) and is intended for **educational & portfolio use only**.

---

## 📜 License

This project is open for **non-commercial, educational** use only. Please credit the original dataset creator, Christine Jiang, if you reference or reuse this repository.
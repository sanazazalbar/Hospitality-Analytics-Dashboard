# 🏨 Hotel Hospitality Data Analysis
**Python (EDA + Data Cleaning) | Power BI Dashboard**

A full-cycle data analytics project on hotel booking data — 
covering data cleaning, exploratory data analysis, and an 
interactive 4-page Power BI dashboard.

---

## 📁 Project Structure
```
├── hospitality.xlsx              # Raw dataset
├── FinalProject.ipynb            # Data cleaning notebook
├── FinalProjectAnalysis.ipynb    # EDA & visualization notebook
├── hotel.pbix                    # Power BI dashboard

```             

---

## 📊 Dataset — Real Numbers
- **1,080 hotel bookings | 27 columns**
- **6 cities:** Bangalore, Hyderabad, Pune, Goa, Delhi, Mumbai
- **3 room types:** Standard, Deluxe, Suite
- **4 booking channels:** Website, Agent, OTA, Direct
- **4 services:** SPA, Room Service, Tour, Breakfast

---

## 🔧 Phase 1 — Data Cleaning (FinalProject.ipynb)

**Missing values treated across 8 columns:**

| Column | Missing | Treatment |
|---|---|---|
| Service Used | 145 | Filled with "No Service" |
| Guest Rating | 73 | Filled with column mean |
| Room Type | 35 | Filled with "Standard" |
| Guest Name | 34 | Filled with default |
| Location | 32 | Filled with "Unknown" |
| Room Rate / Revenue / Cost | 50 each | Mean/median/derived |

**Text standardization across 5 columns:**
- Room Type: 10 inconsistent values → 3 clean categories
- Service Used: 7 variants → 4 clean categories
- Booking Channel: 5 variants → 4 clean categories
- Status: 4 variants → 3 clean categories
- Guest Name: title-cased

**Feature Engineering:**
- Derived `Total Revenue` = Room Rate × Nights Stayed
- Derived `Profit` = Total Revenue − Operating Cost
- Added `Review Category` using pd.cut() on Guest Rating
- Added `Month`, `Year`, `Weekday` columns

---

## 📈 Phase 2 — EDA & Analysis (FinalProjectAnalysis.ipynb)

### 📌 KPIs
| Metric | Value |
|---|---|
| Total Bookings | **1,080** |
| Total Revenue | **₹7,84,211** |
| Avg Revenue per Booking | **₹726** |
| Average Guest Rating | **3.68 / 5** |
| Average Room Rate | **₹186.1/night** |

### 📌 Booking Status
| Status | Count | % |
|---|---|---|
| Confirmed | 532 | 49.3% |
| Pending | 281 | 26.0% |
| Cancelled | 267 | 24.7% |

### 📌 Revenue by City (Top → Bottom)
| City | Revenue |
|---|---|
| Pune | ₹1,39,971 |
| Delhi | ₹1,32,923 |
| Bangalore | ₹1,29,084 |
| Hyderabad | ₹1,25,223 |
| Mumbai | ₹1,22,807 |
| Goa | ₹1,09,717 |

### 📌 Revenue by Room Type
| Room Type | Revenue |
|---|---|
| Deluxe | ₹2,71,334 |
| Standard | ₹2,59,083 |
| Suite | ₹2,31,881 |

### 📌 Top Booking Channel
Website — 439 bookings (40.6%)

### 📌 Most Used Service
SPA — 317 bookings | Room Service — 307

### 📌 Peak Booking Day
Wednesday (178) followed by Thursday (172)

### 📌 Outlier Detection
8 revenue outliers detected using IQR method

### Visualizations Created (8 charts)
Bar chart, Pie chart, Line chart, Bar chart,
Histogram, Boxplot, Bar chart, Bar chart

---

## 📊 Phase 3 — Power BI Dashboard (hotel.pbix)
4-page interactive dashboard:
- **Executive Summary** — KPIs overview
- **Operations** — Booking status & channel analysis
- **Guest Analytics** — Demographics & satisfaction
- **Financial** — Revenue, cost & profit breakdown

## 📸 Dashboard Preview
![Executive](executive.jpg)
![Operations](Operations.jpg)
![Guest Analytics](GuestAnalytics.jpg)
![Financial](Financial.jpg)

---

## 🛠 Tech Stack
Python | Pandas | Matplotlib | NumPy | Jupyter Notebook | Power BI | Excel

---

## 🚀 Getting Started
1. Run `FinalProject.ipynb` → generates cleaned CSV
2. Run `FinalProjectAnalysis.ipynb` → EDA & charts
3. Open `hotel.pbix` in Power BI Desktop






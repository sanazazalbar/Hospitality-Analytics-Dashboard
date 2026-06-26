# 🏨 Hotel Hospitality Data Analysis

A full-cycle data analytics project on hotel booking and guest data — covering data cleaning, exploratory analysis, and interactive visualization via a Power BI dashboard.

---

## 📁 Project Structure

```
├── hospitality.xlsx              # Raw dataset
├── FinalProject.ipynb            # Data cleaning notebook
├── FinalProjectAnalysis.ipynb    # EDA & visualization notebook
├── hotel.pbix                    # Power BI dashboard
└── README.md
```

---

## 📊 Dataset Overview

The raw dataset (`hospitality.xlsx`) contains hotel booking records with the following fields:

| Column | Description |
|---|---|
| Booking ID / Guest ID | Unique identifiers |
| Guest Name, Age, Gender, Country | Guest demographics |
| Room Type | Standard, Deluxe, Suite |
| Service Used | SPA, Room Service, Tour, etc. |
| Location | Bangalore, Hyderabad, Pune, Goa, etc. |
| Booking Channel | Agent, OTA, Website, Direct |
| Status | Confirmed, Pending, Cancelled |
| Check In / Check Out Date | Stay dates |
| Night Stays | Duration of stay |
| Guest Rating / Room Rate | Ratings and room pricing |
| Total Revenue / Operating Cost / Profit | Financial metrics |
| Purpose of Visit | Business, Leisure, Family |
| Guest Type | New / Returning |
| Payment Method | UPI, Cash, Credit/Debit Card |
| Review Category | Poor, Average, Good, Excellent |

---

## 🔧 Phase 1 — Data Cleaning (`FinalProject.ipynb`)

Key cleaning steps performed:

- Removed duplicate records
- Standardized text fields (Guest Name, Room Type, Service Used, Booking Channel, Status)
- Handled missing values:
  - **Guest Rating & Room Rate** → filled with column mean
  - **Total Revenue** → derived from Room Rate × Nights Stayed
  - **Operating Cost** → filled with median
  - **Profit** → recalculated as Total Revenue − Operating Cost
  - **Room Type, Location, Service Used, Guest Name** → filled with meaningful defaults
- Added a **Review Category** column using `pd.cut()` on Guest Rating bins
- Exported cleaned data to `hospitality_cleaned_dataset.csv`

---

## 📈 Phase 2 — Analysis & Visualization (`FinalProjectAnalysis.ipynb`)

Key analyses performed:

- **KPIs:** Total bookings, total revenue, average guest rating, average room rate
- **Revenue by Location** — bar chart
- **Booking Status Distribution** — pie chart
- **Monthly Revenue Trend** — line chart
- **Bookings by Room Type** — bar chart
- **Guest Rating Distribution** — histogram
- **Revenue Outlier Detection** — boxplot + IQR method
- Breakdowns by booking channel, service used, day of week, and guest country

New columns derived during analysis: `Month`, `Year`, `Weekday`

Final cleaned dataset exported to `hospitality_final_dataset.csv`

---

## 📊 Phase 3 — Power BI Dashboard (`hotel.pbix`)

An interactive Power BI dashboard built on the final cleaned dataset, enabling:

- Revenue and profit exploration by location, room type, and time period
- Guest satisfaction analysis by review category
- Booking channel and payment method breakdowns
- Filtering by status, guest type, and purpose of visit

---

## 📸 Dashboard Preview
![Dashboard]()

## 🛠️ Tech Stack

- **Python** (pandas, matplotlib, numpy)
- **Jupyter Notebook**
- **Microsoft Power BI**
- **Microsoft Excel**

---

## 🚀 Getting Started

1. Clone this repository
2. Open `FinalProject.ipynb` and run all cells to generate the cleaned dataset
3. Open `FinalProjectAnalysis.ipynb` to explore the analysis and charts
4. Open `hotel.pbix` in Power BI Desktop to interact with the dashboard

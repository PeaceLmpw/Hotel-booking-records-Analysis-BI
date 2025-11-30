# Hotel-booking-records-Analysis-BI

# 🏨 Wembo hotel - Business Intelligence Dashboard
A comprehensive data analysis project analyzing 9,000+ hotel bookings to improve occupancy rates and customer satisfaction.


## 🎯 Project Overview

This project analyzes **3+ years of hotel booking data** (2022-2025) for a fictional 4-star hotel with 150 rooms. The goal was to:
- Predict occupancy patterns
- Analyze guest satisfaction drivers
- Optimize revenue management
- Provide actionable business recommendations

**Role:** Data Analyst Consultant  
**Tools:** Power BI Desktop, DAX, Power Query
---

## 📊 Dataset

### Data Source
- **Synthetic dataset** generated for analysis (realistic patterns)
- **9,000 booking records** from January 2022 to November 2025

### Dataset Features (20 columns)

| Column | Type | Description |
|--------|------|-------------|
| `booking_id` | Text | Unique identifier |
| `booking_date` | Date | When reservation was made |
| `checkin_date` | Date | Guest arrival date |
| `checkout_date` | Date | Guest departure date |
| `nights_stayed` | Integer | Length of stay (1-14 nights) |
| `adults` | Integer | Number of adults (1-4) |
| `children` | Integer | Number of children (0-3) |
| `room_type` | Categorical | Standard, Deluxe, Suite, Executive |
| `booking_channel` | Categorical | Direct, OTA, Corporate, Travel_Agent |
| `country` | Text | Guest country (FR, US, UK, DE, etc.) |
| `price_per_night` | Decimal | Nightly rate ($80-$450) |
| `special_requests` | Integer | Number of special requests (0-5) |
| `is_canceled` | Binary | 0=Confirmed, 1=Canceled |
| `previous_stays` | Integer | Number of prior visits (0-10) |
| `satisfaction_score` | Decimal | Rating 1.0-5.0 |
| `lead_time_days` | Integer | Days between booking and arrival |
| `total_revenue` | Decimal | Price × nights_stayed |
| `booking_status` | Text | "Confirmed" or "Canceled" |
| `satisfaction_segment` | Text | Excellent, Very Good, Good, Average, Poor |
| `season` | Text | Summer, Winter, Spring, Autumn |

**Download Dataset:** [hotel_bookings_2022_2025.csv](#) *(9,000 rows × 20 columns)*

---

## ✨ Key Features

### Advanced Analytics
- ✅ **9 Custom DAX Measures** (Occupancy Rate, RevPAR, ADR, etc.)
- ✅ **Calendar Table** with time intelligence
- ✅ **Data Modeling** with proper relationships
- ✅ **Dynamic Filtering** with synchronized slicers
- ✅ **Conditional Formatting** for KPI visualization

### Interactive Visualizations
- 📊 **Line Charts** - Revenue trends over time
- 📈 **Bar/Column Charts** - Bookings by segment
- 🎯 **KPI Cards** - Real-time performance metrics
- 🔥 **Heatmaps** - Occupancy by month/year
- 🔵 **Scatter Plots** - Price vs Satisfaction correlation
- 🥧 **Donut Charts** - Distribution analysis
- 📋 **Tables/Matrix** - Detailed country/channel performance

---

## 📱 Dashboard Pages

### 1️⃣ Executive Overview
**Purpose:** High-level business performance at a glance
**Key Metrics:**
- Total Bookings: **9,000**
- Total Revenue: **$15.71M**
- Occupancy Rate: **54.20%**
- Satisfaction Score: **4.31/5.0**
**Visualizations:**
- Monthly Revenue Trend (2022-2025)
- Bookings by Room Type
- Revenue by Booking Channel
- Top 10 Countries

### 2️⃣ Detailed Analysis
**Purpose:** Deep dive into patterns and anomalies
**Key Insights:**
- Occupancy Heatmap (identifies low-performing months)
- Price vs Satisfaction Scatter Plot
- Cancellation Rate by Channel
- Booking Lead Time Distribution (Avg: **91 days**)
- Seasonal Satisfaction Patterns

### 3️⃣ Customer Insights
**Purpose:** Understanding guest behavior and loyalty
**Key Findings:**
- **27% returning customers** (loyalty opportunity)
- Loyalty impact on satisfaction (6+ stays = 4.4+ rating)
- Guest composition: **81% Adults Only** vs **19% Families**
- Special requests **negatively correlate** with satisfaction
- Revenue Matrix: Channel × Country performance


## 🔍 Key Insights

### 🚨 Critical Findings

1. **Occupancy Crisis**
   - Current: 54.20% | Target: 85% | **Gap: -30.8 percentage points**
   - Worst months: February (40%), January (46%), March (47%)
2. **Direct Channel Underperformance**
   - Only 22% of bookings despite 0% commission
   - Highest cancellation rate: 12.64%
   - Lost potential: ~$120K annually in OTA commissions
3. **Loyalty Effect**
   - Customers with 6+ stays: **4.4+ satisfaction**
   - First-time guests: **4.2 satisfaction**
   - Only **27% return rate** (industry avg: 40%)
4. **Seasonal Opportunities**
   - Summer dominates satisfaction across all room types
   - Autumn shows strong occupancy (October: 61%, November: 57%)
   - Winter needs strategic intervention
5. **Service Gap**
   - **Inverse correlation:** More special requests = Lower satisfaction
   - Indicates expectation management issues
---

## 🛠️ Technologies Used

### Core Tools
- **Power BI Desktop** - Data visualization and reporting
- **Power Query (M Language)** - Data transformation and cleaning
- **DAX (Data Analysis Expressions)** - Advanced calculations and measures
- **Excel** - Initial data inspection

### Key Techniques
- Data modeling and relationship management
- Time intelligence calculations
- Conditional formatting and dynamic visuals
- Cross-filtering and drill-through capabilities
- Custom tooltips for enhanced UX

---
## 🚀 How to Use

### Prerequisites
- Power BI Desktop (free download from Microsoft)
- Windows 10 or later (for Power BI Desktop)
### Installation Steps
1. **Clone this repository**
```bash
git clone https://github.com/yourusername/hotel-analytics-powerbi.git
cd hotel-analytics-powerbi
```
2. **Open the Power BI file**
- Double-click `booking_hotel_BI.pbix`
- Power BI Desktop will launch automatically
3. **Refresh the data** (optional)
- If you want to use your own data:
  - Click "Transform data" → "Data source settings"
  - Point to your CSV file
  - Apply changes
4. **Interact with the dashboard**
- Use slicers to filter by year, room type, season
- Hover over visuals for detailed tooltips
- Click on data points to cross-filter other visuals
- Navigate between pages using the buttons

---

## 📁 Project Structure

```
hotel-analytics-powerbi/
│
├── 📊 booking_hotel_BI.pbix                        # Main Power BI dashboard file
├── 📄 hotel_bookings_2022_2025.csv                 # Dataset (9,000 records)
├── 📝 hotel_bookings_records - Report.pdf         # Full analysis report (English)
├── 📝 hotel_bookings_records - Report v-fr.pdf    # Full analysis report (French)
├── 📸 screenshots/                                 # Dashboard screenshots
│   ├── executive_overview.png
│   ├── detailed_analysis.png
│   └── customer_insights.png
├── 📋 README.md                                    # This file
└── 📜 LICENSE                                     # MIT License

```

## 📈 Key Metrics & DAX Formulas

### Total Revenue
```dax
Total Revenue = 
SUMX(
    FILTER(hotel_bookings, hotel_bookings[is_canceled] = 0),
    hotel_bookings[total_revenue]
)
```

### Occupancy Rate
```dax
Occupancy Rate = 
VAR TotalRoomNights = [Total Room Nights]
VAR DaysInPeriod = COUNTROWS(Calendar)
VAR AvailableRooms = 150
VAR TotalAvailableRoomNights = DaysInPeriod * AvailableRooms
RETURN
DIVIDE(TotalRoomNights, TotalAvailableRoomNights, 0)
```

### Average Daily Rate (ADR)
```dax
ADR = 
CALCULATE(
    AVERAGE(hotel_bookings[price_per_night]),
    hotel_bookings[is_canceled] = 0
)
```

### RevPAR (Revenue Per Available Room)
```dax
RevPAR = DIVIDE([Total Revenue], [Total Room Nights], 0)
```

---

## 🎓 What I Learned

This project helped me develop skills in:
- ✅ Business requirements analysis
- ✅ Data cleaning and transformation (Power Query)
- ✅ Advanced DAX calculations
- ✅ Data modeling best practices
- ✅ Dashboard design and UX
- ✅ Business storytelling with data
- ✅ Strategic recommendation formulation

---

## 🔮 Future Enhancements

Potential improvements for this project:
- [ ] Integrate **Pythonfor predictive modeling (occupancy forecasting)
- [ ] Add **real-time data refresh** via Power BI Service
- [ ] Implement **anomaly detection** for revenue/occupancy
- [ ] Create **mobile-optimized layout**
- [ ] Add **natural language Q&A** feature
- [ ] Integrate with **SQL database** for live updates

---

## 📞 Contact & Feedback

**Peace Lwanzo**  
💼 - LinkedIn: https://www.linkedin.com/in/peace-lwanzo-b862b51a6/
   - Facebook: https://www.facebook.com/share/1A5rXdCxQx/
   - Instagram: https://www.instagram.com/peacelmpw?igsh=MWV0dTMzZXNjZ2oxcw==
📧 Email: peacelwanzo@gmail.com  
🐙 GitHub: https://github.com/PeaceLmpw
---

## 🙏 Acknowledgments

- Dataset generated using realistic hospitality industry patterns
- Inspired by real-world hotel revenue management challenges
- Power BI community for DAX formula optimization tips

---

**Last Updated:** December 01st, 2025  
**Version:** 1.0.0

---

*Made with ❤️ and Power BI*

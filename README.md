# ✈️ Airline Performance Dashboard — Power BI

> An interactive Power BI report providing end-to-end visibility into airline operations across Indian carriers — covering flight volumes, revenue, delays, and route performance.

---

## 📊 Dashboard Overview

The report is built on the `Airline_Data` dataset and spans **3 report pages**, each targeting a distinct analytical domain. A custom **Airline Dark Theme** is applied throughout for a polished, professional look.

| Page | Purpose |
|------|---------|
| 🏠 Executive Overview | High-level KPIs, revenue trends, and flight status summary |
| ⏱️ Delay Analysis | Deep-dive into delay drivers by airline, route, and time slot |
| 🗺️ Route & Location | Geographic route performance with bubble map visualisation |


Page 1- Executive Overview
<img width="1195" height="675" alt="Executive overview" src="https://github.com/user-attachments/assets/c8ab2e37-aa20-4e45-83d3-9c6d128cc121" />

Page 2- Detailed Insights
<img width="1202" height="677" alt="Detailed insights" src="https://github.com/user-attachments/assets/90291192-88ca-4f46-b7f4-3c93c2cb6600" />

Page 3- Analyze Route
<img width="1203" height="678" alt="Analyze route" src="https://github.com/user-attachments/assets/255e13c4-e814-48c2-9301-72bb53a54439" />

---

## 🔑 Key Performance Indicators (KPIs)

### Executive Overview
| KPI | Description |
|-----|-------------|
| **Total Flights** | Aggregate count of all flights in the dataset |
| **Total Revenue (INR)** | Sum of revenue generated across all airlines |
| **Average Delay (mins)** | Mean delay in minutes across all flights |
| **On-Time %** | Percentage of flights that departed/arrived on schedule |
| **Delay Status Split** | Donut chart showing On-Time vs Delayed flight proportions |
| **Revenue by Airline** | Column chart comparing revenue across IndiGo, Air India, Vistara, SpiceJet, Akasa Air |
| **Revenue Trend** | Monthly/yearly line chart by airline |

### Delay Analysis
| KPI | Description |
|-----|-------------|
| **Delayed Flights** | Total count of delayed flights |
| **Average Delay (mins)** | Mean delay per flight |
| **Total Delay (mins)** | Cumulative delay minutes across all flights |
| **Max Delay (mins)** | Worst-case single-flight delay recorded |
| **Delay by Airline** | Column chart of average delay per carrier |
| **Delay by Route** | Table: Source City → Total Delay, Avg Delay, Total Flights |
| **Delay by Time Slot** | Donut chart showing delay distribution across time slots (Morning / Afternoon / Evening / Night) |

### Route & Location
| KPI | Description |
|-----|-------------|
| **Total Routes** | Number of unique origin-destination route pairs |
| **Avg Delay per Route** | Mean delay aggregated at route level |
| **Max Delay** | Maximum delay observed on any single route |
| **Route Map** | Bubble map — bubble size = Total Flights, bubble colour = Avg Delay |
| **Top 8 Routes by Delay** | Horizontal bar chart of the most delayed destination cities |
| **Route Performance Table** | Destination City → Avg Delay, Total Flights, Revenue (INR) |

---

## 🏢 Airlines Covered

- **IndiGo**
- **Air India**
- **Vistara**
- **SpiceJet**
- **Akasa Air**

---

## 🗂️ Data Model

### Tables
| Table | Description |
|-------|-------------|
| `Airline_Data` | Core fact table containing flights, delays, revenue, status |
| `Airline_Routes` | Route-level dimension (Source City, Destination City) |

### Key Columns / Measures
| Field | Type | Description |
|-------|------|-------------|
| `Airline` | Dimension | Carrier name |
| `Source City` | Dimension | Origin city |
| `Destination City` | Dimension | Destination city |
| `Date` | Dimension | Flight date (with Year / Month hierarchy) |
| `Time Slot` | Dimension | Time-of-day bucket |
| `Status` | Dimension | On-Time / Delayed |
| `Revenue (INR)` | Measure | Ticket revenue in Indian Rupees |
| `Delay (Minutes)` | Measure | Raw delay value per flight |
| `Total Flights` | Measure | Count of flights |
| `Avg Delay` | Measure | Average delay (DAX calculated) |
| `Avg Delay per Route` | Measure | Average delay scoped to route |
| `Total Delay (mins)` | Measure | Sum of all delay minutes |
| `Max Delay` / `Max Delay (mins)` | Measure | Maximum delay |
| `Delayed Flights` | Measure | Count of flights with Status = Delayed |
| `On-Time %` | Measure | % of on-time flights |
| `Total Routes` | Measure | Count of distinct routes |
| `Total Revenue` | Measure | Sum of Revenue (INR) |

---

## 🎛️ Filters & Slicers

Each page includes interactive slicers to drill down by:
- **Airline Name**
- **Source City**
- **Time Slot**
- **Delay (Minutes)** range
- **Route** (on Delay Analysis page)

---

## 🧭 Report Navigation

The report uses **page navigation buttons** for seamless movement between the three pages:

```
[Overview] ←→ [Delay Analysis] ←→ [Route & Location]
```

---

## 🛠️ Technical Details

| Property | Value |
|----------|-------|
| File Format | `.pbix` (Power BI Desktop) |
| Theme | Airline Dark Theme (custom JSON) |
| Canvas Size | 1920 × 1080 px |
| Schema Version | Report 3.2.0 / Page 2.3.1 / Visual 2.7.0 |
| Tool | Microsoft Power BI Desktop |

---

## 🚀 Getting Started

1. **Clone or download** this repository.
2. Open `airline_data.pbix` in **Power BI Desktop** (April 2024 or later recommended).
3. If prompted, refresh the data source connection.
4. Use the navigation buttons to explore each dashboard page.
5. Apply slicers to filter by airline, route, or time slot.

---

## 📁 Repository Structure

```
📦 airline-dashboard
 ┣ 📊 airline_data.pbix       # Main Power BI report file
 ┣ 📄 README.md               # This file
```

---

## 🙌 Acknowledgements

Dashboard designed with a custom dark aviation theme. Background imagery and branding assets are included within the `.pbix` resource package.

---

*Built with ❤️ using Microsoft Power BI*

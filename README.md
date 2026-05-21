# Uber-booking-analysis
# 🚗 Uber Booking System — Power BI Dashboard

A comprehensive Power BI report analyzing ride booking data for an Uber-style cab booking system. The dashboard covers end-to-end operational metrics including ride volume, revenue, cancellations, vehicle performance, and customer/driver ratings.

---

## 📊 Dashboard Overview

The report is built on a single dataset — `ncr_ride_bookings` — and contains **6 interactive pages**, each focused on a specific area of the business.

| Page | Description |
|------|-------------|
| **Home** | Landing/navigation page with branding |
| **Overall** | High-level KPIs, ride volume trends, and booking status breakdown |
| **Vehicle Type** | Performance breakdown by vehicle category |
| **Revenue** | Revenue KPIs, vehicle-wise revenue, and payment method split |
| **Cancellation** | Cancellation rates, reasons, and driver vs. customer split |
| **Ratings** | Average customer and driver ratings with distribution charts |

---

## 📁 File

| File | Description |
|------|-------------|
| `Uber_booking_systemm.pbix` | Power BI Desktop report file |

---

## 📄 Pages in Detail

### 🏠 Home
- Branded landing page with the Uber logo
- Acts as a navigation hub to all report sections

---

### 📈 Overall
- **Total Bookings** KPI card
- **Ride Volume Over Time** — area chart by month showing booking trends
- **Booking Status** — pie chart showing the distribution of completed, cancelled, and other statuses
- **Date Slicer** — filter all visuals by date range

---

### 🚙 Vehicle Type
- Table showing per-vehicle-type breakdown of:
  - Total Bookings
  - Total Booking Value (Revenue)
  - Total Ride Distance

---

### 💰 Revenue
- **Total Revenue** and **Avg Revenue Per Ride** KPI cards
- **Revenue by Vehicle Type** — column chart
- **Revenue by Payment Method** — donut chart (e.g., cash, card, UPI)
- Additional revenue segment cards for drill-down

---

### ❌ Cancellation
- **Cancellation Rate %**, **Total Cancellations**, **Customer Cancellations**, **Driver Cancellations** — KPI cards
- **Customer vs. Driver Cancellation Split** — donut chart
- **Cancellation Reason Tables** — separate tables for customer-side and driver-side cancellation reasons

---

### ⭐ Ratings
- **Avg Customer Rating** and **Avg Driver Rating** KPI cards
- **Customer Rating Distribution** — line chart
- **Driver Rating Distribution** — clustered column chart
- Total driver ratings summary card

---

## 🗃️ Data Model

### Table: `ncr_ride_bookings`
The core fact table containing one row per booking. Key columns include:

| Column | Description |
|--------|-------------|
| `Booking ID` | Unique identifier for each ride |
| `Date` | Date of the booking |
| `Booking Status` | Status of the ride (e.g., Completed, Cancelled) |
| `Vehicle Type` | Category of vehicle booked |
| `Booking Value` | Fare/revenue for the ride |
| `Ride Distance` | Distance covered in the ride |
| `Payment Method` | How the ride was paid for |
| `Customer ID` | Identifier for the customer |
| `Customer Rating` | Rating given by the customer |
| `Driver Ratings` | Rating given to the driver |
| `Reason for cancelling by Customer` | Customer-provided cancellation reason |
| `Driver Cancellation Reason` | Driver-provided cancellation reason |

### Measures Table: `_Uber Measures`
Custom DAX measures used across visuals:

| Measure | Description |
|---------|-------------|
| `Total Bookings` | Count of all booking records |
| `Total Revenue` | Sum of all booking values |
| `Avg Revenue Per Ride` | Average fare per completed ride |
| `Cancellation Rate %` | Percentage of rides cancelled |
| `Total Cancellations` | Total cancelled rides |
| `Total Customer Cancellations` | Cancellations initiated by customers |
| `Total Driver Cancellations` | Cancellations initiated by drivers |
| `Avg Customer Rating` | Average rating given by customers |
| `Avg Driver Rating` | Average rating given to drivers |

---

## 🛠️ Requirements

- **Power BI Desktop** (latest version recommended)
- No external data connections or gateway required — data is embedded in the `.pbix` file

---

## 🚀 Getting Started

1. Download and install [Power BI Desktop](https://powerbi.microsoft.com/desktop/)
2. Open `Uber_booking_systemm.pbix` in Power BI Desktop
3. Use the **Home** page to navigate between report sections
4. Use the **Date slicer** on the Overall page to filter data by time period

---

## 📌 Notes

- The dataset appears to be focused on **NCR (National Capital Region)** ride bookings based on the table name `ncr_ride_bookings`
- All data is static and embedded within the `.pbix` file
- Page navigation is handled via built-in Power BI `pageNavigator` and `actionButton` visuals

---

## 📷 Preview

> Open the `.pbix` file in Power BI Desktop to view the full interactive dashboard with Uber branding and navigation.

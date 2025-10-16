# uber_rides_analysis
## Project Title
**Exploratory Data Analysis of Uber Rides Dataset**

**Objective:**
Understand ride patterns, pricing, vehicle usage, weather influence, and ride cancellations for Uber rides.

---

## Dataset Description

| Column Name       | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| ride_id           | Unique identifier for each ride                                             |
| date              | Date of the ride (YYYY-MM-DD)                                              |
| time              | Time of the ride (HH:MM)                                                   |
| city              | City where the ride occurred                                               |
| source            | Ride start location                                                        |
| destination       | Ride end location                                                          |
| vehicle_type      | Type of vehicle (SUV, Sedan, Mini, Auto)                                   |
| weather           | Weather during ride (Rainy, Clear, etc.)                                   |
| distance_km       | Distance of the ride in km                                                 |
| surge_multiplier  | Surge pricing multiplier                                                   |
| price             | Ride fare (INR)                                                            |
| payment_method    | Payment type (UPI, Cash, Card)                                            |
| driver_rating     | Rating given to the driver (1-5)                                          |
| ride_status       | Ride completion status (Completed, Cancelled)                              |

**Dataset Stats:**
- 2000 rides, 15 columns
- Minor missing values in `driver_rating`
- Outliers detected in numeric columns (`price`, `distance_km`)

---

## Data Preprocessing

1. Filled missing `vehicle_type` with "UNKNOWN".
2. Converted `date` and `time` columns to datetime for temporal analysis.
3. Removed outliers in `price` and `distance_km`.
4. Identified categorical columns: `city`, `vehicle_type`, `weather`, `payment_method`, `ride_status`.

---

## Exploratory Data Analysis (EDA)

### 1. Bar Plots (Single Category Analysis)
- Rides per city, vehicle type, weather, payment method, ride status.
- **Insights:**
  - Chennai has the most rides.
  - SUV is the most popular vehicle type.
  - UPI is the most used payment method.
  - Most rides are completed.

### 2. Box Plots (Numeric vs Category)
- **Price by vehicle type:** SUVs more expensive.
- **Distance by weather:** Longer rides in Rainy weather.
- **Driver ratings by payment method:** Small variation across payment types.

### 3. Combined Categorical Analysis
- **Route Heatmap:** Popular source → destination routes.
- **Ride Status by City & Vehicle Type (Stacked Bar):** Shows completed vs cancelled rides per category.

### 4. Temporal Trends
- **Rides per hour:** Peaks in morning (8–10 AM) and evening (6–9 PM).
- **Average price per vehicle type by hour:** Shows surge pricing during peak times.
- **Cancelled rides per weekday:** Higher on weekends.
- **Weekday vs Hour Heatmap:** Visualizes busy hours per day.

---

## Key Insights

1. **Ride Demand:** Highest in Chennai; peak hours in morning/evening.
2. **Vehicle Usage:** SUV most popular; price depends on vehicle type and surge.
3. **Cancellations:** Mostly completed rides; proportionally more on weekends.
4. **Pricing Trends:** Surge pricing increases during peak hours; longer and SUV rides cost more.

---

## Conclusion
- Analysis provides actionable insights for driver allocation, surge pricing, reducing cancellations, and identifying high-demand routes and times.
- Visualizations help understand ride patterns clearly.

---

## Usage Instructions
1. Place your plots/images in an `images/` folder.
2. Open this README.md in GitHub or VSCode to view with embedded images.
3. Can convert to PDF using Markdown-to-PDF tools if needed.

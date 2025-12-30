## About Dataset

### Uber Ride Analytics Dataset 2024

This comprehensive dataset contains detailed ride-sharing data from Uber operations for the year 2024, providing rich insights into booking patterns, vehicle performance, revenue streams, cancellation behaviors, and customer satisfaction metrics.

### Dataset Overview

The dataset captures 148,770 total bookings across multiple vehicle types and provides a complete view of ride-sharing operations including successful rides, cancellations, customer behaviors, and financial metrics.


### Data Schema

| Column                            | Description                                                                     |
| --------------------------------- | ------------------------------------------------------------------------------- |
| Date                              | Date of the booking                                                             |
| Time                              | Time of the booking                                                             |
| Booking ID                        | Unique identifier for each ride booking                                         |
| Booking Status                    | Status of booking (Completed, Cancelled by Customer, Cancelled by Driver, etc.) |
| Customer ID                       | Unique identifier for customers                                                 |
| Vehicle Type                      | Type of vehicle (Go Mini, Go Sedan, Auto, eBike/Bike, UberXL, Premier Sedan)    |
| Pickup Location                   | Starting location of the ride                                                   |
| Drop Location                     | Destination location of the ride                                                |
| Avg VTAT                          | Average time for driver to reach pickup location (in minutes)                   |
| Avg CTAT                          | Average trip duration from pickup to destination (in minutes)                   |
| Cancelled Rides by Customer       | Customer-initiated cancellation flag                                            |
| Reason for cancelling by Customer | Reason for customer cancellation                                                |
| Cancelled Rides by Driver         | Driver-initiated cancellation flag                                              |
| Driver Cancellation Reason        | Reason for driver cancellation                                                  |
| Incomplete Rides                  | Incomplete ride flag                                                            |
| Incomplete Rides Reason           | Reason for incomplete rides                                                     |
| Booking Value                     | Total fare amount for the ride                                                  |
| Ride Distance                     | Distance covered during the ride (in km)                                        |
| Driver Ratings                    | Rating given to driver (1–5 scale)                                              |
| Customer Rating                   | Rating given by customer (1–5 scale)                                            |
| Payment Method                    | Method used for payment (UPI, Cash, Credit Card, Uber Wallet, Debit Card)       |
 
---
## Uber Ride Analytics – Exploratory Data Analysis (EDA)

### 0. Data Preparation & Feature Engineering
To enable meaningful analysis, the following preprocessing steps were performed:

- Converted `Date` and `Time` columns into proper datetime formats
- Extracted **temporal features**:
  - Hour
  - Day
  - Month
- Verified data consistency across booking status, cancellations, and incomplete rides
- Focused analysis on key operational, financial, and behavioral variables

=> This transformation allowed raw transaction data to be analyzed as **behavioral and operational patterns**.

### 1. Ride Demand Analysis
- Aggregated ride bookings by **hour of day**
- Observed clear **peak and off-peak demand periods**
- Ride demand is not evenly distributed throughout the day

 => *This highlights the importance of time-based planning for ride allocation and pricing.*


### 2. Payment Method Analysis
- Analyzed distribution of payment methods across all rides
- Found that **digital payment methods** (UPI, cards, Uber Wallet) dominate transactions
- Cash payments account for a smaller share of total bookings

=> *This reflects strong customer adoption of cashless payment systems.*


### 3. Cancellation Analysis
- Separated **customer-initiated** and **driver-initiated** cancellations
- Examined cancellation reasons for each group:
  - Customer cancellations are largely driven by **behavioral factors** (e.g., change of plans, booking mistakes)
  - Driver cancellations are more often linked to **operational constraints** (e.g., vehicle or acceptance issues)

=> *Cancellation behavior differs significantly between customers and drivers.*


### 4. Importance of Cancellation Reasons
- Instead of analyzing only cancellation counts, this EDA focused on **reason codes**
- This enabled **root-cause analysis**, rather than surface-level metrics

=> *Understanding “why” cancellations happen is more valuable than simply measuring how often they occur.*

---

## Key Insights

- Ride demand exhibits strong **time-of-day patterns**, making temporal features critical for analysis.
- **Digital payments dominate**, indicating opportunities for fintech partnerships and digital reward programs.
- Customer and driver cancellations have **distinct root causes**, requiring separate mitigation strategies.
- Feature engineering on time variables significantly improves the depth of insights without complex modeling.
- Descriptive analytics and visualization alone can surface **actionable operational insights**.

## Business & Operational Takeaways
- Time-based demand patterns can inform:
  - Driver allocation
  - Peak-hour incentives
  - Dynamic pricing strategies
- Improving driver-side reliability and support may reduce driver-initiated cancellations
- Customer experience can be improved through clearer booking flows and real-time communication
- Payment behavior insights support further investment in digital payment ecosystems

---

## Tools & Skills Used
- **Python** (Pandas, NumPy, Matplotlib / Seaborn)
- **Exploratory Data Analysis (EDA)**
- **Feature Engineering**
- **Data Visualization**
- **Operational Analytics**


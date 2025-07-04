# Summer-Analytics-2025

# 🚗 Dynamic Pricing for Urban Parking Lots – Summer Analytics 2025

This project was completed as part of the **IIT Guwahati Summer Analytics 2025 Capstone Project**.

---

## 📌 Objective

Build two dynamic pricing models for 14 urban parking lots using real-time and historical data. The models account for:

- Occupancy rate
- Queue length
- Vehicle type
- Traffic conditions
- Special event days

---

## ⚙️ Tech Stack

- **Python** (Core logic)
- **Pandas** (Data processing)
- **Matplotlib** (Static plots)
- **Bokeh** (Real-time graph attempts)
- **Google Colab** (Execution platform using `clear_output()` for real-time simulation)

---

## 🧠 Models Used

### 1. **Linear Model**

\[
Price = Previous\_Price + α \times \left(\frac{Occupancy}{Capacity}\right)
\]

- Base Price: \$10  
- Price capped between \$5 and \$20

---

### 2. **Demand-Based Model**

\[
Demand = α \cdot \left(\frac{Occupancy}{Capacity}\right) + β \cdot Queue - γ \cdot Traffic + δ \cdot SpecialDay + ε \cdot VehicleTypeWeight
\]

\[
Price = BasePrice \times \left(1 + λ \cdot NormalizedDemand\right)
\]

- Normalized and clipped output  
- Uses realistic weights for each factor

---

## 🔁 Real-Time Simulation

- Used `IPython.display.clear_output()` in loop to simulate real-time pricing
- Plots update based on each time tick from the dataset

> Note: Due to Colab limitations, `push_notebook()` (from Bokeh) does not work. So we simulate real-time with `clear_output(wait=True)`.

---

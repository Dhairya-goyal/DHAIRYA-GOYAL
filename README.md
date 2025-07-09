# 🚗 Dynamic Pricing for Urban Parking Lots

**Capstone Project – Summer Analytics 2025**  
Hosted by Consulting & Analytics Club × Pathway

## 📌 Problem Statement

Urban parking spaces face inconsistent demand throughout the day, leading to either congestion or underutilization. This project builds a **real-time dynamic pricing engine** for 14 parking lots using simulated data, employing machine learning and economic principles.

---

## 🛠️ Tech Stack

| Layer            | Tools/Packages Used           |
|------------------|-------------------------------|
| Programming      | Python 3.x                    |
| Data Processing  | Pandas, NumPy                 |
| Real-Time Engine | Pathway                       |
| Visualization    | Bokeh                         |
| Notebook         | Google Colab                  |

---

## 🧠 Model Architecture Flow

1. **Data Ingestion (Simulated)**:
    - 73 days × 18 time points/day for 14 parking spaces.
    - Fields include location, occupancy, queue, traffic, vehicle type, special day, etc.

2. **Feature Engineering**:
    - Normalize occupancy and demand drivers.
    - Assign weights to features like queue length, traffic, special days, and vehicle type.

3. **Pricing Models**:
    - **Model 1**: Linear Price Update  
      `Price_t+1 = Price_t + α * (Occupancy / Capacity)`

    - **Model 2**: Demand-Based Pricing  
      ```
      Demand = α*(Occupancy/Capacity) + β*QueueLength - γ*Traffic + δ*SpecialDay + ε*VehicleType
      Price_t = BasePrice * (1 + λ * NormalizedDemand)
      ```

    - **Model 3** (optional): Competitive Location-Aware Pricing  
      - Incorporates competitor prices and suggests rerouting based on proximity.

4. **Real-Time Simulation**:
    - Streaming data via Pathway.
    - Pricing logic updated in real time and predictions emitted continuously.

5. **Visualization**:
    - Live Bokeh plots for:
        - Pricing trends
        - Competitor price comparisons
        - Occupancy dynamics

---

## 🗂️ Project Structure

```

├── FIRST.ipynb                # Colab Notebook (Main logic and models)
├── dataset.csv                # Raw simulated parking data
├── problem statement.pdf      # Official project brief
├── README.md                  # This file
└── architecture.png           # Architecture flow diagram (optional)
```

---

## 🧭 Architecture Diagram
![Image Jul 9, 2025, 10_46_51 PM](https://github.com/user-attachments/assets/f49563e2-79dc-4524-93fe-bceee3956005)
---

## 📈 Sample Visualizations

- Price curves by time & space
- Occupancy vs price
- Comparison with competitors (Model 3)

---


## 🚀 Run Instructions

1. Open `FIRST.ipynb` in [Google Colab](https://colab.research.google.com).
2. Ensure Pathway is installed (`!pip install pathway`).
3. Run all cells in order.
4. Interactive visualizations will render using Bokeh.

---

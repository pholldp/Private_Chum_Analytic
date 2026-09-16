# CHUM CHUM TEA Analytics Dashboard 🍵
> **Interactive Sales & Menu Intelligence Dashboard**

A client-side, responsive single-page web application designed for analyzing transaction exports from POS systems. Provides deep insights into revenue streams, menu engineering matrices (Kasavana-Smith model), tea base distributions, sparkling beverage performance, branch comparisons, peak hourly curves, customer ordering behavior, and topping upsell simulations.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=flat-square&logo=chart.js&logoColor=white)
![Status](https://img.shields.io/badge/Deploy-GitHub_Pages_Ready-success?style=flat-square)

---

## 🌟 Key Features

### 1. 📊 Executive Overview & Daily Trends
- **Key Performance Indicators**: Real-time aggregation of Total Net Revenue, Margin %, Orders (Bills), Average Order Value (AOV), Volume Sold, and Discount Rate.
- **Visual Analytics**: Interactive daily revenue timeline and category share distributions powered by Chart.js.

### 2. 🧩 Menu Engineering Matrix (Kasavana-Smith)
- **4-Quadrant Classification**: Categorizes products into **Stars**, **Plowhorses**, **Puzzles**, and **Dogs** based on popularity (volume) vs. profitability (margin/unit or average price).
- **Product Scatter Plot**: Interactive bubble chart mapping item volume against unit economics with customizable quadrant crosshairs.
- **Hourly Demand Heatmap**: Visualizes category demand intensity across operating hours with relative heat grading.

### 3. 🍃 Tea Base & Sparkling Analysis
- **Tea Base Type Breakdown (หมวดหมู่ชา)**: Revenue, quantity, and unit margin across tea bases (e.g., Green Tea, Black Tea, Oolong).
- **Sparkling Analysis**: Tracks performance of carbonated items, price premium comparisons, and attachment rates.

### 4. 🏬 Branch & Peak Hour Performance
- **Branch Performance Matrix**: Compares net revenue, AOV, order volume, and store classification across branches.
- **Hourly Demand Curves & Day-of-Week**: Toggle between total and daily average volume to identify operational rush hours and quiet periods.

### 5. 👥 Customer Behavior & Topping Upsell Simulator
- **Multi-Dimensional Behavior Matrix**: Explores sales by channel (Walk-in, Delivery, Online), order type, and payment methods.
- **Upsell Simulator**: Model revenue impact from increasing topping attachment rates across active transaction bills.

### 6. 🛠️ Data Source Manager & Active List
- Dynamic client-side filtering by branches, channels, categories, and tea base types with real-time recalculation.
- Zero server dependency: all CSV parsing and data aggregation happens securely inside the browser via PapaParse.

---

## 🚀 Quick Start

### Run Locally
No build tools or Node.js required! Simply clone and open `index.html` in any modern web browser:

```bash
git clone https://github.com/pholldp/Private_Chum_Analytic.git
cd Private_Chum_Analytic
open index.html # On macOS
# or start a lightweight python server:
# python3 -m http.server 8080
```

---

## 🌐 Deploy to GitHub Pages (1-Click)

1. Push this repository to GitHub: `https://github.com/pholldp/Private_Chum_Analytic`
2. In your GitHub repository:
   - Go to **Settings** $\rightarrow$ **Pages** (in the left sidebar).
   - Under **Build and deployment** $\rightarrow$ **Branch**, select `main` and folder `/ (root)`.
   - Click **Save**.
3. Your live application will be available at:
   ```
   https://pholldp.github.io/Private_Chum_Analytic/
   ```

---

## 📁 Repository Structure

```
Private_Chum_Analytic/
├── index.html       # Standalone single-page application (UI, Analytics, & Visualizations)
├── README.md        # Documentation and guide
└── .gitignore       # Git ignore rules
```

---

## 🛠️ Built With
- **Vanilla JavaScript (ES6+)** - Zero dependencies, fast and lightweight.
- **Tailwind CSS (CDN)** - Modern responsive layout and styling.
- **Chart.js** - Interactive visual charts.
- **PapaParse** - In-browser fast CSV parser.
- **FontAwesome** - Icon library.

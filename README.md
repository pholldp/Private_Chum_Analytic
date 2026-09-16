# Private Sale Projection 📊
> **Retail Profit & Pricing Projection Simulator**

An interactive, responsive single-page web application designed for retail brands, pop-up events, and private sales. Model product pricing, retailer shelf fees (GP share), and sales mix ratios to determine required sales volume and target net profit in real time.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=flat-square&logo=chart.js&logoColor=white)
![Status](https://img.shields.io/badge/Deploy-GitHub_Pages_Ready-success?style=flat-square)

---

## 🌟 Key Features

### 1. 💼 Unit Economics & Product Catalog
- **Add / Edit / Duplicate Products**: Easily configure product catalog with custom unit costs, retail selling prices, and retailer shelf fees / GP percentages.
- **Real-Time Margin Health**: Visual indicators classify profit margins (Healthy $>25\%$, Acceptable $0-25\%$, or Loss-Making $\le 0\%$).
- **Currency Flexibility**: Seamlessly toggle between **THB (฿)** and **USD ($)** with a customizable live exchange rate.

### 2. 🎛️ Dynamic Sales Mix & Two-Way Target Sync
- **Interactive Mix Sliders**: Adjust proportional sales weight across SKUs with automatic percentage normalization.
- **Bi-Directional Target Sync**:
  - Enter **Target Net Profit** $\rightarrow$ instantly calculates **Required Unit Volume**.
  - Enter **Target Volume** $\rightarrow$ instantly calculates **Projected Net Profit**.
- **Financial Summary**: Real-time aggregation of Estimated Gross Revenue, Retailer / Shelf Fees, and Cost of Goods Sold (COGS).
- **Interactive Visualizations (Chart.js)**: Toggle between detailed breakdown lists and interactive donut/bar charts displaying unit distributions and profit contributions.

### 3. 💾 Comprehensive Simulation Scenario Engine
- **Save Scenarios**: Snapshot your current catalog, mix weights, and targets under custom names (e.g., *"Q4 Pop-Up Optimistic"*, *"Conservative 50k"*).
- **Scenario Manager**: Browse, load, duplicate, rename, or delete saved simulations.
- **Draft Auto-Save**: Never lose progress—active changes are automatically preserved in browser `localStorage`.
- **JSON Export & Import**:
  - Export single scenarios or backup all scenarios to `.json` files.
  - Import `.json` files to restore or share scenarios across devices.
- **CSV Breakdown Export**: Export full SKU breakdown requirements directly to `.csv` for Excel or Google Sheets.

---

## 📐 Mathematical Model

### Unit Net Margin
$$\text{Fee Amount} = \text{Price} \times \left( \frac{\text{ShelfFee}\%}{100} \right)$$
$$\text{Net Margin} = \text{Price} - \text{Unit Cost} - \text{Fee Amount}$$
$$\text{Margin } \% = \left( \frac{\text{Net Margin}}{\text{Price}} \right) \times 100$$

### Weighted Average Net Margin ($\text{WAM}$)
$$\text{Normalized Weight}_i = \frac{\text{Weight}_i}{\sum_{j} \text{Weight}_j}$$
$$\text{WAM} = \sum_{i} \left( \text{Net Margin}_i \times \text{Normalized Weight}_i \right)$$

### Target Synchronization
$$\text{Required Total Units} = \left\lceil \frac{\text{Target Profit}}{\text{WAM}} \right\rceil$$
$$\text{Target Profit} = \text{Total Units} \times \text{WAM}$$
$$\text{Required Units}_i = \left\lceil \text{Required Total Units} \times \text{Normalized Weight}_i \right\rceil$$

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
├── index.html       # Standalone single-page application (UI, Simulator, & Storage)
├── README.md        # Documentation and guide
└── .gitignore       # Git ignore rules
```

---

## 🛠️ Built With
- **Vanilla JavaScript (ES6+)** - Zero dependencies, fast and lightweight.
- **Tailwind CSS (CDN)** - Modern responsive layout and styling.
- **Chart.js** - Interactive visual charts.
- **FontAwesome 6** - Vector iconography.
- **HTML5 LocalStorage API** - In-browser persistence.

# E-Commerce Sales Analytics Dashboard

An interactive Jupyter notebook dashboard for exploring e-commerce sales data — built with `pandas`, `Plotly`, and `ipywidgets`. Pick a region from a dropdown and instantly see revenue, quantity, payment method, rating, and order breakdowns update across six linked charts.

## 📊 Features

- **Interactive region filter** — a single dropdown drives every chart on the dashboard
- **Sunburst chart** — Region → Product Category → Payment Method revenue breakdown
- **Revenue by product category** — bar chart, per selected region
- **Quantity sold by category** — bar chart, per selected region
- **Revenue by payment method** — bar chart, per selected region
- **Average customer rating by category** — bar chart (0–5 scale), per selected region
- **Total orders by category** — bar chart, per selected region

All charts are rendered with Plotly and include hover tooltips with formatted currency (₹) and percentages.

## 🗂️ Repository Contents

| File | Description |
|---|---|
| `AI_and_Automation_.ipynb` | Main notebook containing the data pipeline and dashboard |
| `E-Commerce_Sales_Analytics.csv` | Source dataset (5,000 order records) |

## 📁 Dataset

The dataset (`E-Commerce_Sales_Analytics.csv`) contains order-level e-commerce transaction records with the following columns:

| Column | Description |
|---|---|
| `order_id` | Unique order identifier |
| `order_date` | Date the order was placed |
| `customer_id` | Unique customer identifier |
| `product_category` | Category of the purchased product |
| `region` | Region the order was shipped to |
| `quantity` | Number of units ordered |
| `unit_price` | Price per unit |
| `discount` | Discount applied (as a fraction) |
| `payment_method` | Payment method used (e.g., Wallet, Card) |
| `delivery_days` | Days taken for delivery |
| `customer_rating` | Customer rating (0–5) |
| `revenue` | Total revenue for the order |

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- Jupyter Notebook or JupyterLab

### Installation

```bash
git clone <your-repo-url>
cd <your-repo-folder>
pip install pandas numpy plotly ipywidgets jupyterlab
```

If using classic Jupyter Notebook, you may also need to enable the widgets extension:

```bash
jupyter nbextension enable --py widgetsnbextension
```

### Usage

1. Place `E-Commerce_Sales_Analytics.csv` in the same folder as the notebook (or update the file path in the notebook — it currently points to a local Windows path and should be changed to a relative path, e.g. `pd.read_csv("E-Commerce_Sales_Analytics.csv")`).
2. Launch Jupyter:
   ```bash
   jupyter lab
   ```
3. Open `AI_and_Automation_.ipynb` and run all cells.
4. Use the **⚡ Region** dropdown at the top of the dashboard to filter the charts.

## 🛠️ Built With

- [pandas](https://pandas.pydata.org/) – data loading and aggregation
- [Plotly](https://plotly.com/python/) – interactive charts
- [ipywidgets](https://ipywidgets.readthedocs.io/) – dashboard controls and layout

## 📝 Notes

- Non-numeric values in `revenue`, `quantity`, and `customer_rating` are coerced and rows with missing key fields are dropped during cleaning.
- Currency values are displayed in ₹ (INR); update the formatting in the notebook if your dataset uses a different currency.

## 📄 License

Add a license of your choice (e.g., MIT) here.

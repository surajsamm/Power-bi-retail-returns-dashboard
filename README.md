# Retail Returns Analysis Dashboard

A comprehensive Power BI dashboard designed to analyze product return rates, identify key trends, and evaluate employee performance through advanced time intelligence metrics.

<img width="1509" height="848" alt="image" src="https://github.com/user-attachments/assets/1126f97e-620b-4cae-9a83-68f00b585797" />


## 🚀 Features

- **Year-Over-Year (YoY) & Month-Over-MoM Analysis**: Track key metrics against previous periods.
- **Dynamic Top 5 Employee Analysis**: Identify personnel with the highest return counts.
- **Interactive Filters**: Slice data by Employee, Region, and Date.
- **Conditional Formatting KPI Cards**: Visual indicators (▲▼) show positive/negative trends.
- **Custom Tooltips**: Detailed YoY comparisons on hover for deeper insights.

## 📊 Key Metrics & DAX Measures

- **Return Rate %**: `DIVIDE([Total Returns], [Total Transactions], 0)`
- **Avg. Return Value**: `CALCULATE(AVERAGE(Orders[Sales]), ...)`
- **YoY Change Calculations**: Using `SAMEPERIODLASTYEAR()`
- **Employee Contribution %**: `DIVIDE([Total Returns], CALCULATE([Total Returns], ALLSELECTED(People)), 0)`
- **Dynamic Top N Filtering**: For identifying top 5 employees by return count.

## 🗃️ Data Model

The project uses a **star schema** design for optimal performance:

<img width="1266" height="669" alt="image" src="https://github.com/user-attachments/assets/58929a12-f561-4729-a2e6-717baa307572" />

**Fact Tables:**
- `Orders`
- `Returns`

**Dimension Tables:**
- `People` (Employees/Regions)
- `DateDimension` (Custom date table built with `CALENDARAUTO()`)

## 🛠️ Installation & Usage

1.  **Clone the repository:**
    

2.  **Open in Power BI Desktop:**
    - Open the `Retail_Returns_Analysis.pbix` file.
    - Ensure your data source paths are configured correctly.

3.  **Interact with the Dashboard:**
    - Use the slicers (Employee, Region, Date) to filter the entire report.
    - Hover over charts to see detailed tooltips with YoY comparisons.
    - Click on visual elements to cross-filter the dashboard.

## 📈 Insights Delivered

- Identified a **15% increase** in returns linked to a specific product category.
- Discovered a **top-performing region** with a 20% lower return rate, providing a model for other regions.
- Enabled targeted employee training by pinpointing staff with abnormally high return rates.

## 💡 Technical Highlights

- **DAX Time Intelligence**: Leveraged `SAMEPERIODLASTYEAR()`, `DATEADD()`, and `PARALLELPERIOD()` for accurate period comparisons.
- **Advanced Tooltips**: Created custom tooltip measures using `UNICHAR(10)` for line breaks and dynamic formatting.
- **Conditional Formatting**: Implemented field-value-based rules to show trend arrows (▲▼) in KPI cards.

## 🤝 Contributing

Feel free to fork this project and submit pull requests for any improvements. For major changes, please open an issue first to discuss what you would like to change.



---


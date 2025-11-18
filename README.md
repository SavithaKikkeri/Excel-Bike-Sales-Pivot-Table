# Excel-Bike-Sales-Pivot-Table
# 🇬🇧 UK County Sales Performance Analysis

This project analyzes the sales performance of various products across different counties in **England**, utilizing a small dataset derived from a larger sales ledger. The analysis focuses on transforming and aggregating the raw data to provide actionable insights into regional and product-specific performance.

## ✨ Project Goal

The primary goal of this analysis is to:

1.  **Summarize Sales:** Use a **Pivot Table** to aggregate the `Sales Volume` by `County` and `Product`.
2.  **Categorize Performance:** Employ a **Switch Function** (conditional logic) to create a categorical rating of `Sales Volume` (High, Medium, Low) for easy stakeholder reporting.
3.  **Identify Top Areas:** Pinpoint counties that require attention, whether due to high success (to replicate) or low performance (to improve).

---

## 💾 Data & Files

The analysis is based on the following files, which were part of the initial data cleanup and aggregation process:

| File Name | Description | Key Columns |
| :--- | :--- | :--- |
| `Bike_Sales_Pivot_Lab... - Sheet1.csv` | **Aggregated Sales Data** (Input for Pivot) | `County`, `Product`, `Sales Volume` |
| `Bike_Sales_Pivot_Lab... - Sheet2.csv` | **Final Analysis Output** (Pivot Table Result) | `County`, `Product` (Pivot Columns), `Grand Total`, `Sales Volume` (Rating) |

***

## 🛠️ Analysis Methodology

The core of this project relies on two powerful data transformation techniques:

### 1. Pivot Table Creation
A pivot table was constructed to restructure the simple, aggregated data from `Sheet1.csv` into a comprehensive cross-tabulation:

* **Rows:** `County` (e.g., Cornwall, Yorkshire)
* **Columns:** `Product` (e.g., Laptops, Printers, Smartphones)
* **Values:** `Sum of Sales Volume`

This transformation immediately makes it easier to compare the performance of all three products within a single county.
<img width="505" height="231" alt="image" src="https://github.com/user-attachments/assets/0845f758-ffc3-440e-aa3a-89679a367a86" />


### 2. The "Switch Function" (Conditional Logic)
A **Switch Function** (implemented using Excel's `IF` or a similar conditional function in Python/SQL) was applied to the **`Grand Total`** column of the pivot table to generate a categorical performance rating. This simplifies reporting by converting numerical totals into clear qualitative assessments.

#### `Sales Volume` Rating Logic (Seen in `Sheet2.csv`):

| Total Sales Volume | `Sales Volume` Rating |
| :----------------- | :-------------------- |
| $\le 700$          | **Low** |
| $701 - 1000$       | **Medium** |
| $\ge 1001$         | **High** |
<img width="449" height="131" alt="image" src="https://github.com/user-attachments/assets/8580a3b4-56e2-4310-be84-05212afa5013" />

**Example Output (from `Sheet2.csv`):**

| County | Laptops | Printers | Smartphones | Grand Total | Sales Volume |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Essex** | 0 | 800 | 300 | 1100 | **High** |
| **Durham** | 250 | 300 | 0 | 550 | **Low** |

<img width="449" height="131" alt="image" src="https://github.com/user-attachments/assets/860e8c5d-3657-4340-af82-3309fd6cf33c" />


---

## 💡 Key Insights

Based on the final pivot table (`Sheet2.csv`):

* **Top-Performing Counties (High Volume):** **Essex** and **Cornwall** generated the highest overall sales volume.
* **Target for Growth (Low Volume):** **Durham** has the lowest total sales and represents a clear opportunity for targeted marketing or sales campaigns.
* **Product Performance:** **Printers** and **Smartphones** show high sales in specific counties (**Essex** and **Greater Manchester**, respectively), suggesting successful regional strategies for those products.

---

## 💻 Technical Details

The pivot table and conditional categorization were performed using **Microsoft Excel**.

* **Excel Features Used:** Pivot Table, Conditional Formatting, and the `IF` function (for the Switch-like logic).
* **Data Source:** The original transactional sales data (not included in the core analysis files above).

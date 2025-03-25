
# **Online Retail Data Analysis and Dashboard Insights**

## **Project Overview**

This project analyzes online retail data and visualizes key metrics using **Power BI**. The goal is to gain actionable insights on sales performance, customer behavior, and revenue generation. The project was implemented in **Visual Studio Code (VS Code)**, using **Python** for data preparation and **Power BI** for interactive dashboards.

---

## **Data Source**

The dataset used in this project is the **Online Retail dataset** from the **UCI Machine Learning Repository**. It contains transactional data from a UK-based online retail store, including invoice information, product prices, and timestamps.

- **Source**: [UCI Machine Learning Repository - Online Retail Dataset](https://archive.ics.uci.edu/ml/datasets/online+retail)

---

## **Project Setup in VS Code**

### **Step 1: Installing VS Code and Python**

1. Download and install **Visual Studio Code** from [VS Code Official Site](https://code.visualstudio.com/).
2. Install **Python** from [Python's official site](https://www.python.org/downloads/).
3. Install the Python extension in VS Code (from the Extensions tab).

### **Step 2: Setting up a Virtual Environment**

1. **Create a Virtual Environment**:   Run the following command in the terminal (inside your project folder):

   ```bash
   python -m venv .virtual  
   ```

2. **Activate the Virtual Environment**:

   - On **Windows**:
     ```bash
     .\.virtual\Scriptsctivate  
     ```
   - On **Mac/Linux**:
     ```bash
     source .virtual/bin/activate  
     ```

   You will see the virtual environment name (e.g., `.virtual`) appear in the terminal prompt.

3. **Install Required Libraries**:   Install the necessary libraries by running:

   ```bash
   pip install pandas matplotlib  
   ```

   This will install libraries for data manipulation (`pandas`) and visualization (`matplotlib`).

---

## **Data Cleaning and Preprocessing (in Python)**

### **Steps Taken in Python**

1. **Loading the Data**:   The CSV file was loaded into a pandas DataFrame named `note`:

   ```python
   import pandas as pd  
   note = pd.read_csv("OnlineRetail.csv", encoding='ISO-8859-1')  
   ```

2. **Data Cleaning**:

   - Dropping rows with missing `CustomerID`:
     ```python
     note = note.dropna(subset=['CustomerID'])  
     ```
   - Creating new features such as `TotalRevenue`:
     ```python
     note['TotalRevenue'] = note['Quantity'] * note['UnitPrice']  
     ```
   - Converting `InvoiceDate` to datetime:
     ```python
     note['InvoiceDate'] = pd.to_datetime(note['InvoiceDate'], dayfirst=True)  
     ```

3. **Exporting Cleaned Data**:   The cleaned data was exported for use in Power BI:

   ```python
   note.to_csv("Cleaned_OnlineRetail.csv", index=False)  
   ```

---

## **Creating the Power BI Dashboard**

After cleaning the data, Power BI was used to create the following visualizations:

### **Power BI Dashboard Insights**

The Power BI dashboard (see file **OnlineRetailStore.pbix**) contains the following key metrics and charts:

### **Key Metrics and Insights**

1. **Revenue Overview**:
   - Total Revenue: **\$8.3M**
   - Number of Countries: **37**
   - Total Quantity Sold: **5M units**
   - Average Unit Price: **\$3.46**
   - Total Customers: **4372**
   **Recommendation**:   Leverage upselling and cross-selling strategies by bundling popular items or creating combo deals to increase average basket size and revenue.

---

### **Top Performing Products (StockCode)**

- **Insight**:  The top StockCodes (`22223`, `85099B`, `47566`) generate the highest revenue.

  **Recommendation**:
  - Increase promotions for these top-selling products and ensure consistent inventory levels to avoid stockouts.

---

### **Sales by Country**

- **Insight**:  Most revenue (81.54%) is from the **United Kingdom**, followed by the **Netherlands**, **Germany**, and **France**.

  **Recommendation**:
  - Expand marketing efforts in lower-performing countries by offering localized promotions and region-specific offers.

---

### **Customer Purchase Behavior**

- **Insight**:  Many customer transactions are linked to specific high-demand products (analyzed via `CustomerID` counts by StockCode). Revenue trends show steady upward growth over the years.

  **Recommendation**:
  - Launch loyalty programs to encourage repeat purchases and boost long-term customer value.

---

### **Seasonality and Quantity Trends**

- **Insight**:  Seasonal peaks and dips in sales quantities can be observed.

  **Recommendation**:
  - Prepare inventory and staffing for peak demand periods. Launch seasonal promotions to capitalize on increased activity.

---

## **How to Use This Project**

1. **Clone the Repository**:

   ```bash
   git clone <repository-url>  
   ```

2. **Set Up Virtual Environment**:   Follow the steps mentioned in the **Project Setup in VS Code** section.

3. **Run the Notebook**:   Load and run the Jupyter Notebook in VS Code to explore the data cleaning and analysis process.

4. **Explore the Power BI Dashboard**:   Open the `OnlineRetailStore.pbix` file in Power BI to view and interact with the visualizations.

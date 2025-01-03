# **Sales Revenue Dashboard**

This project demonstrates a **Sales Revenue Dashboard** built using **Power BI**, **SQL**, and **Excel** to visualize sales data and provide actionable insights. The dashboard focuses on key performance metrics, sales trends, and regional analysis to empower decision-making.

---

## **Objective**

The primary goal of this dashboard is to offer a comprehensive overview of:
- Revenue performance across regions, stores, and product categories.
- Sales representatives’ contributions to transactions and revenue.
- Temporal trends in revenue generation (quarterly and monthly).
- Comparative analysis between stores and product categories.

---

## **Dashboard Features**

### **1. Total Performance Metrics**
At the top, the dashboard displays high-level KPIs:
- **Total Revenue**: $127.41M
- **Average Revenue**: $39.04K per transaction.
- **Total Transactions**: 3,264 transactions.
- **Total Countries**: 3,264 (likely a count of unique records, clarification may be needed).

These KPIs provide an immediate understanding of overall sales performance.

---

### **2. Revenue Analysis by Region**
- **Regions Covered**: Asia, U.K., and U.S.A.
- **Key Insights**:
  - **Asia**: $16.62M (13.05% of total revenue).
  - **U.K.**: $32.14M (25.22% of total revenue).
  - **U.S.A.**: $78.65M (61.73% of total revenue).
  
This breakdown helps identify the most lucrative regions for the business.

---

### **3. Detailed Revenue by Country**
- Countries analyzed include:
  - **Asia**: Singapore, Hong Kong, and Taiwan.
  - **U.K.**: England and Wales.
  - **U.S.A.**: Ohio, Las Vegas, and New York.
- A line and bar combination chart showcases:
  - Total Revenue by country.
  - Average Revenue for each country.

---

### **4. Revenue Trends by Quarter**
- **Quarterly Revenue Breakdown**:
  - **Q1**: $48M
  - **Q4**: $32M
  - **Q3**: $30M
  - **Q2**: $17M

A bar chart visualizes seasonal trends, allowing the business to strategize for peak quarters.

---

### **5. Revenue Contribution by Products**
- **Product Categories**:
  - **Smartphones**: The highest revenue-generating category.
  - **Accessories**: Moderate contribution.
  - **Tablets**: Lower contribution.
  - **Laptops**: Comparatively minimal impact.
  
A stacked bar chart separates the contribution of each product across the top-performing stores.

---

### **6. Revenue by Store Rank**
- **Top 5 Stores**:
  - Store 1 dominates, followed by Store 2, Store 3, Store 4, and Store 5.
- A **Tree Map** highlights the proportion of revenue contributed by each store.

This visualization supports comparisons between store performances at a glance.

---

### **7. Performance by Sales Representatives**
- Detailed table includes:
  - **Sales Reps**: Names of top-performing representatives.
  - **Total Transactions**: 192 per representative.
  - **Total Revenue**:
    - **Top Representative**: Andrew T. with $2,09,20,686.
    - Others: Revenue contributions range from $21,63,330 to $1,37,43,773.

This enables management to recognize high-performing sales reps and allocate resources effectively.

---

### **8. Monthly Revenue Trends**
- A line chart tracks:
  - **Total Revenue** by month.
  - **Average Revenue** trends.
- Observes revenue consistency, peaks, and dips over the months.

---

## **Technical Implementation**

### **1. Data Preparation with SQL**
- SQL was used to:
  - **Clean and transform data**: Handle missing values, duplicates, and outliers.
  - **Aggregate metrics**: Summarize data by region, store, product category, and sales rep.
  - **Generate Key Metrics**:
    - Total Revenue.
    - Average Revenue per transaction.
    - Transaction counts.
  - **Join Tables**: Combine data from multiple sources like regions, products, and transactions.

**Sample SQL Queries**:
```sql
-- Example: Revenue by Region
SELECT 
    Region, 
    SUM(Revenue) AS Total_Revenue, 
    COUNT(TransactionID) AS Total_Transactions
FROM SalesData
GROUP BY Region;
```

---

### **2. Data Formatting with Excel**
- **Data Cleaning**:
  - Removed invalid records.
  - Standardized date and currency formats.
- **Pivot Tables**:
  - Used for quick exploratory analysis.
- **Exported Data**:
  - Cleaned datasets saved as CSV for Power BI import.

---

### **3. Data Visualization in Power BI**
- **Dataset Import**:
  - Data from SQL and Excel loaded into Power BI.
- **Relationships**:
  - Established relationships between tables (e.g., Sales Data ↔ Products ↔ Regions).
- **Visuals Used**:
  - Pie Chart: Revenue distribution by region.
  - Stacked Bar Chart: Revenue by products and store rank.
  - Tree Map: Store revenue contribution.
  - Line Chart: Monthly trends.
  - Table: Sales representatives’ performance.

**Interactivity**:
- Filters for:
  - Years (2019, 2020).
  - Store Rank (Select All, Store 1-5).

---

## **Steps to Recreate the Dashboard**

1. **Prepare Data**:
   - Use SQL to aggregate and clean raw data.
   - Export structured data to Excel for further cleaning and validation.
2. **Import Data into Power BI**:
   - Load Excel and SQL outputs into Power BI.
   - Create relationships between tables.
3. **Design Visualizations**:
   - Add charts, tables, and interactivity with slicers and filters.
4. **Optimize Performance**:
   - Optimize SQL queries for faster data processing.
   - Test Power BI filters for responsiveness.

---

## **Applications of the Dashboard**
- **Management**:
  - Monitor key sales performance metrics.
- **Strategic Planning**:
  - Focus marketing efforts on high-revenue regions.
- **Sales Operations**:
  - Incentivize top-performing sales reps.
- **Product Development**:
  - Invest in high-performing product categories.

---

## **Future Enhancements**
- **Drill-through Analysis**: Enable drill-downs to individual transactions.
- **Predictive Analytics**: Use historical data for forecasting sales trends.
- **Real-Time Integration**: Connect live data streams for real-time updates.

---

Feel free to reach out if you need further details or support in extending this project!

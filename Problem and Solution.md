**##Problem**

**The formula is trying to sum up the values from a column that it is currently trying to create.**



**Typically, "Sales per Quantity" implies a division (Sales / Quantity), not a sum. If you had a Sales / Quantity calculation at the row level before grouping, summing those individual ratios is mathematically different from and usually not as meaningful as calculating the ratio of the total sum of sales to the total sum of quantity.**



**For example, (Total Sales) / (Total Quantity) is not the same as Sum of (Individual Sale / Individual Quantity). The first is the correct way to get an average price across all transactions for a product.**





**##How to Correct the Calculation**

**To accurately calculate the sales per quantity for each product group, you should divide the sum of sales by the sum of the quantity.**



**You would need to modify the "Grouped Rows" step to perform two aggregations (a sum of sales and a sum of quantity) and then add a new custom column to divide them.**



1. **Add 'Total Sales': Click the Add aggregation button**
2. **Add 'Total Quantity': Click Add aggregation again.**
3. **Now you'll add a new column to perform the final division (Total Sales / Total Quantity).**

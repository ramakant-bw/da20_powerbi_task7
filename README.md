# da20_powerbi_task7
## Problem and Solution

The formula is trying to sum up the values from a column that it is currently trying to create.

Typically, **"Sales per Quantity"** implies a division (`Sales / Quantity`), not a sum.  
If you had a Sales / Quantity calculation at the row level before grouping, summing those individual ratios is **mathematically different** from and usually not as meaningful as calculating the ratio of the total sum of sales to the total sum of quantity.

For example:  

- ✅ **Correct:** `(Total Sales) / (Total Quantity)`  
- ❌ **Incorrect:** `Sum of (Individual Sale / Individual Quantity)`  

The first method gives the correct average price across all transactions for a product.

---

## How to Correct the Calculation

To accurately calculate the sales per quantity for each product group, you should divide the **sum of sales** by the **sum of the quantity**.

**Steps:**
1. Modify the **"Grouped Rows"** step to perform two aggregations:
   - Add **Total Sales** → Click *Add aggregation*  
   - Add **Total Quantity** → Click *Add aggregation* again  
2. Add a **new custom column** to perform the final calculation:  

   ```formula
   Total Sales / Total Quantity


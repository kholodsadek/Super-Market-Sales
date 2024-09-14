# Super-Market-Sales
## Description

This project analyzes the effectiveness of marketing promotions using key performance indicators (KPIs) such as *Promotion Effectiveness*. The dataset used includes transactional data from various branches, with information about product sales, customer types, and pricing. To ensure the quality and accuracy of the data, a series of data cleaning steps were performed, and additional columns were created to enhance the analysis.

### Data Cleaning

1. **NULL Values**:
   - **Tax 5%**: 9 rows with missing values were replaced with a calculated value:  
     `Tax = Total - (Price * Quantity)`.
   - **Total**: 3 rows with missing values were replaced with a calculated value:  
     `Total = (Price * Quantity) + Tax`.

2. **Currency Symbols**:
   - **UnitPrice**: 5 rows had 'USD' as a suffix, which was removed, and the column was converted to a float data type.

3. **Customer Type**:
   - 27 rows had non-standard entries, which were replaced with 'Normal'.

4. **Time Format**:
   - 1 row contained a time format in '8:30 PM'. All time formats were standardized to 'HH:MM AM/PM' (e.g., '01:27:00 PM').

5. **Data Types**:
   - **UnitPrice**: The column was initially of type object. It was converted to a float for accurate numerical analysis.

6. **Duplicate Rows**:
   - 6 duplicate rows were identified and removed from the dataset.

7. **Outliers**:
   - **Quantity**: 3 outliers with negative values [-8, -7, -1] were found. These values were replaced with their absolute values.
   - **Tax 5%**: 7 values were flagged as potential outliers but were found to be reasonable, so no changes were made.
   - **Total**: 9 high values were flagged but retained after verification as they were not true outliers.
   - **Rating**: 1 outlier (97) was corrected to 9.7 for accuracy.

### New Columns

- **branch_city**: A new column was created to indicate the city of each branch. This column ensures that branches are correctly identified by their corresponding city names.


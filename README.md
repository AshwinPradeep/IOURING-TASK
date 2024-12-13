# IOURING-TASK
# README for IOURING Simple Moving Average Task

## Project Title:  
**Simple Moving Average (SMA) Calculation for RELIANCE Historical Data**

## Organization:  
IOURING PRIVATE LIMITED  
Chennai - 600096  

---

## Problem Statement  
The task is to calculate the Simple Moving Average (SMA) for 1 year of historical stock data for RELIANCE. The dataset includes the following columns:  
- Open Price  
- High Price  
- Low Price  
- Close Price  
- Adjusted Close Price  
- Volume  

### Requirements:  
1. **Calculate SMA**: For each of the above fields, compute the 10-day SMA.  
2. **Update the Sheet**: Add new columns to the sheet for the computed SMA values under respective headings (`Open SMA(10)`, `High SMA(10)`, etc.).  
3. **Programming Language**: The program can be implemented in any language of choice.  
4. **Output**: The updated Excel sheet with computed SMA values must be saved and committed to the GitHub repository along with the source code.  

**Reference for SMA**: [Investopedia SMA](https://www.investopedia.com/terms/s/sma.asp)  

---

## Files in the Repository  
1. **`iouring_task_new.py`**: The Python script containing the SMA calculation program.  
2. **`RELIANCE_new.csv`**: The input CSV file with historical data.  
3. **`RELIANCE_updated.csv`**: The output CSV file with added SMA columns.  

---

## Execution Instructions  

### Pre-requisites:  
- Python 3.x installed.  
- Libraries required: `pandas`. Install it using:  
  ```bash
  pip install pandas
  ```  

### Steps to Run the Program:  
1. Clone the repository to your local machine:  
   ```bash
   git clone <repository_url>
   ```  
2. Navigate to the project directory:  
   ```bash
   cd iouring-task
   ```  
3. Place the input file `RELIANCE_new.csv` in the same directory as the script.  
4. Run the program using:  
   ```bash
   python iouring_task_new.py
   ```  
5. After successful execution, the updated file `RELIANCE_updated.csv` will be generated in the same directory.  

---

## Explanation of the Code  

### Objective:  
The program calculates a 10-day Simple Moving Average (SMA) for the specified columns in the dataset and appends these calculations to the original dataset.

### Steps Performed:  

1. **Importing Required Libraries**:  
   The script imports `pandas`, a powerful library for data manipulation and analysis.  

2. **Defining the SMA Calculation Function**:  
   - A reusable function `calculate_sma` is defined to compute the SMA for a given column.  
   - The rolling window function from `pandas` is used with a window size of 10.  
   - `min_periods=1` ensures calculations start even if fewer than 10 rows are available.  

3. **Loading the Data**:  
   - The program reads the input CSV file (`RELIANCE_new.csv`) using `pandas`.  
   - The dataset is loaded into a DataFrame, which allows easy manipulation.  

4. **Iterating Over Columns for SMA**:  
   - The script iterates through a list of columns (`Open`, `High`, `Low`, `Close`, `Adj Close`, `Volume`).  
   - For each column, the `calculate_sma` function is called.  
   - The SMA values are added as new columns to the DataFrame with names such as `SMA(Open) 10D`, `SMA(High) 10D`, etc.  

5. **Saving the Output**:  
   - The updated DataFrame is saved as a new CSV file (`RELIANCE_updated.csv`).  
   - This file contains the original data along with the computed SMA values.  

6. **Completion Message**:  
   - A success message is printed, indicating that the SMA calculation is complete and the output file is saved.

---

## Evaluation Criteria  
1. **Correctness of Output**: The SMA values are correctly computed and stored in the file.  
2. **Modular Code**: The use of a function for SMA calculation ensures reusability and clarity.  
3. **Error Handling**: The code gracefully handles missing or incomplete data using `min_periods=1`.  
4. **Efficiency**: The use of `pandas` for computation ensures that the program is efficient in handling large datasets.  

---

## References  
- [Simple Moving Average on Investopedia](https://www.investopedia.com/terms/s/sma.asp)  
- `pandas` Documentation: [Rolling Window](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.rolling.html)  

---

For any queries, contact: **support@iouring.com**


# Sales Data Cleaning

This project cleans a messy 200-row sales CSV with Pandas and NumPy. The workflow is contained in `clean.ipynb`.

## Dataset

The notebook reads `messy_sales - Sheet1.csv` and processes these columns:

- `Date`
- `Region`
- `Product`
- `Category`
- `UnitsSold`
- `UnitPrice`
- `TotalSales`
- `ProfitMargin(%)`

## Cleaning Performed

- Normalizes column names.
- Converts dates to datetime values.
- Trims and standardizes region, product, and category text.
- Corrects common category misspellings.
- Converts text units such as `thirty` and `twenty` to numbers.
- Removes currency symbols and converts unit prices to numeric values.
- Converts profit margins to percentages.
- Recalculates `TotalSales` as `UnitPrice * UnitsSold`.
- Exports the cleaned dataset.

## Requirements

- Python 3
- Pandas
- NumPy
- Jupyter Notebook or JupyterLab

Install the Python packages with:

```bash
pip install pandas numpy jupyter
```

## Usage

1. Update the input path in the first notebook cell if the CSV is stored somewhere else.
2. Open and run `clean.ipynb` from top to bottom.
3. The cleaned data is written to `path`.

For a portable setup, replace the absolute file paths with paths relative to this project folder.

## Output

The cleaned DataFrame has 200 rows and 8 columns. Invalid or missing values in `UnitsSold` are retained as missing values, so `TotalSales` is also missing where units could not be determined. The notebook reports that there are 4 missing `UnitsSold` values.

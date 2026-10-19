# Hotel Booking Cancellation Analysis

This project explores hotel booking data to understand booking cancellations and prepare a cleaned dataset for further analysis and future cancellation prediction.

## Project files

- `Ogabek_Hotel_Lab.ipynb` — Jupyter notebook containing the data loading, inspection, cleaning, feature engineering, analysis, and visualizations.
- `Ogabek_Hotel_Documentation.txt` — written documentation of the decisions and findings.
- `hotel_bookings.csv` — source dataset required to run the notebook.
- `hotels_clean.csv` — cleaned dataset exported by the notebook.

## Requirements

- Python 3
- Jupyter Notebook support
- pandas
- NumPy
- Matplotlib
- Seaborn

Install the Python packages with:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

## Run the notebook

1. Place `hotel_bookings.csv` in the project folder, alongside the notebook.
2. Open `Ogabek_Hotel_Lab.ipynb` in VS Code or Jupyter.
3. Select a Python environment with the required packages installed.
4. Run the notebook cells in order.

The notebook expects the CSV to contain 119,390 rows and 32 columns.

## Workflow

The notebook:

1. Loads the CSV with pandas and preserves an original in-memory copy.
2. Inspects the dataset dimensions, data types, missing values, duplicates, and unusual values.
3. Identifies `is_canceled` as the target and examines columns that could cause target leakage.
4. Cleans selected missing values, duplicate rows, impossible bookings, and suspicious ADR values; standardizes meal labels and data types; and combines arrival-date fields.
5. Creates four features: `total_nights`, `total_guests`, `total_price`, and `is_family`.
6. Compares cancellation rates and booking characteristics across hotel types and other booking groups.
7. Creates five visualizations, including a lead-time histogram, hotel cancellation count plot, monthly ADR line chart, market-segment cancellation bar plot, and numeric-feature correlation heatmap.
8. Exports the cleaned data to `hotels_clean.csv`.

The notebook reports 86,970 rows and no remaining missing values after cleaning. It performs exploratory analysis and feature engineering; it does not train or evaluate a machine-learning model.

## Notes

- Cleaning decisions are documented in `Ogabek_Hotel_Documentation.txt`.
- `reservation_status` and `reservation_status_date` are removed from the cleaned data because they describe outcomes that are not available when a booking is made.
- The notebook's results depend on the supplied source CSV and the executed notebook cells.

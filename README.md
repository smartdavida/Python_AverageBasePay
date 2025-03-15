**People Analytics: Average Base Pay Analysis**

This project answers the question: "What is the average base pay for US employees?" using a dataset of employee compensation details. The code filters the dataset to include only US employees, cleans the base pay values, and calculates the average salary. This analysis is valuable for People Analytics, helping organizations assess compensation trends and make data-driven decisions.


**Features**
- Filters employee data to include only US employees.
- Cleans and converts base pay values for accurate calculations.
- Computes the average base pay for US employees.
- Useful for compensation analysis in People Analytics.


**Installation**

To use this project, follow these steps:
1. Open Google Colab (or any Python environment).
2. Upload the dataset (CSV file with employee data).
3. Run the Python script to filter, clean, and calculate the average base pay.


**Usage**

**Step 1: Upload Dataset**

from google.colab import files
uploaded = files.upload()
df = pd.read_csv("your_filename.csv")

**Step 2: Convert Base Pay to Numeric**

df["Base Pay"] = df["Base Pay"].replace('[\$,]', '', regex=True).astype(float)

**Step 3: Filter US Employees**

df_us = df[df["Country Name"] == "US"]

**Step 4: Calculate Average Base Pay**

average_base_pay_us = df_us["Base Pay"].mean()
print(f"Average Base Pay for US Employees: ${average_base_pay_us:,.2f}")


**Contributing**

Contributions are welcome! If you have suggestions for improving the analysis, feel free to fork the repository and submit a pull request.


**License**

This project is open-source under the MIT License.


**Contact**

For any questions, reach out via GitHub or LinkedIn! 🚀

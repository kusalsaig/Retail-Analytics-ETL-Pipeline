# 🛒 Retail Analytics ETL Pipeline

This project builds a simple **ETL (Extract, Transform, Load) pipeline** using the **Online Retail Dataset** from Kaggle. It demonstrates how to preprocess, clean, and analyze retail transaction data using Python in Google Colab.

---

## 📁 Dataset

- **Name:** OnlineRetail.csv  
- **Source:** [UCI Machine Learning Repository / Kaggle](https://archive.ics.uci.edu/ml/datasets/Online+Retail)
- **Description:** This dataset contains over 500,000 transactions from a UK-based online retailer from 2010 to 2011.

---

## 🔄 Project Workflow

### 1️⃣ Extract
- Load data from `OnlineRetail.csv`
- Handle encoding issues using `ISO-8859-1`

### 2️⃣ Transform
- Remove rows with:
  - Missing `CustomerID`
  - Missing `Description`
  - Negative `Quantity`
  - Zero or negative `UnitPrice`
- Convert `InvoiceDate` to datetime
- Add new column: `TotalPrice = Quantity × UnitPrice`

### 3️⃣ Load
- Export cleaned data to `OnlineRetail_Cleaned.csv`
- Preview top-performing countries based on revenue

---

## 🧪 Sample Output

```bash
Raw data shape: (541909, 8)
Cleaned data shape: (397924, 9)

Top 5 Countries by Revenue:
United Kingdom    8,187,929.64
Netherlands         284,661.65
EIRE                263,276.72
Germany             221,698.35
France              197,403.75
🧰 Tools & Technologies
Python (Pandas)

Google Colab

Jupyter Notebook

CSV Handling

🚀 How to Run (in Google Colab)
Open Google Colab

Upload OnlineRetail.csv using:

python
Copy
Edit
from google.colab import files
uploaded = files.upload()
Run each cell of the ETL code provided.

Download the cleaned dataset using:

python
Copy
Edit
files.download('OnlineRetail_Cleaned.csv')
📦 Output Files
✅ OnlineRetail_Cleaned.csv — Cleaned and transformed retail data.

📊 Optional Add-ons
You can enhance this project by adding:

Revenue over time visualizations

Top-selling products charts

Customer segmentation or RFM analysis

🙋‍♂️ Author
G. Kusal Sai
Final Year B.Tech Project | Data Analytics | Deep Learning

📄 License
This project is open-source under the MIT License.

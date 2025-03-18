# Hackathon-Assignment-Detecting-and-Extracting-Tables-from-PDFs



# PDF Table Extractor

## 📌 Introduction

PDF Table Extractor is a Python-based tool designed to extract tables from PDF files and convert them into structured Excel spreadsheets. Unlike other solutions, this tool operates independently of Tabula or Camelot, making it versatile for handling various table formats, including structured, unstructured, and borderless tables.

## 🚀 Key Features

- Extracts tables from PDFs using `pdfplumber` and `PyPDF2`
- Handles complex and irregular table layouts with custom extraction techniques
- Detects and corrects page orientations (e.g., rotated pages) before extraction
- Cleans and formats extracted table data for better usability
- Exports extracted tables directly to Excel (`.xlsx` format)
- Provides a user-friendly interface via Streamlit for seamless interaction

## 🛠 Installation

Ensure you have the required dependencies installed before running the tool:

```bash
pip install pdfplumber PyPDF2 pandas openpyxl streamlit base64
```

## 💻 How to Use

### 1️⃣ Running in Jupyter Notebook

For running the extraction script within a Jupyter Notebook (without the Streamlit UI), use the following approach:

```python
from pdf_extractor import extract_tables_from_pdf  # Ensure pdf_extractor.py exists in your directory

pdf_path = "sample.pdf"  # Update with your file path
output_path = "output.xlsx"

dfs, success = extract_tables_from_pdf(pdf_path, output_path)

if success:
    print("Tables extracted and saved to", output_path)
else:
    print("No tables found.")
```

### 2️⃣ Running as a Streamlit Web Application

To launch the interactive web interface with Streamlit, execute:

```bash
streamlit run pdf_extractor.py
```

Once the app is running:

- Open the provided link in your browser
- Upload a PDF file
- Extract tables and download them in Excel format

## 📂 Project Structure

```
📂 PDF-Table-Extractor
│── pdf_extractor.py       # Core script for table extraction
│── README.md              # Documentation
│── requirements.txt       # Dependencies list
│── 📂 pdfs                # Directory to store input PDFs
│── 📂 output              # Directory to save extracted Excel files
```

## 🔥 Example Output

Extracted tables are saved as Excel files in the `output/` folder, with each sheet representing a different table from the processed PDF.

### Sample Extracted Tables:

![Example Output 1](path/to/image1.png)

![Example Output 2](path/to/image2.png)

## 🤝 Contributions

Contributions and enhancements are always welcome! Feel free to fork this repository and improve the table extraction logic.


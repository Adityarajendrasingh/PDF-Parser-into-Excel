# PDF-Parser-into-Excel

This Python project extracts structured data from bank statement PDFs and saves it to an Excel file. It supports different statement formats using pattern detection and custom parsing functions.

## 🧠 Features

- Extracts text lines from bank statements.
- Automatically detects the layout pattern.
- Parses transactions based on the detected pattern.
- Saves extracted data into a `.xlsx` Excel file.
- Easily extendable to support new PDF formats.

## 📁 Project Structure

```
.
├── main.py                 # Main script
├── test.pdf                # Sample PDF file
├── test_parsed.xlsx        # Sample PDF file
└── README.md               # Project documentation
```

## ⚙️ How It Works

1. The PDF is read using `extract_text_lines(pdf_path)`.
2. `detect_pattern(lines)` figures out which format the bank statement follows.
3. If the pattern is recognized (e.g., `PatternA`), the corresponding parsing function like `parse_pattern_a(lines)` is called.
4. The parsed data is converted into a Pandas DataFrame and saved as an Excel file.

## 🚀 Getting Started

### Requirements

- Python 3.7+
- Install required packages:
  ```bash
  pip install pandas openpyxl pdfplumber
  ```

# Extract Data from PDF file and convert to CSV

This project extracts unstructured data from PDF files containing well information and converts it into a CSV format for easier analysis and processing.

## Project Overview

The script performs the following key steps:

1. Extracts images from input PDF files
2. Preprocesses the extracted images to improve OCR accuracy
3. Uses OCR (Optical Character Recognition) to extract text from the images
4. Parses the extracted text to identify relevant data fields
5. Organizes the extracted data into a structured format
6. Outputs the structured data to a CSV file

## Key Features

- PDF image extraction using PyMuPDF
- Image preprocessing with OpenCV
- OCR using Tesseract via pytesseract
- Regular expression parsing to identify data fields
- Structured data output to CSV using pandas

## Requirements

- Python 3.x
- Libraries: pymupdf, pytesseract, pandas, cv2, os, re

## Usage

1. Ensure all required libraries are installed
2. Place the input PDF file in the same directory as the script
3. Update the input filename in the script if necessary
4. Run the script
5. The output will be saved as "temp.csv" in the same directory

## Data Fields Extracted

- Case Number
- Date Received by OCD
- Pooling Approval Date
- State
- County
- Landing Zone
- Operator
- Pooling Code
- Well Family
- Well Name
- API Number
- TVD (True Vertical Depth)
- Surface Hole Latitude and Longitude
- Bottom Hole Latitude and Longitude
- AFE (Authorization for Expenditure) Total

  ## Sample Output

| Case # | State | County | Landing Zone | Operator | Pooling Code | Well Family | Well Name | API # | TVD | Surface Hole Lat | Surface Hole Long | Bottom Hole Lat | Bottom Hole Long | AFE Total |
|--------|-------|--------|--------------|----------|--------------|-------------|-----------|-------|-----|------------------|-------------------|-----------------|------------------|-----------|
| 24337 | New Mexico | Lea | Bone Spring | Mewbourne Oil Company | 97903 | Red Hills West Bone Spring wells | Red Hills West 22/15 Fed. Com. Well No. 521H | 30-025-51120 | 10521 | 32.0215572 | 103.6666865 | 32.0500022 | 103.6698576 | 8,784,000 |
| 24337 | New Mexico | Lea | Bone Spring | Mewbourne Oil Company | 97903 | Red Hills West Bone Spring wells | Red Hills West 22/15 Fed. Com. Well No. 571H | 30-025-Pending | 11013 | 32.0215574 | 103.6666221 | 32.0500071 | 103.6666221 | 9,678,900 |
| 24337 | New Mexico | Lea | Bone Spring | Mewbourne Oil Company | 97903 | Red Hills West Bone Spring wells | Red Hills West 22/15 Fed. Com. Well No. 502H | 30-025-Pending | 10251 | 32.0215575 | 103.6664931 | 32.0500122 | 103.6641782 | 9,678,900 |
| 24337 | New Mexico | Lea | Bone Spring | Mewbourne Oil Company | 97903 | Red Hills West Bone Spring wells | Red Hills West 22/15 Fed. Com. Well No. 524H | 30-025-50993 | 10555 | 32.0215577 | 103.6664285 | 32.0215577 | 103.6664285 | 9,678,900 |
| 24337 | New Mexico | Lea | Bone Spring | Mewbourne Oil Company | 97903 | Red Hills West Bone Spring wells | Red Hills West 22/15 Fed. Com. Well No. 574H | 30-025-51121 | 11018 | 32.0215574 | 103.6665575 | 32.0500073 | 103.6669534 | |
| 24337 | New Mexico | Lea | Bone Spring | Mewbourne Oil Company | 97903 | Red Hills West Bone Spring wells | Red Hills West 22/15 Fed. Com. Well No. 573H | 30-025-Pending | 11018 | 32.0215572 | 103.6667511 | 32.0500020 | 103.6699867 | |

## Notes

- The script is designed for a specific PDF format. Adjustments may be needed for different input formats.
- OCR accuracy depends on the quality of the input PDF and may require fine-tuning for optimal results.

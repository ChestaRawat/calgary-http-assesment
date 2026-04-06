# 📊 Web Server Log Analysis Project

## 📌 Overview
This project focuses on analyzing real-world web server log data using Python. The dataset used is the Calgary HTTP dataset, which contains nearly one year of web server logs.

The goal of this project is to:
- Process raw, unstructured log data
- Clean and transform it into structured format
- Perform analysis to extract meaningful insights

---

## 🏗️ Approach

The project follows a structured data pipeline:

### 1. Data Acquisition
- Downloaded dataset programmatically using HTTP requests
- Stored data locally in compressed (`.gz`) format

### 2. Data Loading
- Used `gzip` to read compressed log files
- Loaded raw log lines into memory for processing

### 3. Log Parsing
- Applied **Regular Expressions (Regex)** to extract structured fields:
  - IP Address (Host)
  - Timestamp
  - HTTP Method (GET, POST, etc.)
  - Requested Resource
  - Protocol
  - Status Code
  - Bytes Transferred

### 4. Data Cleaning
- Converted timestamps into `datetime` format
- Converted numeric fields (status codes, bytes) into proper types
- Handled missing or malformed data
- Removed invalid records

### 5. Data Analysis
Performed exploratory data analysis to derive insights such as:
- Total number of requests
- Distribution of HTTP status codes
- Most frequently accessed resources
- Traffic patterns over time

---

## 🧠 Key Assumptions

- Log entries follow a consistent structure (Apache-style logs)
- Missing or malformed entries are minimal and can be safely ignored
- Timestamp format is uniform across records
- Status codes and byte values are valid when present

---

## 🛠️ Tools & Technologies Used

- **Python**
- **Pandas** – Data manipulation and analysis
- **Requests** – Downloading dataset
- **Gzip** – Handling compressed files
- **Regex (re module)** – Parsing unstructured log data
- **Datetime** – Time-based transformations

---

## 📈 Key Insights

- Identified high-traffic periods on the server
- Determined most frequently accessed endpoints
- Analyzed error patterns (e.g., 404, 500 responses)
- Observed user access trends over time

---

## ⚠️ Challenges Faced

### 1. Handling Unstructured Data
- Raw logs were not in a tabular format
- Required careful regex design to extract fields accurately

### 2. Regex Complexity
- Writing and debugging regex patterns was time-consuming
- Needed to ensure patterns handled edge cases

### 3. Data Cleaning
- Dealing with missing or inconsistent values
- Ensuring correct datatype conversions

### 4. Performance Considerations
- Processing large log files required efficient memory handling

---

## 🚀 Learnings

- Improved understanding of **real-world data processing**
- Hands-on experience with **regex for data extraction**
- Strengthened **data cleaning and preprocessing skills**
- Learned how to build an **end-to-end data pipeline**

---

## 📂 Project Structure

```
ChestaAnalysis.ipynb   # Main notebook
ChestaAnalysis.html    # Exported HTML version
README.md              # Project documentation
```

---

## 🏁 Conclusion

This project demonstrates how raw log data can be transformed into actionable insights using Python. It highlights key skills in data processing, cleaning, and analysis, which are essential for real-world data engineering and analytics tasks.

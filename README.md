# 📊 Entity Duplication Detection in a CMS

## 📌 Overview
This project focuses on detecting and removing duplicate customer records from a Customer Management System (CMS) dataset. Poor data quality due to duplication can lead to inaccurate insights, increased costs, and operational inefficiencies.

The goal of this project is to build a **robust deduplication pipeline** using a combination of exact, fuzzy, and probabilistic matching techniques.

---

## 🚀 Key Results
- 📉 **1904 duplicate records removed**
- 📊 Dataset reduced from **5186 → 3282 unique customers**
- 🔍 Identified:
  - **31% exact duplicates**
  - **5.7% inconsistent records (typos, missing values, etc.)**
- 🧹 Produced:
  - Cleaned dataset
  - Separate dataset of potential duplicates with confidence scores (0–100)

---

## 🧠 Methodology

### 1. Data Cleaning & Preprocessing
- Standardised text (lowercase, removed whitespace, handled accents)
- Normalised phone numbers to a consistent format (`07XXXXXXXXX`)
- Preserved null values to avoid bias and GDPR risks

---

### 2. Deduplication Techniques

#### ✅ Exact Matching
- Email address matching
- Address-based matching (house number, street, postcode, etc.)
- Name + phone number combinations
- Name + date of birth combinations

---

#### 🔍 Fuzzy Matching
- Detected near-duplicates caused by:
  - Typos (e.g., "Jhon" vs "John")
  - Slight variations in email addresses
- Applied similarity thresholds (>90%)

---

#### 📈 Probabilistic Record Linkage
- Compared records using statistical similarity scoring
- Identified duplicates missed by other methods
- Tuned threshold to reduce false positives

---

## ⚠️ Challenges
- **Phone numbers are not unique identifiers** (multiple people can share them)
- Avoiding **data loss** while merging duplicate records
- Handling **incomplete data** without introducing bias
- Ensuring **GDPR compliance**

---

## 💡 Key Insights
- No single column can reliably identify a unique customer
- Combining multiple attributes significantly improves accuracy
- Data quality issues often compound (duplicates + inconsistencies)

---

## 🛠️ Tech Stack
- Python
- Pandas
- Record linkage / fuzzy matching libraries

---

## 📂 Project Structure

---

## 📈 Future Improvements
- Real-time duplicate detection during data entry
- Machine learning-based entity resolution
- Scalable pipeline for larger datasets
- Integration into production CMS systems

---

## 📚 References
- Fellegi-Sunter Model (Record Linkage)
- Data deduplication best practices
- GDPR data handling guidelines

---

## 👤 Author
**Andrew Scott**

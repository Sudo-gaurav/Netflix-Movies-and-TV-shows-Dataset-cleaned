# 📺Netflix-Movies-and-TV-shows-Dataset-Cleaning Project


Welcome! This project showcases how I manually cleaned and formatted the **Netflix Movies and TV Shows** dataset using **Microsoft Excel**. It’s perfect for anyone learning data cleaning, data profiling, or preparing datasets for dashboards or analysis.

---

## 📂 Dataset Sources

- 🔗 **Original Dataset:** [Netflix Movies and TV Shows – Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows)
- 📊 **Cleaned Dataset:** `netflix_cleaned.xlsx` *(uploaded in this repo)*

---

## 🧼 Cleaning Tasks Performed

The following data cleaning tasks were done manually in Excel:

1. **Removed Duplicates**
   - Used `Remove Duplicates` on entire rows to eliminate repeated entries.

2. **Trimmed Whitespace**
   - Applied `=TRIM()` and `=CLEAN()` to remove extra spaces and non-printable characters.

3. **Standardized Date Format**
   - Split `date_added` using “Text to Columns” → Month, Day, Year
   - Reconstructed proper date using:
     ```
     =DATE(Year, Month, Day)
     ```
   - Formatted the new date column as **DD/MM/YYYY (DMY)**

4. **Handled Missing Values**
   - Replaced blanks in `director`, `cast`, `country`, `rating`, and `date_added` with:
     ```
     =IF(A2="", "Unknown", A2)
     ```

5. **Split Multi-Value Columns (Optional)**
   - Separated values in `listed_in` (genres) using:
     ```
     =TEXTSPLIT(A2, ", ")
     ```
     *(Only if Excel 365 or handled manually using filters)*

6. **Formatted Text Columns**
   - Standardized text casing with:
     ```
     =PROPER(A2) or =UPPER(A2)
     ```

7. **Validated Column Data Types**
   - Ensured correct format for each:
     - `release_year` = Number
     - `date_added` = Date
     - `duration` = Text (standardized minutes/seasons)

---

## 🧾 Final Columns (After Cleaning)

| Column        | Description                              |
|---------------|------------------------------------------|
| show_id       | Unique Netflix ID                        |
| type          | Movie or TV Show                         |
| title         | Title of the content                     |
| director      | Director’s name (or “Unknown”)           |
| cast          | Lead actors (or “Unknown”)               |
| country       | Country of origin (or “Unknown”)         |
| date_added    | When it was added to Netflix (DMY)       |
| release_year  | Year of release                          |
| rating        | Age rating (e.g., TV-MA, PG)             |
| duration      | Duration (minutes or seasons)            |
| listed_in     | Genre tags                               |
| description   | Short summary                            |

---

## ⚙️ Tools Used

- 📊 **Microsoft Excel**
- 🧮 Excel formulas (`TRIM`, `IF`, `DATE`, `PROPER`)
- 🧠 Manual validation and inspection
- 🧷 GitHub for version control & publishing

---

## 📁 Files Included

| File | Description |
|------|-------------|
| `netflix_cleaned.xlsx` | Final cleaned Excel dataset |
| *(Optional)* `original_sample.csv` | Original sample dataset from Kaggle (if uploaded) |
| `formulas_used.txt` | List of Excel functions/formulas used for cleaning |
| *(Optional)* `screenshots/` | Screenshots of before/after cleaning steps |

---

## 📌 How to Use This Dataset

- Perfect for **exploratory data analysis**, **dashboard creation**, or **data profiling**
- Use in:
  - Excel
  - Python (Pandas)
  - Power BI / Tableau
  - SQL databases

---

## 🙌 Credits

- 📊 Original dataset by [Shivamb](https://www.kaggle.com/shivamb) on Kaggle
- ✍️ Cleaned and published by [Gaurav Tawri](Sudo-gaurav)

---

## ⭐ Like This Project?

Feel free to ⭐ star this repo or fork it for your own use. Contributions and feedback are welcome!


# 🧠 Knowledge Library Curation Dashboard

This Streamlit-based dashboard is designed to help users curate, analyze, and manage large-scale textual knowledge libraries (e.g., question-answer datasets, product documentation, FAQs). It offers powerful filtering, clustering, flagging, merging, and analytical capabilities through a modern and interactive UI.

---

## 🚀 Features

### 📁 File Management
- Upload `.csv` files to the platform.
- View and manage previously uploaded datasets.
- Automatically track file metadata (e.g., upload time, number of entries).

### 🧭 Dashboard Sections

#### 1. **Overview**
- View key health metrics:
  - Total entries
  - Outdated entries
  - Unique products and categories
  - Duplicate statistics
- Interactive bar and pie charts:
  - Entry distribution per product and category
  - Entry creation timeline

#### 2. **Clusters**
- Used **__sentence-transformers__** for embedding and **__HDBSCAN__** for clustering.
- Select entries within a cluster to:
  - **Merge**: Combine two or more entries into a new one.
  - **Flag**: Mark entries for review.
  - **Archive**: Mark entries as archived with timestamp.
- Merging UI includes:
  - Preview of selected entries
  - Input fields for new merged entry
  - Suggestions or custom inputs

#### 3. **Outdated Entries**
- Based on the metadata provided such as deleted_at.
- Useful for pruning stale content.

#### 4. **Compare**
- Compare two entries side by side for similarity or differences.

#### 5. **Duplicates**
- Detect and review duplicate entries based on count thresholds.

#### 6. **Product Analysis**
- Analyze entries by product over time and across categories.

#### 7. **Merged Entries** ✅ *(New)*
- Log of all merged entries.
- Shows:
  - Timestamp
  - Auto-generated ID
  - Source CQIDs
  - Merged question and answer

#### 8. **All Entries**
- Allows to navigate thorugh all the entries in the dataset.
- Implement filtering and sorting based on CQID, category, name and so on.

---


## 🔍 Filtering Options (Sidebar)
- **Search**: Keyword search on questions.
- **Category & Product**: Filter by metadata.
- **Date Range**: Filter by creation date.
- **Duplicate Range**: Filter by duplicate count.


## 📦 Requirements

- Python 3.8+
- Dependencies:
  ```
  pip install -r requirements.txt
  ```
  Includes:
  - streamlit
  - pandas
  - plotly
  - numpy
  - pyarrow
  - streamlit
  - scikit-learn
  - hdbscan
  - joblib
  - sentence-transformers
  - matplotlib

---

## 🚀 Running the App

```bash
streamlit run app/new_ui.py
```

---



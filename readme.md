<div align="center">

# 🎌 Anime Feature Extraction & EDA

### Cleaning messy scraped anime data and uncovering insights using Pandas, NumPy & String Regex 

<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
<img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas"/>
<img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy"/>
<img src="https://img.shields.io/badge/Regex-Re-FF6F61?style=for-the-badge&logo=regex&logoColor=white" alt="Regex"/>
<img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter"/>
<img src="https://img.shields.io/badge/Data%20Extraction-4CAF50?style=for-the-badge&logo=databricks&logoColor=white" alt="Data Extraction"/>

</div>

## 📌 About The Project

This project takes a **raw, messy anime dataset** (`anime.csv`) where a single `Title` column contains multiple pieces of information jumbled together — the anime's name, episode count, airing timespan, and member count all mixed into one string — and turn it into a clean, analysis-ready dataset.

The project is split into **two stages**:

| Stage | Focus | File |
|---|---|---|
| 🧹 **Stage 1** | Feature Extraction | `extraction_file.py` |
| 📊 **Stage 2** | Exploratory Data Analysis (EDA) | `Questions_1-10.ipynb` |

Using **Pandas**, **NumPy**, and **Regex**, the raw `Title` column is first parsed and cleaned into structured columns, and the resulting dataset is then explored through 10 guided EDA questions.

---

## 🧠 What The Raw Data Looked Like

A single value in the `Title` column of `anime.csv` looked something like this:

```
Fullmetal Alchemist: BrotherhoodTV (64 eps)Apr 2009 - Jul 20103,218,472 members
```

All the useful information — episodes, timespan, and member count — was buried inside this one messy string.

---

## 🧹 Stage 1: Feature Extraction

**Goal:** Parse the raw `Title` string and pull out structured columns.

- 🎬 **Episodes** — total number of episodes
- 📅 **Timespan** — airing start and end date
- 👥 **Members** — number of members who added the anime to their list

### ⚙️ Steps Followed

1. **Imported libraries** — `re`, `numpy`, and `pandas`.
2. **Loaded the raw dataset** — read `anime.csv` into a DataFrame called `data`.
3. **Extracted Episodes** — pulled the number of episodes from inside the parenthesis in the `Title` column, removed the word `" eps"`, and converted the result into an `int` type, storing it in a new `Episodes` column.
4. **Extracted Timespan** — parsed the text right after the closing parenthesis in the `Title` column to get the airing start–end date range, stored in a new `Timespan` column.
5. **Extracted Members** — used **Regex** to capture the numeric member count from the remaining part of the string, cleaned the commas, and converted it into an `int`, stored in a new `Members` column.
6. **Saved the cleaned dataset** — exported the final DataFrame (original columns + 3 new extracted columns) into a new file: `updated_anime_dataset.csv`.

---

## 📊 Stage 2: Exploratory Data Analysis — `Questions_1-10.ipynb`

**Goal:** Answer 10 real-world analytical questions on the cleaned dataset using Pandas & NumPy.

| # | Question | Technique Used |
|---|---|---|
| 1 | Top 5 highest rated anime | `nlargest()` |
| 2 | Top 5 most popular anime (by members) | `sort_values()` |
| 3 | Anime with the lowest member count | Boolean filtering |
| 4 | Score statistics (mean, median, std, min, max) | `numpy` functions & `describe()` |
| 5 | High-score & high-popularity anime (Score ≥ 9.00 & Members > 1M) | Multi-condition filtering |
| 6 | Count of long-running anime (Episodes > 100) | Boolean filtering + `count()` |
| 7 | List of long-running anime | Boolean filtering |
| 8 | Short-series high performers (Episodes ≤ 13 & Score ≥ 9.00) | Multi-condition filtering |
| 9 | Custom episode-count grouping | `pd.cut()` with bins & labels |
| 10 | Average score by episode group | `groupby()` |

### 🔑 Key Concepts Practiced

- Filtering and boolean indexing with multiple conditions
- Sorting and ranking (`nlargest`, `sort_values`)
- Descriptive statistics with **NumPy** and Pandas `.describe()`
- Custom binning with `pd.cut()` to group continuous data into categories
- Aggregation with `groupby()`

---

## 📂 Project Structure

```
Anime Feature Extraction/
├── anime.csv                    # Raw, original dataset
├── extraction_file.py           # Python script for feature extraction
├── updated_anime_dataset.csv    # Cleaned dataset with extracted features
├── Questions_1-10.ipynb         # EDA notebook — 10 Pandas/NumPy questions
└── README.md                    # Project documentation
```

---


## 👤 Author

<div align="center">

**Malik Waleed Hussain**

**BS Computer Science Student**

<a href="https://github.com/waleed4we">
<img src="https://img.shields.io/badge/GitHub-waleed4we-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/>
</a>

</div>

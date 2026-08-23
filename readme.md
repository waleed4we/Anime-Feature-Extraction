<div align="center">

# 🎌 Anime Feature Extraction

### Extracting hidden features from messy scraped anime data using Pandas, NumPy & Regex

<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
<img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas"/>
<img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy"/>
<img src="https://img.shields.io/badge/Regex-Re-FF6F61?style=for-the-badge&logo=regex&logoColor=white" alt="Regex"/>
<img src="https://img.shields.io/badge/Data%20Extraction-4CAF50?style=for-the-badge&logo=databricks&logoColor=white" alt="Data Extraction"/>

</div>

---

## 📌 About The Project

This project takes a **raw, messy anime dataset** (`anime.csv`) where a single `Title` column contains multiple pieces of information jumbled together — the anime's name, episode count, airing timespan, and member count all mixed into one string.

Using **Pandas**, **NumPy**, and **Regex**, the raw `Title` column is parsed and cleaned to extract three brand-new, structured columns:

- 🎬 **Episodes** — total number of episodes
- 📅 **Timespan** — airing start and end date
- 👥 **Members** — number of members who added the anime to their list

The cleaned result is then saved into a new file: **`updated_anime_dataset.csv`**.

> ⚠️ Note: This is the **first stage** of the project — pure feature extraction. Exploratory Data Analysis (EDA), visualizations, and deeper Pandas/NumPy queries will be added in the upcoming stages.

---

## 🧠 What The Raw Data Looked Like

A single value in the `Title` column of `anime.csv` looked something like this:

```
Fullmetal Alchemist: BrotherhoodTV (64 eps)Apr 2009 - Jul 20103,218,472 members
```

All the useful information — episodes, timespan, and member count — was buried inside this one messy string.

---

## ⚙️ Steps Followed

1. **Imported libraries** — `re`, `numpy`, and `pandas`.
2. **Loaded the raw dataset** — read `anime.csv` into a DataFrame called `data`.
3. **Extracted Episodes** — pulled the number of episodes from inside the parenthesis in the `Title` column, removed the word `" eps"`, and converted the result into an `int` type, storing it in a new `Episodes` column.
4. **Extracted Timespan** — parsed the text right after the closing parenthesis in the `Title` column to get the airing start–end date range, stored in a new `Timespan` column.
5. **Extracted Members** — used **Regex** to capture the numeric member count from the remaining part of the string, cleaned the commas, and converted it into an `int`, stored in a new `Members` column.
6. **Saved the cleaned dataset** — exported the final DataFrame (original columns + 3 new extracted columns) into a new file: `updated_anime_dataset.csv`.

---

## 📂 Project Structure

```
Anime Feature Extraction/
├── anime.csv                    # Raw, original dataset
├── extraction_file.py           # Python script for feature extraction
├── updated_anime_dataset.csv    # Final dataset with extracted features
└── README.md                    # Project documentation
```

---

## 🚀 Upcoming Work

- 📊 Exploratory Data Analysis (EDA)
- 🐼 More Pandas & NumPy queries
- 📈 Visualizations and insights

---

## 👤 Author

<div align="center">

**Malik Waleed Hussain**

<a href="https://github.com/waleed4we">
<img src="https://img.shields.io/badge/GitHub-waleed4we-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/>
</a>

</div>
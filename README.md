# 🌍 Global Terrorism Analysis Project

An Exploratory Data Analysis (EDA) project on the **United Nations Global Terrorism Analysis (UNGTA)** dataset, covering over **181,000 terrorist incidents worldwide from 1970 to 2017**.

> Submitted by: **Aman Juyal** | B.Tech CSE (IV Sem), Roll No: 2472132  
> Under the Guidance of: **Mr. Kamal Rawal**  
> Institution: **Doon University**

---

## 📌 Project Overview

This project uses data science techniques to uncover meaningful patterns in global terrorism data — spanning temporal trends, geographical hotspots, attack characteristics, and human impact. It also includes statistical hypothesis testing and machine learning classification models.

**GitHub Repository:** https://github.com/aman88-dev/Global-Terrorism-Analysis.git

---

## 🎯 Objectives

1. Analyze terrorism trends from 1970 to 2017
2. Identify the most affected countries and regions
3. Understand attack types and weapons used
4. Study casualties and their impact
5. Generate actionable insights for stakeholders
6. Build and compare ML models to predict attack success

---

## 📂 Dataset

**Source:** United Nations Global Terrorism Analysis (UNGTA) Dataset  
**File:** `Global Terrorism Data (2).csv`

| Property | Value |
|---|---|
| Total Records | 181,691 rows |
| Total Features | 135 columns |
| Time Range | 1970 – 2017 |
| Encoding | latin1 |

### Key Columns Used

| Column | Description |
|---|---|
| `iyear` / `imonth` / `iday` | Date of the incident |
| `country_txt` | Country where the incident occurred |
| `region_txt` | Region of the incident |
| `city` | City of the incident |
| `attacktype1_txt` | Primary attack method |
| `targtype1_txt` | Primary target category |
| `weaptype1_txt` | Weapon type used |
| `gname` | Name of the perpetrating group |
| `nkill` | Number of fatalities |
| `nwound` | Number of wounded |
| `success` | Whether the attack was successful (target variable) |
| `suicide` | Whether it was a suicide attack |

---

## 🛠️ Tech Stack

- **Python 3**
- **pandas** — data manipulation
- **NumPy** — numerical operations
- **Matplotlib** — visualizations
- **Seaborn** — statistical plots
- **SciPy** — hypothesis testing
- **scikit-learn** — machine learning models

---

## 🔧 Setup & Usage

### 1. Clone the Repository

```bash
git clone https://github.com/aman88-dev/Global-Terrorism-Analysis.git
cd Global-Terrorism-Analysis
```

### 2. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn
```

### 3. Add the Dataset

Place `Global Terrorism Data (2).csv` in the project root directory.

### 4. Run the Notebook

Open and run `globalterrorism.ipynb` in **Jupyter Notebook** or **Google Colab**.

> ⚠️ The notebook is designed to be fully executable in one go without errors.

---

## 📊 Exploratory Data Analysis

The analysis follows the **UBM Rule** of visualization:

- **U** — Univariate Analysis
- **B** — Bivariate Analysis (Numerical–Categorical, Numerical–Numerical, Categorical–Categorical)
- **M** — Multivariate Analysis

### Visualizations Included

| # | Chart | Key Insight |
|---|---|---|
| 1 | Attacks by Year (bar) | Attacks surged dramatically after 2000, peaking in 2014 |
| 2 | Trend Over Time (line) | Sharp escalation post-2004; slight decline after 2014 |
| 3 | Top 10 Affected Countries (bar) | Iraq is the most affected; South Asia and MENA dominate |
| 4 | Attack Types (bar) | Bombing/Explosion is by far the most common method |
| 5 | Weapon Types (bar) | Explosives and firearms are most frequently used |
| 6 | Region-wise Attacks (bar) | Middle East & North Africa has the highest attack count |
| 7 | Top Terrorist Organizations (bar) | Taliban, ISIS, and Boko Haram are the most active groups |
| 8 | Year-wise Casualties (line) | Casualties accelerated rapidly after 2010 |
| 9 | Top 10 Affected Cities (bar) | Baghdad, Kabul, and Mosul top the list |
| 10 | Missing Values Heatmap | Highlights data quality issues in the raw dataset |
| 11 | Killed vs Wounded per Year (grouped bar) | Wounded consistently outnumber killed; both peaked in 2014–2015 |
| 12 | Killed vs Wounded Scatter | Most incidents cluster near zero; a few catastrophic outliers exist |
| 13 | Most Targeted Groups (bar) | Private Citizens, Military, and Police are primary targets |
| 14 | Attack Type Distribution (pie) | Bombing/Explosion accounts for the largest share |
| 15 | Most Dangerous Groups by Kills (bar) | Taliban and ISIL are responsible for the most deaths |
| 16 | Region-wise Casualties (bar) | MENA and South Asia suffer the most casualties |
| 17 | Casualties Distribution (histogram) | Highly right-skewed; most incidents cause few casualties |
| 18 | Monthly Attack Pattern (line) | Attacks are fairly distributed across months |
| 19 | Weapons in Top Countries (bar) | Iraq, Pakistan & India rely heavily on explosives |
| 20 | Casualties Boxplot | Reveals significant outliers in high-impact events |
| 21 | Top 5 Countries Per Decade | Dominant hotspots shift across decades |
| 22 | Correlation Heatmap | Strong correlation between wounded and total casualties |

---

## 🔬 Hypothesis Testing

| # | Hypothesis | Test Used | Result |
|---|---|---|---|
| H1 | Suicide attacks cause more deaths than non-suicide attacks | Welch's t-test | ✅ Rejected H₀ — Suicide attacks are significantly more lethal |
| H2 | Attack type is independent of region | Chi-Square Test | ✅ Rejected H₀ — Region and attack type are significantly associated |
| H3 | No correlation between killed and wounded | Pearson Correlation | ✅ Rejected H₀ — Significant positive correlation exists |

---

## 🤖 Machine Learning Models

All models predict **attack success** (binary classification: success = 1 or 0).

### Features Used
`attacktype1_txt`, `targtype1_txt`, `weaptype1_txt`, `region_txt`, `nkill`, `nwound`

### Models Compared

| Model | Notes |
|---|---|
| Logistic Regression | Baseline probabilistic classifier |
| Decision Tree | Interpretable tree-based classifier |
| Random Forest | Ensemble of trees; highest accuracy |
| Naive Bayes | Probabilistic; assumes feature independence |
| K-Nearest Neighbors (KNN) | Instance-based; k=5 |
| Support Vector Machine (SVM) | Linear kernel (LinearSVC) |

A final bar chart compares all model accuracies side-by-side.

> **Best Performer:** Random Forest — demonstrated the highest accuracy and robustness across all models.

---

## 📈 Key Findings

- Global terrorism peaked in **2014**, with 2014–2015 recording the highest casualty counts
- **Iraq** is the single most affected country; the **Middle East & North Africa** is the most affected region
- **Bombing/Explosion** accounts for the majority of attacks; **explosives** are the weapon of choice
- **Private Citizens & Property** are the most frequent targets
- The number of **wounded** consistently exceeds the number of **killed** in most incidents
- Suicide attacks are statistically more lethal than non-suicide attacks
- Random Forest outperforms all other classifiers for attack success prediction

---

## 📁 Project Structure

```
Global-Terrorism-Analysis/
│
├── globalterrorism.ipynb        # Main analysis notebook
├── Global Terrorism Data (2).csv  # Dataset (not included in repo)
└── README.md                    # Project documentation
```

---

## 📜 License

This project is for academic purposes only. The dataset is sourced from the Global Terrorism Database (GTD).

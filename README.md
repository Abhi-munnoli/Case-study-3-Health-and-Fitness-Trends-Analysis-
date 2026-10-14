# 🏃 Health and Fitness Trends Analysis Using Python

### VitalityApp Case Study | Data Analysis and Visualization

## 📌 Project Overview

This project analyzes health and fitness activity data from a sample of VitalityApp users to identify daily step-count patterns, compare active and inactive user segments, and explore the relationship between height and weight.

Using Python and data analysis libraries, the project transforms fitness records into descriptive statistics, visualizations, and actionable observations that can support user engagement initiatives.

## 🎯 Project Objectives

- Calculate the average and median daily step counts.
- Identify users recording more than 10,000 daily steps.
- Compare active and inactive users by count and percentage.
- Visualize the distribution of daily steps.
- Examine the relationship between height and weight.
- Summarize fitness activity patterns and provide recommendations.

## 🗂️ Project Structure

```text
health-fitness-trends-analysis/
│
├── README.md
├── Health_Fitness_Trends.ipynb
├── health_fitness_dataset.csv
└── health_fitness_trends_report.pdf
```

## 📁 Dataset Description

The dataset contains **20 VitalityApp user records**. Each record represents a user and includes activity information and body measurements.

| Column | Description |
|---|---|
| `Daily_Steps` | Number of steps recorded by a user in a day |
| `Height_cm` | User height in centimetres |
| `Weight_kg` | User weight in kilograms |
| `Active_User` | Boolean indicator of the user's activity segment |

The report also describes user identifiers and age in the available dataset. Refer to the CSV file for the complete list of columns.

### Activity Segment Definition

The report defines an active user as someone recording at least 8,000 daily steps. The `Active_User` field is used to compare the active and inactive groups.

## 🛠️ Technologies Used

- **Python** — Programming language for analysis
- **Pandas** — Data loading, filtering, and statistical calculations
- **Matplotlib** — Data visualization
- **Google Colab** — Cloud-based notebook execution
- **Jupyter Notebook** — Interactive Python analysis

## ⚙️ Analysis Workflow

### 1. Data Loading and Exploration

Load the fitness dataset into a Pandas DataFrame and inspect its structure, sample size, numeric ranges, and activity-segment values.

### 2. Daily-Step Statistics

Calculate the mean, median, minimum, and maximum daily step counts.

### 3. Users Exceeding 10,000 Steps

Identify users who recorded more than 10,000 steps.

```python
users_over_10000 = (df["Daily_Steps"] > 10000).sum()
print("Users exceeding 10,000 steps:", users_over_10000)
```

### 4. Active and Inactive User Analysis

Summarize user counts and percentages by activity segment.

```python
segment_summary = df["Active_User"].value_counts()
print(segment_summary)
```

### 5. Daily-Step Distribution

Create a histogram to visualize how daily step counts vary across the user sample.

### 6. Height and Weight Relationship

Create a scatter plot comparing height in centimetres with weight in kilograms. Calculate Pearson correlation to describe the observed linear association.

## 📊 Key Findings

The following results are taken from the accompanying PDF report.

### Daily-Step Statistics

| Metric | Result |
|---|---:|
| Users analyzed | 20 |
| Average daily steps | 10,080.8 |
| Median daily steps | 10,229 |
| Minimum daily steps | 3,162 |
| Maximum daily steps | 14,567 |
| Users exceeding 10,000 steps | 10 |
| Percentage exceeding 10,000 steps | 50% |

**Observation:** The sample average is slightly above 10,000 steps per day. Exactly half of the users recorded more than 10,000 steps.

### Active vs. Inactive Users

| Activity Segment | User Count | Percentage | Mean Daily Steps |
|---|---:|---:|---:|
| Active | 14 | 70% | 11,885 |
| Inactive | 6 | 30% | 5,871 |
| Total | 20 | 100% | — |

**Observation:** Most sampled users belong to the active segment. Active users also have a higher observed average daily step count than inactive users.

### Height and Weight Relationship

- **Pearson correlation coefficient:** -0.28
- **Interpretation:** The sample shows a weak negative linear association between height and weight.

The relationship is descriptive only. The small sample does not support broad conclusions about body measurements.

## 📈 Visualizations

The project includes the following charts:

1. **Daily-Step Distribution:** A histogram showing the spread of daily steps among users.
2. **Height vs. Weight:** A scatter plot comparing users' heights and weights.
3. **Activity-Segment Comparison:** A bar chart comparing active and inactive user counts.

These visualizations make it easier to interpret activity patterns and compare the user segments.

## 💡 Recommendations

1. **Encourage less-active users:** Consider achievable step goals, progress reminders, and engagement features for the inactive segment.
2. **Promote consistent activity:** Use the observed activity patterns to inform user engagement initiatives.
3. **Monitor step-count trends:** Analyze activity over longer periods to understand changes in user behavior.
4. **Collect more data:** Include more users and repeated observations to improve the reliability of future analysis.
5. **Avoid unsupported conclusions:** Do not use this small descriptive sample to make medical or causal claims about health outcomes.

## 🚀 How to Run the Project

### Option 1: Google Colab

1. Open [Google Colab](https://colab.research.google.com/).
2. Upload `Health_Fitness_Trends.ipynb`.
3. Upload `health_fitness_dataset.csv` when required.
4. Run the notebook cells sequentially.
5. Review the statistics and visualizations.

### Option 2: Run Locally

**Step 1 — Clone the repository**

```bash
git clone https://github.com/YOUR_USERNAME/health-fitness-trends-analysis.git
```

**Step 2 — Open the project directory**

```bash
cd health-fitness-trends-analysis
```

**Step 3 — Install dependencies**

```bash
pip install pandas matplotlib jupyter
```

**Step 4 — Start Jupyter Notebook**

```bash
jupyter notebook
```

Open `Health_Fitness_Trends.ipynb` and execute the cells.

**Note:** Ensure the notebook reads `health_fitness_dataset.csv` from the project directory. Update any Google Colab upload or file-path code if necessary.

## 📄 Project Report

The `health_fitness_trends_report.pdf` file provides the detailed case study, including:

- Introduction and problem statement.
- Project objectives and tools.
- Dataset description and methodology.
- Daily-step statistics.
- Active/inactive user comparison.
- Height and weight analysis.
- Visualizations and key findings.
- Recommendations and conclusion.

## ⚠️ Limitations

- The dataset contains only 20 users.
- The analysis is descriptive and represents a limited sample.
- No repeated observations are available to assess changes over time.
- Correlation does not establish causation.
- The results should not be treated as medical advice or generalized to all users.

## 🏁 Conclusion

The analysis shows that the 20 sampled users averaged 10,080.8 daily steps, with 70% classified as active under the supplied activity-segment definition. Ten users recorded more than 10,000 daily steps, while the height–weight relationship was weakly negative in this sample.

These findings demonstrate how Python-based data analysis can summarize fitness activity patterns and help inform potential user engagement initiatives. Further analysis using a larger dataset and observations over time would strengthen future insights.

## 👨‍💻 Author

**Abhinandan Babu Munnoli**

Aspiring AI & Machine Learning Engineer | Python Developer | Final-Year Computer Science Engineering Student

- **GitHub:** [Abhi-munnoli](https://github.com/Abhi-munnoli)
- **LinkedIn:** [Connect with me](https://www.linkedin.com/in/abhinandan-munnoli-361a932bb/)

---

⭐ If you find this project useful, consider giving the repository a star.

*Developed as an educational health and fitness data analysis case study.*

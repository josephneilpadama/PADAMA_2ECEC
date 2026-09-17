# Experiment 4: Data Wrangling and Data Visualization

| **Student Information** | **Course & Submission Details** |
| :--- | :--- |
| **Name:** Padama, Joseph Neil C. | **Course Code:** ECE 2112 - Advanced Computer Programming |
| **Section:** 2ECE-C | **Date Submitted:** September 17, 2026 |

---

> **I. Objectives**
> 1. Filter tabular data using several categorical and numerical conditions.
> 2. Construct focused DataFrames by selecting relevant features.
> 3. Summarize the relationship between categorical features and a numerical variable.
> 4. Communicate a data comparison using clear and correctly labeled plots.

## II.  Setup

The initial code imports pandas and matplotlib.pyplot, reads board2.xlsx into a DataFrame named df, and computes the Average score across Math, GEAS, Electronics, and Communication before previewing the first 30 rows.

<details>
<summary><b>Click to Expand: Initial Setup Code and Output</b></summary>

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_excel('board2.xlsx')

if 'Average' not in df.columns:
    df['Average'] = df[['Math', 'GEAS', 'Electronics', 'Communication']].mean(axis=1)

df.head(30)
```
<img src="images/Setup.png" width="800" alt="Setup DataFrame Preview">
</details>

The excel file was loaded using pd.read_excel(). To calculate the total performance score, the student computed the row-wise mean using df[['Math', 'GEAS', 'Electronics', 'Communication']].mean(axis=1) with axis=1 to cover all four board subjects. The student then used df.head(30) to verify that the dataset and new Average column loaded accurately.





















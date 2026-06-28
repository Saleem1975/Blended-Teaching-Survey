# Blended-Teaching-Survey

This repository contains the analysis of the *"Blended Teaching
Experience: Student Satisfaction Survey"*. The survey was designed to
gather feedback from students on their experience with blended learning,
including both online and face-to-face components.

## Data Collection

The data for this survey was collected using Google Forms, ensuring
confidentiality and anonymity for all respondents. The survey included
sections on:

-   **Demographics** (program year, comfort with technology, gender,
    major, current role, and preferred communication media).
-   **Satisfaction Ratings** (using a 5-point Likert scale to assess
    various aspects of blended learning).

## Data Preparation and Wrangling

Before visualizing the data in Power BI and running statistical tests in
Python, several data wrangling steps were performed:

-   ✅ **Unpivoted Columns** -- Converted wide-format data into a more
    analysis-friendly long format.
-   ✅ **Split Columns** -- Separated multi-response fields for clearer
    insights.
-   ✅ **Added Custom Columns** -- Created calculated fields as needed.
-   ✅ **Replaced Values** -- Standardized and cleaned responses for
    consistency.

## Hypothesis Testing Results

To statistically evaluate satisfaction levels, Python was used to
conduct two hypothesis tests on the survey data:

1.  **One-sample t-test (Q9 vs Neutral = 3)**
    -   *Result:* The average satisfaction rating was **2.51** (SD =
        1.38), which is **significantly below the neutral value of 3**
        (*t*(234) = −5.49, *p* = 0.001 for the one-sided test of μ \<
        3).
    -   *Interpretation:* Students, on average, reported
        lower-than-neutral satisfaction with the blended teaching
        experience.
2.  **One-way ANOVA (Q9 by Comfort Level with Technology)**
    -   *Result:* There was a **significant difference** among groups
        (*F*(2, 232) = 7.73, *p* \< 0.001; η² = 0.062).
    -   *Group Means:*
        -   High Comfort: 2.41
        -   Medium Comfort: 2.25
        -   Low Comfort: 3.08
    -   *Post-hoc tests (Tukey HSD):* Confirmed that students with **Low
        comfort** reported significantly higher satisfaction compared to
        both Medium and High comfort groups.
    -   *Nonparametric Check:* A Kruskal--Wallis test supported this
        finding (*H* = 13.72, *p* = 0.001).

**Summary of Insights:**\
- Overall satisfaction was lower than neutral.
- Comfort with technology plays a role: students who reported lower
comfort actually gave higher satisfaction ratings than those with medium
or high comfort.

## Data Analysis and Visualization

In addition to hypothesis testing, Power BI was used to generate
dashboards with:
- Demographic breakdowns (e.g., program year, comfort with technology).
- Satisfaction ratings across different aspects of blended learning.
- Insights into communication media preferences.

## Repository Contents

-   `Blended_Teaching_Experience_Student_Survey.docx`: The original
    survey questionnaire.
-   `Blended_Teaching_Experience_Survey_Results.xlsx`: The collected
    survey responses.
-   `PowerBI_Report.pbix`: The Power BI report (if included).
-   `blended_satisfaction_tests_summary.csv`: Statistical test results
    from Python.
-   `blended_satisfaction_group_descriptives.csv`: Group-level
    descriptive statistics.
-   `blended_satisfaction_tukey_posthoc.csv`: Post-hoc test results.
-   `data/`: (optional) Directory containing cleaned and transformed
    datasets.

## How to Use

1.  **Clone this repository** to your local machine.
2.  Open the Power BI report (`PowerBI_Report.pbix`) to explore
    interactive dashboards.
3.  Review the CSV files generated from Python for detailed statistical
    analysis.
4.  Refer to this README for context on methodology and results.

------------------------------------------------------------------------

If you have any questions or suggestions, feel free to open an issue or
submit a pull request!

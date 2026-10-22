# Healthcare Analytics: Doctor Visits

## About the project

This project looks at doctor-visit patterns across **5,190 people**. It
explores how reported visits relate to illness, days when normal
activities were reduced, age and income codes, gender, and selected
health-support or chronic-condition flags.

The goal is to make the patterns in the data easier to understand. The
analysis describes relationships in the dataset; it does not prove that
one factor causes more or fewer doctor visits.

## Main questions

-   How many people reported no doctor visits, and how many visited at
    least once?
-   How do visit patterns differ across the available health and
    demographic fields?
-   Which factors remain associated with having at least one visit when
    the other listed fields are considered?

## What the analysis does

1.  **Checks the data:** reviews the number of records, missing values,
    duplicate rows, IDs, data types, and value ranges.
2.  **Cleans the data:** standardizes text labels, converts numeric
    fields, and renames the record ID column. No rows are removed
    because the audit found no missing values or duplicate records.
3.  **Explores visit patterns:** summarizes the number of visits and
    compares average visits across groups.
4.  **Checks relationships:** uses rank correlations to assess how
    numeric fields move with visit counts.
5.  **Fits an adjusted model:** estimates which fields are associated
    with having at least one visit while accounting for the other fields
    included in the model.
6.  **Creates charts:** visualizes visit counts, group comparisons,
    correlations, and adjusted model results.

## Key findings

-   **Most people reported no doctor visits.** 4,141 people (79.8%)
    reported zero visits, while 1,049 (20.2%) reported one or more.
-   **Illness count was related to visits.** Average visits generally
    increased as the reported number of illnesses increased.
-   **Reduced-activity days had a clear relationship with visits.**
    People reporting more days when their activities were reduced tended
    to report more visits.
-   **Visit patterns differed across groups.** For example, 24.4% of
    women and 15.6% of men in this dataset reported at least one visit.
    These are descriptive differences and do not explain why the
    difference exists.
-   **Some relationships remained after adjustment.** Illness count and
    reduced-activity days were still associated with having any visit in
    the adjusted model. The model is for statistical analysis, not for
    predicting an individual's medical needs.

## Tools used

-   **Python** for the analysis
-   **Pandas and NumPy** for working with data
-   **Matplotlib and Seaborn** for charts
-   **SciPy** for statistical tests and correlations
-   **Statsmodels** for the adjusted logistic regression model

## Files

-   `Healthcare_Doctor_Visits_Analysis.ipynb` -- the Jupyter Notebook
    containing the analysis, charts, and results.
-   `DoctorVisit.csv` --- the input dataset  
    `Presentation.ppt`-- a stakeholder ready slides explaining important metrics



## Data limitations

-   The supplied notebook does not document the survey period or
    sampling method.
-   The units for the age and income fields are not specified; they are
    treated as coded values in the analysis.
-   The direction of the health code is not documented, so higher or
    lower values cannot safely be described as better or worse health.
-   The data shows associations, not cause and effect. It does not
    establish care quality, unmet medical need, or visits per unit of
    time.
-   The results should be checked against newer and representative data
    before being used to make service or staffing decisions.

## Conclusion

The clearest patterns in this dataset connect doctor visits with
reported illness and days of reduced activity. These findings can guide
further questions about healthcare use, but more information about how
the data was collected and what its coded fields mean is needed before
drawing broader conclusions.

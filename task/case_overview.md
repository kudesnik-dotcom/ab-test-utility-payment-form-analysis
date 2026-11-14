# Utility Bill Payment Form: A/B Test Analysis

## Dataset Overview

This case study examines an A/B test of a redesigned utility bill payment form. The repository contains a **synthetic dataset based on real-world payment data structures and patterns**. The data has been anonymized and modified to protect confidential information and prevent the disclosure of sensitive customer details.

The dataset reflects a realistic experimental setup and includes data-quality issues that require attention during the analysis. The geographical scope is localized to Germany, with cities represented as Berlin, Hamburg, and Other cities.

## Experiment Overview

A payments team conducted an A/B test to evaluate a redesigned utility bill payment form featuring simplified payment-detail entry and autofill functionality.

The experiment compared the existing form (Control) with the redesigned form (Treatment).

**Payment funnel**

1. Payment form opened
2. Payment details entered
3. Payment confirmed
4. Payment successful

**Primary metric:** Conversion rate from opening the payment form (Step 1) to successfully completing a payment (Step 4).

**Business hypothesis:** The redesigned form, with autofilled payment details, will increase the conversion rate of utility bill payments.

**Test duration:** April 1–30, 2024 (30 days).

## Dataset Structure

All data is provided in `AB_test_synthetic.xlsx`, which contains two worksheets:

| Sheet | Approx. rows | Description |
|---|---:|---|
| `Users` | 1,500 | Customer-level information, including `user_id`, experiment `group`, `age`, `city`, and `device_type`. |
| `Pays` | 2,700 | Utility bill payment attempts recorded during the experiment, including timestamps for each funnel stage: `step1_opened`, `step2_entered`, `step3_confirmed`, and `step4_success`. |

A CSV export of the `Users` worksheet is also available as `AB_test_synthetic.csv`.

## Analytical Objective

Evaluate the impact of the redesigned payment form on conversion and determine whether the observed results provide sufficient statistical evidence to justify its rollout to all users.

The analysis should address the following areas:

- **Exploratory Data Analysis:** Examine the dataset structure, distributions, experiment groups, and payment funnel performance.
- **Data Quality:** Identify and handle missing values, invalid records, anomalous observations, and potential outliers. Document the reasoning behind any exclusions or transformations.
- **Visualization:** Present the key findings through clear, informative visualizations.
- **Statistical Inference:** Formulate the null and alternative hypotheses, select an appropriate statistical test, and justify the chosen methodology.
- **Business Recommendation:** Interpret the results in a business context and provide a data-driven recommendation on whether to roll out the redesigned form.

**Important experimental consideration:** The A/B test assignment was performed at the customer level, not the individual payment level. Customers may have multiple payment attempts during the experiment. The statistical analysis must account for this assignment structure and avoid treating repeated observations from the same customer as independent.

## Reporting Format

The final output is a concise analytical report in PDF format (1–2 pages), presenting the methodology, key findings, statistical results, and final business recommendation.

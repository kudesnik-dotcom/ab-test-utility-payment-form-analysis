# Case study: A/B test of a new utility bill payment form

> Note: this is an English adaptation of a real job-application case. The original dataset was not available, so the analysis in this repository runs on a **synthetic dataset** built to mimic the structure and the data-quality problems of the original (localized to Germany: cities are Berlin, Hamburg and Other cities).

## Scenario

Imagine you are a product analyst on the payments team. The team ran an A/B test of a new utility bill payment form with simplified entry of payment details and autofill.

**Utility bill payment funnel**

1. Opened the payment form
2. Entered payment details
3. Confirmed the payment
4. Successful payment

**Key metric:** conversion from step 1 to step 4 (successful payment).

## Data

All data is in one Excel file, `AB_test_synthetic.xlsx`, with two sheets:

| Sheet | Rows | Description |
|---|---|---|
| `Users` | ~1,500 | `user_id`, A/B `group`, `age`, `city`, `device_type` |
| `Pays` | ~2,700 | Utility bill payment attempts during the test (funnel timestamps: `step1_opened`, `step2_entered`, `step3_confirmed`, `step4_success`) |

A CSV copy of the `Users` sheet is provided as `AB_test_synthetic.csv`.

**Hypothesis:** the new form with autofilled payment details will increase the share of successful utility bill payments.

**Test duration:** 30 days (April 1-30, 2024).

## Your task

Analyze the A/B test results and give a recommendation: roll the new form out to all users or not.

The split was done by customers (not by payments). The data may contain invalid records (for example, empty users, anomalous values), so handle them appropriately.

**Areas to cover**

- Exploratory data analysis (EDA)
- Handling outliers and invalid records
- Visualization of results
- Statistical hypothesis testing (justify the chosen method)
- A recommendation based on the data

**Deliverable:** a PDF file (1-2 pages).

# `ab_retirements`

**An end-to-end statistics+ML project testing whether a "nudging" campaign can increase investor contributions to their retirement accounts.
Written by Manuel A. Buen-Abad.**

📄 Description
-----------------------------------------

We consider whether nudging the investors/clients of a financial firm ("ABC Investments") results in a measurable increase in their willingness to increase their yearly contributions to their retirement account, and also whether these additional contributions are larger than usual, within a given timeframe from receiving the nudge (e.g. one month).

To complete this project, I:

1. Collected, queried, and cleaned publicly available data from the SCF (Survey of Consumer Finances, which is run by the Fed and can be found [here](https://www.federalreserve.gov/econres/scfindex.htm?utm_source=chatgpt.com)), which has household-level financial indicators such as retirement accounts balances, income, age, etc. Important assumptions include (_i_) there is one investor per household, and (_ii_) this data is representative of ABC's cross section of investors;
2. Used this data to simulate the features of the investment population of ABC Investments,
3. Further modeled other important features, like percentage contributions to retirement accounts, last time the client logged in to his account, and how much time he spends in his inbox/on-line,
4. Synthesized data from these models, in order to create a population of ABC investors,
5. Modeled the conversion rate and increment in retirement contributions with a logistic regression and a linear regression, respectively, with the features of the investor population as covariates,
6. Designed an A/B experiment, where A is the control group (we leave a sample of the investor population alone) and B is the treatment group (the sample of the investor population we "nudged"),
7. Performed a power analysis and extract the sample mean and 95% C.I. of the observed differences in the conversion rates and the increment in retirement contributions,
8. Analyzed further the statistical properties of the two groups, and simulated what it would look like to monitor the experiment in real time.
9. Did a HTE (Heterogeneous Treatment Effects) analysis (Pearson's chi2, ANOVA) and trained (S) meta-learners for uplift.


📒 Notebook
-----------------------------------------
**Jupyter Notebook**: `ab_retirements.ipynb`

📓 [Up-to-date Notebook](./notebooks/ab_retirements.ipynb)

📌 [Snapshot](./notebooks/index.html)


❓ Requirements
-----------------------------------------

1. python
2. matplotlib
3. seaborn
4. numpy
5. pandas
6. duckdb
7. copulas
8. sdv
9. scikit-learn
10. xgboost

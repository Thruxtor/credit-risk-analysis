# Credit Risk Analysis: Identifying Default Drivers in a Credit Card Portfolio
**Objective:** To explore which customer characteristics are most strongly associated with credit card default, and to test whether mean credit limits differ significantly between defaulters and non-defaulters.

**Dataset:**

**Source:** UCI Machine Learning Repository

**Dataset:** Default of Credit Card Clients — Taiwan, 2005

**Size:** 30,000 customers, 25 variables

**Variables:** Demographic data (age, sex, education, marriage), credit limit, six months of payment history, bill amounts and actual payments made

**Link:** https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients

**Tools Used:**

**Microsoft Excel:** Data Analysis Toolpak, PivotTables, CORREL formula

**Hypothesis:**

**H₀:** The mean credit limit of defaulters and non-defaulters is equal

**H₁:** The mean credit limit of defaulters and non-defaulters is not equal

**Process:**

Cleaned the dataset by removing duplicate rows, handling undocumented category values in the Education and Marriage columns, and verifying data types across all numeric columns. Ran descriptive statistics on key variables, built histograms to assess distribution shape, segmented customers by demographic groups using pivot tables, calculated correlations between key variables and default, and conducted a two-sample t-test to test the hypothesis.

**Key Findings:**

22.1% of customers defaulted roughly 1 in 5, indicating a high risk portfolio

Credit limit was right skewed with a median of 140,000 and mean of 167,484, a small number of high limit customers pulled the average up

High school educated customers had the highest default rate at 25.2%; postgraduates the lowest at 19.2%

Males defaulted more than females — 24.2% vs 20.8%

Recent payment delay (PAY_0) had the strongest correlation with default at 0.325, the single most predictive variable in the dataset

Credit limit had a weak negative correlation with default at -0.154, higher limits are associated with lower default but the relationship is not 

Age had virtually no correlation with default at 0.014, disproving the assumption that older customers are more financially responsible

Defaulters had a mean credit limit of 130,110 vs 178,100 for non-defaulters

**Hypothesis Test Result:**

**Two-sample t-test (unequal variances):**

t-stat = -28.95
p-value ≈ 0

Since p < 0.05 we **reject H₀** and conclude that the difference in mean credit limits between defaulters and non-defaulters is statistically significant and did not occur by chance.

**Conclusion:**

Recent payment behaviour is the strongest predictor of credit default, followed by credit limit as a weak but meaningful signal. Demographic variables like age show no meaningful relationship with default risk. These findings align with how real world credit scoring models are built prioritising payment history over demographic assumptions. The analysis confirms that a bank can meaningfully differentiate between high and low risk customers using payment behaviour and credit limit data alone.

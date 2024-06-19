---
title: Code
---
![](./img/code.png)
### [SAS Code - Income Shifting Measure (Klassen & Laplante 2012 JAR)](https://www.dropbox.com/scl/fi/qb0cocq8emmydg6echp0p/Income-Shifting-Measure.sas?rlkey=n12v9m7u6nntu6c14tm8y2bv2&st=6s74oleg&dl=1)

- **Description** 
SAS code that generates the variables (in 5-year averages) needed to run an income shifting test based on Klassen and Laplante (2012). Subscription to WRDS is required.
- **Output File Name** 
IncomeShift.sas7bdat
- **Main Output Variables** 
GVKEY CIK FIC SIC Datadate Fyear AvgFTR(Tax Incentive) AvgROS(Average Worldwide Return) AvgFROS(Average Foreign Return) AvgDROS(Average Domestic Return) AvgFsale(Average Foreign Sales) AvgDsale(Average Domestic Sales) Avgrd_sale(Average R&D) avgads_sale(Average Advertising Expense) avgintan_sale(Average Intagible Asset) avgcash_at(Average Cash) avgdebt_at(Average Debt) avgsize(Average Asset in logs)
- **Comments** 
    Best practices from prior literature:
    - Exclude obs where FIC is not USA.
    - Remove utilities and financial institutions.
    - Constrain fiscal years to 1997 - 2017 (i.e., pre-TCJA).
    - Include firm-level controls in regressions (included in output file).
    Please email me if you spot any errors or have suggestions - much obliged!
    
---
Data
---
![](./img/data.png)

Forthcoming... WaDaYaNeed?

<style>
h3 {
    margin-top: 0px;
    margin-bottom: 0px;
}
ul {
    margin-top: 0px;
    margin-bottom: 0px;
}
</style>
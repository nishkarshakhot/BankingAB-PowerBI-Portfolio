# 📊 DAX Measures Documentation

This document contains the key DAX measures used in the BankingAB Power BI Dashboard.

---

# Loan Measures

## Total Loan Disbursed

```DAX
Total Loan Disbursed =
SUM(fact_loan_accounts[LoanAmount])
```

---

## Total Deposits

```DAX
Total Deposits =
SUM(fact_deposit_accounts[DepositAmount])
```

---

## Interest Income

```DAX
Interest Income =
SUM(fact_loan_accounts[InterestIncome])
```

---

# Risk Measures

## NPA Ratio

```DAX
NPA Ratio =
DIVIDE([Total NPA Amount],[Total Loan Disbursed],0)
```

---

## Credit Deposit Ratio

```DAX
Credit Deposit Ratio =
DIVIDE([Total Loan Disbursed],[Total Deposits],0)
```

---

# Transaction Measures

## Total Transactions

```DAX
Total Transactions =
COUNTROWS(fact_transactions)
```

---

## Average Transaction Amount

```DAX
Average Transaction =
AVERAGE(fact_transactions[Amount])
```

---

# Time Intelligence

## YTD Loan

```DAX
Loan YTD =
TOTALYTD([Total Loan Disbursed],DimDate[Date])
```

---

## Previous Year Loan

```DAX
Loan Previous Year =
CALCULATE([Total Loan Disbursed],SAMEPERIODLASTYEAR(DimDate[Date]))
```

---

# Dashboard Features

- Dynamic KPIs
- Conditional Formatting
- Drill Through
- Custom Tooltips
- Bookmarks
- Time Intelligence

# 🗄 Oracle SQL Documentation

This project uses Oracle SQL for extracting, transforming, and validating banking data.

## SQL Concepts Demonstrated

- Joins
- CTEs
- Window Functions
- CASE Statements
- Aggregate Functions
- GROUP BY
- HAVING
- Date Functions
- Analytical Functions
- Performance Optimization

---

## Sample Query

```sql
SELECT
    BranchName,
    SUM(LoanAmount) AS TotalLoan
FROM fact_loan_accounts
GROUP BY BranchName
ORDER BY TotalLoan DESC;
```

---

## Database Objects

- Fact Tables
- Dimension Tables
- Views
- Stored Procedures
- Packages

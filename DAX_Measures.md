# DAX Measures
```DAX
Total_sales = SUM('Mobile Sales'[Total_sales])

Total_quantity = SUM('Mobile Sales'[Quantity])

Transaction = COUNTROWS('Mobile Sales')

avg_price = AVERAGE('Mobile Sales'[Price])
```

##  measures

```DAX
Sales per Transaction = DIVIDE([Total_sales], [Transaction])

Payment Share % =
DIVIDE(
    [Transaction],
    CALCULATE([Transaction], ALL('Mobile Sales'[Payment Method]))
)

Avg Rating = AVERAGE('Mobile Sales'[Customer Rating])
```

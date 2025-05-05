# Day-05
# 📊 CSV Column Operations Using Shell

This guide demonstrates how to work with a CSV file (`pqr.csv`) using basic Linux shell commands such as `cut`, `sort`, and `column`.

---

## 📁 Sample CSV (`pqr.csv`)

```csv
ID,Name,age,salary,Department
101,alice,20,70000,Data science
102,Bob,25,50000,Engineering
103,Charlie,5,8000,Data Science
104,David,40,90000,HR
105,Eve,28,60000,Engineering
106,Frank,38,75000,HR
107,Grace,27,72000,Data Science
108,Hank,32,68000,Engineering
109,Ivy,29,62000,Data Science
110,Jack,31,71000,HR

column -t pqr.csv
cut -d ',' -f2 pqr.csv
cut -d ',' -f4 pqr.csv

Sort by salary (ascending):
sort -t ',' -k4,4n pqr.csv

##Sort by age (descending):
sort -t ',' -k3,3nr pqr.csv

Sort by salary (descending):
sort -t ',' -k4,4r pqr.csv





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

## 📂 Files

- **`example03.csv`**: Contains employee details with `ID`, `Name`, `Age`, `Salary`, and `Department`.

---

## 🔧 Key Operations

- **Filter by Department**: Extract employees from `Engineering` department.  
  ```bash
  grep 'Engineering' example03.csv
  ```

- **Extract Age**: Get the `Age` of all employees.  
  ```bash
  awk -F',' '{print $3}' example03.csv
  ```

- **Sort by Salary (Ascending)**: Sort employees by their `Salary`.  
  ```bash
  sort -t',' -k4,4n example03.csv
  ```

- **Sort by Salary (Descending)**: Sort employees by `Salary` in descending order.  
  ```bash
  sort -t',' -k4,4 -r example03.csv
  ```

---

## 🛠 Tools Used

- **`awk`** – For column extraction
- **`cut`** – To slice columns
- **`grep`** – For pattern searching
- **`sort`** – For sorting data

---

## 🚀 How to Use

1. Open `example03.csv`.
2. Run any of the commands to manipulate the data.

---




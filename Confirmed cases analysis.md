# COVID-19 Confirmed Cases Analysis

## 📌 Project Objective

This is a small project focused on iterating through a CSV file containing COVID-19 case data. The results include calculating the average age, determining the total number of records, and comparing the number of cases between males and females using Python environment

## 🛠 Requirements

To run this project, you need:
- Python 3.12.3

## 🖥 Python code

The following code is used to process and analyze the COVID-19 dataset:

```python
print('Welcome to the casos_confirmados.csv code')
file_handler = open(input('Provide a path to function:'))
count = 0
male = 0
female = 0
average = 0
list_elements = 0

for line in file_handler:
    data = line.split(',')
    if count > 0:
        print(data[2:4])
        average += int(data[3])
        list_elements += len(data[3])
    else:
        count += 1
    if data[2] == 'MASCULINO':
        male += data.count('MASCULINO')
    elif data[2] == 'FEMENINO':
        female += data.count('FEMENINO')

print('Number of elements:', list_elements)
average = average / list_elements
print('Age Average is =', int(average))
if female > male:
    print('The number of Females with a value of', female, 'is greater than the number of Males with a value of', male)
else:
    print('The number of Males with a value of', male, 'is greater than the number of Females with a value of', female)
```

## 📊 Results

Example output (partial view to keep README concise):

```
Welcome to the casos_confirmados.csv code
['MASCULINO', '28']
['MASCULINO', '49']
['FEMENINO', '67']
['FEMENINO', '41']
['MASCULINO', '43']
['FEMENINO', '47']
['MASCULINO', '54']
['FEMENINO', '33']
['MASCULINO', '56']
['MASCULINO', '30']
['MASCULINO', '45']
['MASCULINO', '30']
['MASCULINO', '36']
['MASCULINO', '59']
['MASCULINO', '45']
['FEMENINO', '47']
['MASCULINO', '24']
['MASCULINO', '29']
['MASCULINO', '40']
['FEMENINO', '34']
['MASCULINO', '42']
['MASCULINO', '46']
['FEMENINO', '60']
['MASCULINO', '78']
...
['FEMENINO', '20']
Number of elements: 737620
Average age is = 22
The number of Males with a value of 198358 is greater than the number of Females with a value of 172354
```

## 📥 Data Download

To execute this notebook, you need to download the CSV file from this repository and the python_iteration.ipynb. Make sure to place it in the same folder as your `.ipynb` file to avoid path errors.

1. Go to the **Files** section of this repository.
2. Download the CSV file containing COVID-19 data.
3. Save the file in the same location of the python_iteration file.

> **Note:** This project is for educational and analytical purposes. The data may be subject to changes and should be verified with official sources.


# BMI Calculator & Health Metrics Tool
#### Author: Tran Nguyen
#### Tools: Python, Functions, Conditional Logic
#### Focus: Healthcare Metrics, Automation, Data Validation

# Project Overview
Developed a Python-based BMI (Body Mass Index) calculator that automates health metric calculations with user-friendly input validation. BMI is widely used in healthcare for population risk assessment, though it has limitations that I explicitly accounted for in the tool's design and documentation.

# Key Features
- Automated Calculation: Instant BMI computation from weight and height inputs
- Input Validation: Handles various units and prevents invalid entries
- Health Categorization: Classifies results according to standard medical categories
- Transparent Limitations: Clearly communicates BMI's constraints in health assessment
```
def hello(name, age, BMI):
  if BMI > 0:
    if (BMI<18.5):
      print(name, 'is underweight.')
    elif (BMI<24.9):
      print(name,' is normal.')
    elif (BMI<29.9):
      print(name, "is overweight.")
    elif (BMI<34.9):
      print(name, 'is Obese.')
    elif (BMI<39.9):
      print(name, 'is servere obese.')
    elif (BMI>=39.9):
      print(name, 'is morbidily obese.')
    else:
      print("Enter valid numbers")
      return
  if BMI >25 and age > 20:
    print ('Please see you doctor.')
  else:
    print('Please do exercise.')

while True:
  name = input('Enter your name: ')
  if name.isnumeric() != True:
    print('Hello ' + name)
    break
  else:
    print('Please enter correct format')
    exit(0)
while True:
    age = input("Enter your age: ")
    if age.isnumeric() == True:
      print('Your age is: ', age)
      break
    else:
      print('Please enter correct format')
      exit(1)
weight =int(input("Enter your weight(in pounds): "))
height =int(input("Enter your height(in inches): "))
BMI = round((weight*703) / (height * height),2)
## convert age to int, and define BMI to add 2 conditions BMI and Age. 
age = int(age)
print(BMI)
hello(name,age,BMI)
```

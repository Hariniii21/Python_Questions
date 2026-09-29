# Python_Questions
# Name: HARINI S
# Reg no : 212223240048
**1. Print all prime numbers between input range**
```
start = int(input("Enter start: "))
end = int(input("Enter end: "))

for n in range(start, end + 1):
    if n > 1:
        for i in range(2, int(n ** 0.5) + 1):
            if n % i == 0:
                break
        else:
            print(n, end=" ")
```
**Output**
<img width="843" height="322" alt="image" src="https://github.com/user-attachments/assets/a519455b-fea6-44fd-b6cc-ce5a6eb175e1" />

**2.Factorial using recursion**
```
def factorial(n):
    if n == 0 or n == 1:
        return 1
    return n * factorial(n - 1)
n = int(input("Enter a number: "))
print("Factorial =", factorial(n))
```
**OUTPUT**
<img width="830" height="231" alt="image" src="https://github.com/user-attachments/assets/c402dde4-a0f5-4d65-a39a-9c440920c6c8" />

**3. Square of numbers using lambda**
```
square = lambda x: x * x
n = int(input("Enter a number: "))
print("Square =", square(n))
```
**Output**
<img width="821" height="166" alt="image" src="https://github.com/user-attachments/assets/dbc5618c-b20a-48e1-8069-e4d61e173c28" />

**4. Find the second largest element in a list**
```
numbers = list(map(int, input("Enter numbers: ").split()))
unique = list(set(numbers))
unique.sort()
print("Second largest =", unique[-2])
```
**Output**
<img width="847" height="215" alt="image" src="https://github.com/user-attachments/assets/abc0ceff-9b84-421c-a2c4-d42b85b9285c" />

**5. Count frequency of characters in a string**
```
s = input("Enter a string: ")
frequency = {}
for ch in s:
    frequency[ch] = frequency.get(ch, 0) + 1
print(frequency)
```
**Output**
<img width="840" height="238" alt="image" src="https://github.com/user-attachments/assets/6c987182-c798-4092-9559-8a763d2a21d1" />

**6. Calculate area of a circle using math library**
```
import math

radius = float(input("Enter radius: "))
area = math.pi * radius * radius

print("Area of circle =", area)
```
**Output**
<img width="831" height="202" alt="image" src="https://github.com/user-attachments/assets/14d6ce3a-cbc6-4dc8-8d34-a59b9f89b9c2" />

**7. Reverse a string without using built-in reverse**
```
s = input("Enter a string: ")

reverse = ""

for ch in s:
    reverse = ch + reverse

print("Reversed string =", reverse)
```

**Output**
<img width="837" height="243" alt="image" src="https://github.com/user-attachments/assets/cb22bd38-46cb-49b8-b803-6eecab1a586a" />

**8. Remove duplicates from a list**
```
numbers = list(map(int, input("Enter numbers: ").split()))

result = []

for n in numbers:
    if n not in result:
        result.append(n)

print("List after removing duplicates:", result)
```
**Output**
<img width="832" height="270" alt="image" src="https://github.com/user-attachments/assets/d8f52f88-b81d-41a2-ade6-830a750129da" />

**9. Merge two dictionaries**
```
dict1 = {"a": 10, "b": 20}
dict2 = {"c": 30, "d": 40}

dict1.update(dict2)

print("Merged dictionary:", dict1)
```
**Output**
<img width="821" height="187" alt="image" src="https://github.com/user-attachments/assets/be36f44c-7fd0-4e31-abaf-b527bc2946d1" />


**10. Fibonacci series using recursion**
```
def fibonacci(n):
    if n <= 1:
        return n
    return fibonacci(n - 1) + fibonacci(n - 2)

n = int(input("Enter number of terms: "))

for i in range(n):
    print(fibonacci(i), end=" ")
```
**Output**
<img width="828" height="271" alt="image" src="https://github.com/user-attachments/assets/4759d1e2-ddb3-4c8a-b231-dcb5e1f496aa" />

# Python function 
**1.Write a function calculate(a, b, operation) that performs addition, subtraction,multiplication, or division based on the supplied operation**
```
def calculate(a, b, operation):
    if operation == "+":
        return a + b
    elif operation == "-":
        return a - b
    elif operation == "*":
        return a * b
    elif operation == "/":
        return a / b
    else:
        return "Invalid operation"

a = float(input("Enter first number: "))
b = float(input("Enter second number: "))
operation = input("Enter operation (+, -, *, /): ")

print("Result =", calculate(a, b, operation))
```
**Output**
<img width="841" height="480" alt="image" src="https://github.com/user-attachments/assets/72ccb163-569f-4416-9ca6-8f61c0f72e4c" />

**2.Write a function sum_numbers(args) that accepts any number of arguments and returns their sum.**
```
def sum_numbers(*args):
    return sum(args)

print("Sum =", sum_numbers(10, 20, 30, 40))
```
**Output**
<img width="837" height="151" alt="image" src="https://github.com/user-attachments/assets/3d5fc8e6-911c-459a-ae01-acbf05f4b61b" />

**3.Write a function employee(args) that accepts employee information such as name, ID,department and salary, then displays the information.**
```
def employee(**args):
    for key, value in args.items():
        print(key, ":", value)

employee(name="Harini", ID="101", department="AIML", salary=30000)
```
**Output**
<img width="817" height="227" alt="image" src="https://github.com/user-attachments/assets/d30577d0-3de2-4fa4-b566-15cfd732f5ec" />

**4.Write a function remove_duplicates(lst) that returns a list containing only unique elements while preserving their original order.**
```
def remove_duplicates(lst):
    result = []

    for item in lst:
        if item not in result:
            result.append(item)

    return result

numbers = [1, 2, 2, 3, 1, 4, 3, 5]

print("Original list:", numbers)
print("After removing duplicates:", remove_duplicates(numbers))
```
**Output**
<img width="823" height="361" alt="image" src="https://github.com/user-attachments/assets/f27966aa-41f2-4ef7-814c-d298fb349819" />

**Using a lambda function, sort a list of tuples based on the second element. Example: [(1,5), (2,3), (4,1)].**
```
numbers = [(1, 5), (2, 3), (4, 1)]

result = sorted(numbers, key=lambda x: x[1])

print("Sorted list:", result)
```

**Output**
<img width="855" height="193" alt="image" src="https://github.com/user-attachments/assets/8a571e94-d83f-473e-bb35-8b7c5c8d0664" />


# Numpy questions
**1.The marks obtained by five students in a subject are given as [78, 65, 89, 56, 92]. Create a NumPy array and display the array along with its basic properties.**
```
import numpy as np

marks = np.array([78, 65, 89, 56, 92])

print("Marks:", marks)
print("Number of dimensions:", marks.ndim)
print("Shape:", marks.shape)
print("Size:", marks.size)
print("Data type:", marks.dtype)
```
**Output**
<img width="852" height="348" alt="image" src="https://github.com/user-attachments/assets/80926ff7-775a-477d-a692-0b4e1df1bd8f" />


**2.The marks of five students are stored in a NumPy array as [72, 85, 64, 90, 76]. Write a program to access and display specific student marks using NumPy indexing and slicing.**
```
import numpy as np

marks = np.array([72, 85, 64, 90, 76])

print("Marks:", marks)
print("First student:", marks[0])
print("Third student:", marks[2])
print("Last student:", marks[-1])
print("First three students:", marks[:3])
print("Students 2 to 4:", marks[1:4])
```
**Output**
<img width="822" height="351" alt="image" src="https://github.com/user-attachments/assets/d208b96f-a201-4ea4-9d24-9ca6176c7dd1" />


**3.The marks obtained by five students in three subjects are given below. Create a NumPy array to represent the data and reshape it into an appropriate matrix format.[78, 85, 90, 65, 72, 80, 88, 91, 84, 56, 62, 70, 95, 89, 92]**

```
import numpy as np

marks = np.array([78, 85, 90,
                  65, 72, 80,
                  88, 91, 84,
                  56, 62, 70,
                  95, 89, 92])

matrix = marks.reshape(5, 3)

print("Original array:")
print(marks)

print("\nMarks Matrix:")
print(matrix)
```
**Output**
<img width="842" height="513" alt="image" src="https://github.com/user-attachments/assets/5622e426-4eac-4390-8840-8b897ff78a16" />

**4.The internal and external examination marks of five students are stored in two NumPy arrays. Write a program to calculate the final marks of each student using NumPy array operations.**
```
import numpy as np

internal = np.array([20, 18, 22, 19, 21])
external = np.array([65, 70, 60, 68, 72])

final_marks = internal + external

print("Internal marks:", internal)
print("External marks:", external)
print("Final marks:", final_marks)
```
**Output**
<img width="850" height="321" alt="image" src="https://github.com/user-attachments/assets/dc1bf5cf-1e8a-44e4-b3ca-a225b8a3d457" />

**5.The marks obtained by five students are [45, 78, 56, 32, 91]. Using NumPy Boolean masking, identify the students who have secured 50 marks or above.**
```
import numpy as np

marks = np.array([45, 78, 56, 32, 91])

passed = marks >= 50

print("Marks:", marks)
print("Students scoring 50 or above:", marks[passed])
print("Boolean mask:", passed)
```
**Output**
<img width="821" height="270" alt="image" src="https://github.com/user-attachments/assets/04c5a163-45ee-4a15-81b4-de252708e9a1" />

**6.The marks of five students in three subjects are represented using a NumPy matrix. Write a program to calculate the average marks of each student.**
```
import numpy as np
marks = np.array([
    [78, 85, 90],
    [65, 72, 80],
    [88, 91, 84],
    [56, 62, 70],
    [95, 89, 92]
])

average = np.mean(marks, axis=1)

print("Marks Matrix:")
print(marks)

print("\nAverage marks of each student:")
print(average)
```

**Output**
<img width="853" height="558" alt="image" src="https://github.com/user-attachments/assets/9e9da440-f9c5-42b3-9392-f96fb96e6d2e" />


**7.The marks obtained by five students are [67, 82, 91, 74, 58]. Using NumPy statistical functions, determine the total, average, highest, lowest, and standard deviation of the marks.**
```
import numpy as np

marks = np.array([67, 82, 91, 74, 58])

print("Marks:", marks)
print("Total:", np.sum(marks))
print("Average:", np.mean(marks))
print("Highest:", np.max(marks))
print("Lowest:", np.min(marks))
print("Standard Deviation:", np.std(marks))
```

**Output**
<img width="865" height="370" alt="image" src="https://github.com/user-attachments/assets/f44aee33-0625-4bd9-9803-9c5fb0022df4" />


**8.The marks of five students in three subjects are stored in a NumPy matrix. Write a program to calculate the total marks obtained in each subject using an appropriate axis operation.**
```
import numpy as np

marks = np.array([
    [78, 85, 90],
    [65, 72, 80],
    [88, 91, 84],
    [56, 62, 70],
    [95, 89, 92]
])

subject_total = np.sum(marks, axis=0)

print("Marks Matrix:")
print(marks)

print("\nTotal marks in each subject:")
print(subject_total)
```

**Output**
<img width="848" height="583" alt="image" src="https://github.com/user-attachments/assets/c316c5aa-08d2-4000-a473-3b7d9bdc18a1" />


**9.The marks of five students in three subjects are stored in a NumPy matrix. Write a program to calculate the total marks obtained by each student using an appropriate axis operation.**
```
import numpy as np

marks = np.array([
    [78, 85, 90],
    [65, 72, 80],
    [88, 91, 84],
    [56, 62, 70],
    [95, 89, 92]
])

student_total = np.sum(marks, axis=1)

print("Marks Matrix:")
print(marks)

print("\nTotal marks of each student:")
print(student_total)
```

**Output**
<img width="846" height="585" alt="image" src="https://github.com/user-attachments/assets/b100eb3f-54fa-431b-82b7-69b0bfa56222" />


**10.The total marks obtained by five students are [245, 278, 219, 290, 256]. Use NumPy sorting and indexing operations to arrange the marks in order and determine the ranking of the students.**
```
import numpy as np

marks = np.array([245, 278, 219, 290, 256])

sorted_marks = np.sort(marks)[::-1]
ranking = np.argsort(marks)[::-1]

print("Original marks:", marks)
print("Marks in descending order:", sorted_marks)

print("\nRanking:")
for rank, index in enumerate(ranking, start=1):
    print("Rank", rank, "- Student", index + 1, "-", marks[index])
```
**Output**
<img width="832" height="487" alt="image" src="https://github.com/user-attachments/assets/4213a06f-554f-40a9-aa19-e83be3ce306b" />


**11.The marks obtained by five students are [85, 92, 85, 76, 92]. Use NumPy functions to identify the unique marks obtained by the students.**
```
import numpy as np

marks = np.array([85, 92, 85, 76, 92])

unique_marks = np.unique(marks)

print("Marks:", marks)
print("Unique marks:", unique_marks)
```
**Output**
<img width="825" height="247" alt="image" src="https://github.com/user-attachments/assets/ae5c745d-889b-4920-a4e7-25edebf62b99" />

**12.The marks of five students are represented as [78, 85, np.nan, 92, 67], where np.nan represents a missing mark. Write a NumPy program to calculate the average marks without considering the missing value.**
```
import numpy as np

marks = np.array([78, 85, np.nan, 92, 67])

average = np.nanmean(marks)

print("Marks:", marks)
print("Average without missing value:", average)
```

**Output**
<img width="822" height="246" alt="image" src="https://github.com/user-attachments/assets/e3bfb466-8193-4744-867a-9f72a2d9546e" />


**13.The marks obtained by five students are [95, 82, 74, 61, 45]. Using NumPy conditional operations, classify the students into appropriate grade categories based on their marks.**
```
import numpy as np

marks = np.array([95, 82, 74, 61, 45])

grades = np.select(
    [
        marks >= 90,
        marks >= 80,
        marks >= 70,
        marks >= 60
    ],
    [
        "A",
        "B",
        "C",
        "D"
    ],
    default="F"
)

print("Marks:", marks)
print("Grades:", grades)
```
**Output**
<img width="841" height="547" alt="image" src="https://github.com/user-attachments/assets/bf03bde6-f336-4dd8-85dc-c4401325bd49" />


**14.Generate marks for five students using NumPy's random number generation functionality. Perform basic statistical analysis on the generated marks.**
```
import numpy as np

np.random.seed(10)

marks = np.random.randint(0, 101, 5)

print("Randomly generated marks:", marks)
print("Total:", np.sum(marks))
print("Average:", np.mean(marks))
print("Highest:", np.max(marks))
print("Lowest:", np.min(marks))
print("Standard deviation:", np.std(marks))
```
**Output**
<img width="847" height="422" alt="image" src="https://github.com/user-attachments/assets/08d417df-bbc6-4c12-8148-2769a3b13490" />


**15.The marks of five students in three subjects are stored in a NumPy array. Develop a program to perform a complete student performance analysis by calculating the total marks, average marks, highest marks, lowest marks, and identifying students who perform above the class average.**
```
import numpy as np

marks = np.array([
    [78, 85, 90],
    [65, 72, 80],
    [88, 91, 84],
    [56, 62, 70],
    [95, 89, 92]
])

total = np.sum(marks, axis=1)
average = np.mean(marks, axis=1)
highest = np.max(marks, axis=1)
lowest = np.min(marks, axis=1)

class_average = np.mean(marks)

above_average = average > class_average

print("Marks Matrix:")
print(marks)

print("\nTotal marks:")
print(total)

print("\nAverage marks:")
print(average)

print("\nHighest marks:")
print(highest)

print("\nLowest marks:")
print(lowest)

print("\nClass average:", class_average)

print("\nStudents performing above class average:")
for i in range(5):
    if above_average[i]:
        print("Student", i + 1)
```
**Output**
<img width="1143" height="726" alt="image" src="https://github.com/user-attachments/assets/4a9d871b-20f7-49c7-9ac1-1bd8964369b7" />

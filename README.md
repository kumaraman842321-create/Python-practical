Programming Using Python - Practical Record
Student Details
Field	Details
Name	Aman kumar
Course	B.Sc. (Hons.) Computer Science
Semester	I (First Semester)
Roll Number	26570008
Subject	Programming Using Python
College	Ramanujan College, University of Delhi
How to Run
Install Python 3.
Save the program with a .py extension.
Open the terminal in the program's folder.
Run the program using:
python filename.py
CONTENT
Roots of a Quadratic Equation
Prime Numbers
Star Pyramids
Character Classification
String Operations
Swap Prefixes of Two Strings
Substring Indices
Cubes of Even Integers
File Handling
Dictionary of Cubes
Tuple Operations
Employee Class and Object Counting
Class Point2D
Inheritance: Class Point3D
Exception Handling for a Name
Practical 01 - Roots of a Quadratic Equation
Problem: Write a program to find the roots of a quadratic equation.

Code:

import math

a = float(input("Enter a: "))
b = float(input("Enter b: "))
c = float(input("Enter c: "))

if a == 0:
    print("Not a quadratic equation")
else:
    d = b**2 - 4*a*c

    if d > 0:
        r1 = (-b + math.sqrt(d)) / (2*a)
        r2 = (-b - math.sqrt(d)) / (2*a)
        print("Two distinct real roots:", r1, "and", r2)
    elif d == 0:
        print("Equal roots:", -b / (2*a))
    else:
        real = -b / (2*a)
        imag = math.sqrt(-d) / (2*a)
        print(f"Complex roots: {real} ± {imag}i")
Output:

Enter a: 1
Enter b: -5
Enter c: 6
Two distinct real roots: 3.0 and 2.0
Practical 02 – Prime Numbers
Problem Statement: Write a Python program to check whether a given number is prime or not.

Code:

n = int(input("Enter a number: "))

if n <= 1:
    print(n, "is not a prime number")
else:
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            print(n, "is not a prime number")
            break
    else:
        print(n, "is a prime number")
Output:

Enter a number: 17
17 is a prime number
Practical 03 – Star Pyramids
Problem Statement: Write a Python program to print a pyramid pattern using stars.

Code:

n = int(input("Enter the number of rows: "))

for i in range(1, n + 1):
    print(" " * (n - i) + "* " * i)
Output:

Enter the number of rows: 5
    *
   * *
  * * *
 * * * *
* * * * *
Practical 04 – Character Classification
Problem Statement: Write a Python program to classify a character as a vowel, consonant, digit, whitespace, or special character.

Code:

ch = input("Enter a character: ")

if len(ch) != 1:
    print("Please enter a single character")
elif ch.isalpha():
    if ch.lower() in "aeiou":
        print("Vowel")
    else:
        print("Consonant")
elif ch.isdigit():
    print("Digit")
elif ch.isspace():
    print("Whitespace")
else:
    print("Special character")
Output:

Enter a character: A
Vowel
Practical 05 – String Operations
Problem Statement: Write a Python program to perform basic string operations such as finding the length, converting case, reversing a string, and checking whether it is a palindrome.

Code:

s = input("Enter a string: ")

print("Length:", len(s))
print("Uppercase:", s.upper())
print("Lowercase:", s.lower())
print("Reversed:", s[::-1])

if s.lower() == s[::-1].lower():
    print("Palindrome")
else:
    print("Not a palindrome")
Output:

Enter a string: Madam
Length: 5
Uppercase: MADAM
Lowercase: madam
Reversed: madaM
Palindrome
Practical 06 – Swap Prefixes of Two Strings
Problem Statement: Write a Python program to swap the first characters of two strings.

Code:

s1 = input("Enter the first string: ")
s2 = input("Enter the second string: ")

if len(s1) > 0 and len(s2) > 0:
    s1, s2 = s2[0] + s1[1:], s1[0] + s2[1:]
    print("First string:", s1)
    print("Second string:", s2)
else:
    print("Both strings must be non-empty")
Output:

Enter the first string: abc
Enter the second string: xyz
First string: xbc
Second string: ayz
Practical 07 – Substring Indices
Problem Statement: Write a Python program to find all starting indices of a substring in a given string.

Code:

s = input("Enter the main string: ")
sub = input("Enter the substring: ")

indices = []

if sub:
    start = 0
    while True:
        index = s.find(sub, start)
        if index == -1:
            break
        indices.append(index)
        start = index + 1

print("Indices:", indices)
Output:

Enter the main string: banana
Enter the substring: ana
Indices: [1, 3]
Practical 08 – Cubes of Even Integers
Problem Statement: Write a Python program to display the cubes of even integers up to a given number.

Code:

n = int(input("Enter the limit: "))

for i in range(2, n + 1, 2):
    print("Cube of", i, "=", i**3)
Output:

Enter the limit: 10
Cube of 2 = 8
Cube of 4 = 64
Cube of 6 = 216
Cube of 8 = 512
Cube of 10 = 1000
Practical 09 – File Handling
Problem Statement: Write a Python program to write data into a file and then read its contents.

Code:

with open("sample.txt", "w") as file:
    file.write("Hello, Python!\n")
    file.write("File handling example.")

with open("sample.txt", "r") as file:
    content = file.read()

print("File contents:")
print(content)
Output:

File contents:
Hello, Python!
File handling example.
Practical 10 – Dictionary of Cubes
Problem Statement: Write a Python program to create a dictionary containing integers and their cubes.

Code:

n = int(input("Enter the limit: "))

cubes = {i: i**3 for i in range(1, n + 1)}

print("Dictionary of cubes:", cubes)
Output:

Enter the limit: 5
Dictionary of cubes: {1: 1, 2: 8, 3: 27, 4: 64, 5: 125}
Practical 11 – Tuple Operations
Problem Statement: Write a Python program to perform basic tuple operations such as concatenation, repetition, indexing, and slicing.

Code:

t1 = (1, 2, 3)
t2 = (4, 5, 6)

print("First tuple:", t1)
print("Second tuple:", t2)
print("Concatenation:", t1 + t2)
print("Repetition:", t1 * 2)
print("First element:", t1[0])
print("Slicing:", t1[1:])
print("Length:", len(t1))
Output:

First tuple: (1, 2, 3)
Second tuple: (4, 5, 6)
Concatenation: (1, 2, 3, 4, 5, 6)
Repetition: (1, 2, 3, 1, 2, 3)
First element: 1
Slicing: (2, 3)
Length: 3
Practical 12 – Employee Class and Object Counting
Problem Statement: Write a Python program to create an Employee class and count the number of objects created.

Code:

class Employee:
    count = 0

    def __init__(self, name, salary):
        self.name = name
        self.salary = salary
        Employee.count += 1

    def display(self):
        print("Name:", self.name)
        print("Salary:", self.salary)


e1 = Employee("Aman", 25000)
e2 = Employee("Riya", 30000)

e1.display()
e2.display()

print("Total employees:", Employee.count)
Output:

Name: Aman
Salary: 25000
Name: Riya
Salary: 30000
Total employees: 2
Practical 13 – Class Point2D
Problem Statement: Write a Python program to define a Point2D class and display the coordinates of a point.

Code:

class Point2D:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def display(self):
        print("Point:", (self.x, self.y))


p = Point2D(3, 4)
p.display()
Output:

Point: (3, 4)
Practical 14 – Inheritance: Class Point3D
Problem Statement: Write a Python program to demonstrate inheritance by creating a Point3D class derived from Point2D.

Code:

class Point2D:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def display(self):
        print("2D Coordinates:", (self.x, self.y))


class Point3D(Point2D):
    def __init__(self, x, y, z):
        super().__init__(x, y)
        self.z = z

    def display(self):
        print("3D Coordinates:", (self.x, self.y, self.z))


p = Point3D(2, 3, 4)
p.display()
Output:

3D coordinates(2,3,4)
Practical 15 – Exception Handling for a Name
Problem Statement: Write a Python program to accept a name and handle an exception if the name is empty.

Code:

try:
    name = input("Enter your name: ").strip()

    if not name:
        raise ValueError("Name cannot be empty")

    print("Hello,", name)

except ValueError as e:
    print("Error:", e)
Output:

Enter your name: Aman kumar
Hello, Aman kumar


# Module4-Exercises
Module 4 Functions and Errors Exercise Code

We add a Leap Day on February 29, almost every four years. The leap day is an extra, or intercalary day and we add it to the shortest month of the year, February.

In the Gregorian calendar three criteria must be taken into account to identify leap years:

The year can be evenly divided by 4, is a leap year, unless:
The year can be evenly divided by 100, it is NOT a leap year, unless:
The year is also evenly divisible by 400. Then it is a leap year.
This means that in the Gregorian calendar, the years 2000 and 2400 are leap years, while 1800, 1900, 2100, 2200, 2300 and 2500 are NOT leap years.

Task
You are given the year, and you have to write a function to check if the year is leap or not. Simply answer if TRUE or FALSE.

Note that you have to complete the function and remaining code is given as template.

Input Format

Read y, the year that needs to be checked.

Output Format

Output is taken care of by the template. Your function must return a boolean value (True/False)

# Python Program to Check Leap Year using Elif Statement
# This is not correct answer only example

def is_leap(year):
    leap = False
    if year % 4 == 0:
        if year % 100 == 0:
            if year % 400 == 0:
                leap = True
        else:
            leap = False
            
    return leap

print(is_leap(int(input("Year: "))))

Exceptions
Errors detected during execution are called exceptions.

Examples:

ZeroDivisionError
This error is raised when the second argument of a division or modulo operation is zero.

a = '1'
b = '0'
print(int(a) / int(b))
# ZeroDivisionError: integer division or modulo by zero
---------------------------------------------------------------------------
ZeroDivisionError                         Traceback (most recent call last)
Input In [46], in <cell line: 3>()
      1 a = '1'
      2 b = '0'
----> 3 print(int(a) / int(b))

ZeroDivisionError: division by zero

ValueError
This error is raised when a built-in operation or function receives an argument that has the right type but an inappropriate value.

a = '1'
b = '#'
print(int(a)/int(b))
# ValueError: invalid literal for int() with base 10: '#'
---------------------------------------------------------------------------
ValueError                                Traceback (most recent call last)
Input In [20], in <cell line: 3>()
      1 a = '1'
      2 b = '#'
----> 3 print(int(a)/int(b))

ValueError: invalid literal for int() with base 10: '#'

Handling Exceptions
The statements try and except can be used to handle selected exceptions. A try statement may have more than one except clause to specify handlers for different exceptions.

#Code
try:
    print 1/0
except ZeroDivisionError as e:
    print "Error Code:",e
Output

Error Code: integer division or modulo by zero

Task

You are given two values a and b. Perform integer division and print a/b.

Input Format

The first line contains T, the number of test cases. The next T lines each contain the space separated values of a and b.

Output Format

Print the value of a/b. In the case of ZeroDivisionError or ValueError, print the error code.

Sample Input

3
1 0
2 $
3 1
Sample Output

Error Code: integer division or modulo by zero
Error Code: invalid literal for int() with base 10: '$'

for i in range(int(input())):
    try:
        a,b = input().split()
        print(int(a)//int(b))
    except ZeroDivisionError:
        print("Error Code: integer division or modulo by zero")
    except ValueError as err2:
        print("Error Code:",err2)

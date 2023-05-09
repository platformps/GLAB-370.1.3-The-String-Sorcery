# Title: Bug Busters: Debugging Techniques for Python Applications

## Introduction

Debugging is a crucial process in software development that involves identifying and fixing errors or bugs in code. Debugging helps developers ensure that their programs are working as expected and can lead to improved code quality and a better user experience. Python applications, like any other software, can have bugs that affect the program's behavior, and it is essential to find and fix these bugs to prevent errors, crashes, or incorrect output.

Example Code

```
import logging

logging.basicConfig(level=logging.DEBUG)

def factorial(n):
    result = 1
    for i in range(1, n + 1):
        result *= i
    return result

if __name__ == '__main__':
    n = 5
    print(f'The factorial of {n} is {factorial(n)}')
```

## Instructions

### Introduction to Debugging

Debugging is a critical process in software development that involves identifying and fixing errors or bugs in code. Bugs in Python applications can manifest in various forms, such as syntax errors, indentation errors, logical errors, and edge cases. Bugs can cause unexpected behavior, crashes, or incorrect results in programs.

- Have the students create a new Python file and name it program.py.
- They should start by importing the logging module: import logging.
- Explain that print statements are a simple and effective way to debug code by printing variable values, function outputs, and control flow.
- Students should then add print statements and logging statements to the code to debug any issues:

```
import logging

logging.basicConfig(level=logging.DEBUG)

def factorial(n):
    result = 1
    for i in range(1, n + 1):
        logging.debug(f'i={i}, result={result}')
        result *= i
    return result

if __name__ == '__main__':
    n = 5
    print(f'The factorial of {n} is {factorial(n)}')
```

- Explain that this code defines a function that calculates the factorial of a number and logs the intermediate results.
- The print statement shows the final output of the function call.
- Debugging with Python Debugger (pdb)

- Explain how to use the Python debugger (pdb) to step through code, inspect variables, and set breakpoints.
- Have the students run the code in the debugger by adding the following lines to the code:

```
import pdb
pdb.set_trace()
```

This will pause the execution of the program at this point and start the pdb prompt.

- Students can use the n command to step to the next line, the s command to step into a function, the p command to print a variable, and the q command to quit the debugger.
- They should use the debugger to identify and fix any bugs in the code.
- Error Handling with Try-Except Blocks and Logging

- Explain how to handle runtime errors using try-except blocks and how to log error messages using the logging module.
- Have the students modify their code to handle runtime errors by adding a try-except block and logging error messages:
```
import logging

logging.basicConfig(level=logging.DEBUG)

def factorial(n):
    try:
        result = 1
        for i in range(1, n + 1):
            logging.debug(f'i={i}, result={result}')
            result *= i
        return result
    except Exception as e:
        logging.error(f"Error calculating factorial: {e}")

result = factorial(5)
print(result)
```

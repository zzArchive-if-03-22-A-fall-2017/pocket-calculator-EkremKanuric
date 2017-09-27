### IF.03.01 Procedural Programming Winter 2017

# Assignment: Pocket Calculator

## Objective
The goal of this assignment is to make you familiar with primitive data types and functions in C. We do this by implementing a very primitive and text based calculator which asks for an operation and one or two operand(s). The operation is then applied to the operand(s) and the result is finally printed.

## Materials

- Atom or any other editor
- gcc
- terminal.

## Required Tasks
1. **Display Menu and Get Operation:** Implement a function which displays a menu as follows
```
Choose one of the following operations:
   Add (1)
   Subtract (2)
   Multiply (3)
   Divide (4)
   Stop program (-1)
Enter your choice: 
```
Valid input are the numbers 1, 2, 3, 4, or -1. If the user enters a correct number the function shall return the user input. If the user does not input a valid number, the program shall respond with the message `Input not allowed, please try again` and re-prompt the user.

2. **Get Operands:** Write a function which asks the user for two operands:
```
Please enter the first operand: 34.245
Please enter the second operand: 28.4
```
The inputs shall be of type `double` and can be positive as well as negative.

3. **Perform Operation:** Implement a function which performs the right operation based on the input provided.

4. **Division by Zero:** If the user enters 4 (Divide) and 0 as a second operand the calculator shall output `Division by zero`.

5. **Overflow and Underflow:** If the operation would yield a result which is greater than the maximum double or lower than the minimum double number the calculator shall output `Number overflow` or `Number underflow`, respectively.

6. **Repetition:** Make your program to repeat from the beginning as soon as a calculation is ready. The user can stop the program by typing -1 as an operation (see Required Task # 1).

## Hints
- Functions which have to return two values (as the one asking for the operands) have to do this via call by reference.
- To get the maximum and minimum double one can use the constants `DBL_MAX` and `DBL_MIN` from `float.h`.
- Take care that the following code snippet does not make any sense (Why?):
```
if (x > DBL_MIN) {
   printf("Number overflow\n");
}
```

## Evaluation
All coding assignments will get checked. Most common reasons that your assignment is marked down are:

- Program does not build or builds with warnings
- One or more items in the *Required Tasks* section are not satisfied
- Submitted code is visually sloppy and hard to read

## Things to Learn
- Using primitive data types, like integer, float/doubles
- Implementing functions

## Extra Credit
The three examples to gain extra credit all include to extend the menu of available operations, to extend the function which chooses the right function to be called and finally the implementation of the function which does the operation.

1. **Power:** Implement the functionality which takes the first operand to the power of the second operand
2. **Square Root:** Implement the functionality which takes the square root of a number. Take care that one needs only one operand for the square root. Search the web to find the header file to be included and the name of the function to be called. Furthermore take care that you have to add the option `-lm` to the call of the `gcc` command to build your program successfully. Furthermore check that the operand must not be negative if you calculate the square root. If the user enters a negative number a message `The square root of a negative number is not defined` shall be displayed.
3. **Arithmetic Series:** Write a program which calculates the Sum of all numbers 1 + 2 + 3 + ... n of a given operand n. Again the user shall be prompted only for one operand in this case and the entered operand must not be smaller than 1.

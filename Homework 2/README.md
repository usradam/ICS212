# ICS 212 - Homework 2

## 📒 Table of Numbers [5 pts]
Create a source file `homework2.c` and write code which generates a table of numbers from 0 to the maximum number specified by the user. The table has a column telling if each number is **Multiple of 3 or not**. The user interface will ask the user for the maximum number to print.

When you run your program, it should look like this below. You must print **a brief description about the program at the beginning of the output** (so replace the `< ... >` part with your description).

```
< Print a brief introductory message describing your program >

Enter maximum number to show:
```

Then, the program must wait for the user input. Let's say the user gave `15`. The program prints 0 through 15 with the additional column.

```
*** Print a brief introductory message describing your program ***

Enter maximum number to show: 15
  Number  Multiple of 3?
       0   No
       1   No
       2   No
       3  Yes
       4   No
       5   No
       6  Yes
       7   No
       8   No
       9  Yes
      10   No
      11   No
      12  Yes
      13   No
      14   No
      15  Yes
```

## User Interface
- Define a `user_interface` function to get the user input.
`int user_interface();`

- This function is to achieve the following tasks.
  - Print the brief introductory message explaining about your program.
  - Print `Enter maximum number to show:`
  - Get the user input
  - Return the gained value
    
- This function must be called by `main`.

## Invalid inputs
- If the given value is **a character or a string**, `user_interface` must **display an error message** AND **prompt the user to enter an integer**. You only need to test for the input of characters and integers. You do not have to worry about floats being entered. Also, if the input is like `123abc`, you can either extract the number or simply consider it as an invalid input.

- If the given number is **less than or equal to 0**, `user_interface` must **display an error message** AND **prompt the user to enter a positive integer**.

- After the program prompts the user to enter a valid input, it **MUST NOT** exit. (it must ask the user for an input until the user gives a valid input.)

## Function to check if the number is Multiple of 3
- Define a function `is_multiple3` with the following prototype:
`int is_multiple3(int);`

- The `is_multiple3` function takes an integer and returns 1 if the number is **Multiple of 3**. Otherwise, it returns 0.

- Note: this function is **NOT** supposed to print anything to the terminal.

## Print Function
- Define a `print_table` function which uses a for-loop to generate a table, starting from 0 to the given maximum number, with the additional column. (see the sample above)
`void print_table(int);`

- The table must be formatted. (see the sample above)

- Columns must be **right-aligned**.

*What is "right-aligned"?*
```
  1
 15
350
```

- This function must be called by `main`.

## Testing
Test your program to show that it works correctly.

1. Think what test cases can verify that your code achieves the requirements.

**Don't just provide many randomized test cases. You should be able to explain the purpose of each test case.**

2. Provide a recorded file (`output.txt`) of testing results. ("recorded file"? Use the `script` command)

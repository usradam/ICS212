# ICS 212 - Homework 0

## Pseudocode [4 pts]
You will write pseudocode to achieve the task described below. Please note that pseudocode is **NOT** the C language at all. Some of you may think of writing C code first and then "translate" it into pseudocode. But **please don't do this!!!** Many students in the past did this and eventually suffered from a lot of problems in the later assignments.

Plus, we are going to use **our own vocabulary** for pseudocode, which is not the same as what you can find on the Internet or in some textbook of algorithm. That is, **please carefully check the vocabulary list and use only the available rules.**

${{\color{Red}\normalsize{\textsf{If your pseudocode contains significant amount of invalid usage, you will get 0pt}}}}\$

## Vocabulary
Use ${{\color{Red}\normalsize{\textsf{ONLY}}}}\$ the following vocabulary.

*replace the bold parts with your variables and expressions.*

- define an int called **variable_name**

example:
```
define an int called i
```
- copy from **expression** to **variable_name**

note: the data type of **expression** must match that of **variable_name**

example:
```
copy from 1+1 to i
copy from 100 to i
copy from numbers[0] to i
copy from i to numbers[i]
```

- while (**boolean_expression**)
 - note1: inside a while loop, put 4 white spaces for indents
 - note2: you CANNOT use a break statement.
example:

while ( i < 10 )
    copy from 0 to numbers[i]
    copy from i + 1 to i
do-while

note1: inside a while loop, put 4 white spaces for indents
note2: you CANNOT use a break statement.
example:

do
    copy from 0 to numbers[i]
    copy from i + 1 to i
while (i < 10)
if (boolean_expression)

note1: inside an if statement, put 4 white spaces for indents
node2: you can use "else".
example:

if ( i < 10 )
    copy from 0 to i
else if ( i < 20 )
    copy from 10 to i
else
    copy from 20 to i
Combining boolean expressions

If necessary, you may use "&&" and "||" to combine comparisons
example:

if ( 0 <= i && i < 10 )
  ...
else if ( j < 5 || 8 < j )
  ...

## Example of Pseudocode
Here is an example of pseudocode which initializes an element of numbers with 0 if it is less than 10. Your pseudocode must follow the same format. You can insert blank lines so that the pseudocode is more readable. Make sure that you always use white spaces for indents. (Never use the Tab key!)

```
define an int called i

copy from 0 to i
while ( i < m )
    if ( numbers[i] < 10 )
        copy from 0 to numbers[i]

    copy from i + 1 to i
```

## Task
Assume you have the following variables and values:

An integer variable called num with some integer value.

An integer array called numbers with n elements (n > 0)

Some integer values are stored in the first m slots of the array (0 <= m < n).

The m integers are already sorted in an increasing order.

Note: An integer value can be negative.

Write your pseudocode achieving the following requirements. Use and modify this template file: pseudocode.txt.

Insert the value of num into the array numbers. The resulting integers must be in an increasing order.

example:



Once num is inserted into numbers, update m so it indicates the correct number of items in the array.

As mentioned above, you can assume the following variables are already defined and you can access them in your pseudocode (so you do not need to define these variables in your pseudocode):

numbers (array of int)
n (int)
m (int)
num (int)

## FAQs
Q: "Can I assume that the uninitialized elements of the array hold 0 or a special value?"

A: No. They are just uninitialized. They may have 1, -47, 0, or any possible integer value.

Q: "In pseudocode.txt, do I need to keep/modify the header?"

A: You don't have to. The header is just for a reminder about the assumptions. You can just start your pseudocode after the header.

Q: "Can I use a for-loop?"

A: No. Use while or do-while as shown in the vocabulary list.

Q: "Can I define/call a function?"

A: No.

Q: "I don't understand what the 'copy from ...' line means."

A: When you have copy from 1 + 1 to i, you are assigning 1+1, which is 2, to the variable i, so i will have 2. When you have copy from i + 1 to i, you are incrementing i, so it will have a value greater than the previous value by 1.

Q: "Can I define a variable and initialize it in one line?"

A: No. Assign an initial value to it in another line after you define the variable.

Q: "Can I define another array?"

A: No.

Q: "I am attaching my pseudocode.txt. Could you tell me if it is correct?"

A: Please at least trace your pseudocode with specific values. (Otherwise, I will just tell you if it correctly uses the vocabulary or not) You can just draw a table on a piece of paper in a similar way as you do on C code in the classes, and put some specific values. Then, run your pseudocode by each line.

Here are some examples. Note that your pseudocode must work on other possible cases.

- Case 1:
n = 5
m = 3
num = 5
numbers = [3, 6, 8, X, X]

- Case 2:
n = 5
m = 0
num = 0
numbers = [X, X, X, X, X]

- Case 3:
n = 5
m = 2
num = -5
numbers = [0, 2, X, X, X]

- Case 4:
n = 5
m = 3
num = 9
numbers = [-10, 0, 3, X, X]

While testing, you may want to ask yourself for some questions.

For example,
- Does it accidentally use an invalid space or an undefined variable?
- Could it cause infinite loops?
- Are the assumed variables correctly updated at the end?

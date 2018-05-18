# Lesson 3
* Conditionals if, not
* Boolean algebra intro
* Nested conditions
* Indentation, function scope (VERY HARD)
* For any kind of logic or control flow, we need conditional statements.

## Booleans
* For conditionals, we work with the boolean data type, which is either `True` or `False`
* Note a boolean is a data type we can assign to a variable!
* We create a boolean using comparison operators
```python
# Basic comparison operators
x = 3 # This is not equal! This is a declaration!
x > 3 # False
x >= 3 # True
x < 5  # True
x <= 2  # False
x == 3  # is x equal to three? Yes!
x != 4  # is x not equal to 4? Yes!
y = x != 4  # Evaluate x is not equal to 4, save the result to y
```

## Conditionals
* The basic conditional is if <expression>:
* If the logical expression is true, the if will run the indented commands. Otherwise nothing will happen
* We also have else. If the condition in the if evaluates to False, the else branch gets run. Either the code in the if section runs, or the code in the else section runs. Never both!
```python
x = 4
if x == 4:
    print("this should be printed out)
print("This should also be printed out")
```
```python
x = 4
if x == 4:
    print("this should be printed out)
else:
    print("This should NOT be printed out")
print("This should be printed out again")
```

## Boolean algebra
* To combine conditions, we can use `and` and `or` operators
* To invert a truth value use `not`
* **NOTE** make truth value tables

## Nested conditions
* For more complex schemes, we can nest if statements in each other.
* It is often better to combine them into **and** statements, sometimes it is not possible

```python
if x > 2:
    if x < 4:
        print("x is between 2 and 4")
# OR
if x > 2 and x < 4:
    print("x is between 2 and 4")

# OR
if 2 < x < 4:
    print("x is between 2 and 4")    
```

## Exercises
### Upgrade your scripts from the first and second lesson.
* For the age calculator, test if their age is over 65 and output something different
* For the BMI calculator, do a quick check if people used meters instead of centimeters (the height should be over 100cm, for example)

### Mini scripts
* Make a script that takes 2 numbers and says which one is bigger (note, don't just print the number, tell which one is larger! I.e. the first or the second)
* Make a script that takes a numberic input and gives you it's absolute value (if x is -5, it prints 5)

## Calculator
* Create a calculator! A script that asks you for 2 numbers, then asks you whether you want to add, subtract, multiply or divide them. Use if for the resposne and do the operation

## Blood pressure
* Tell if a user has high blood pressure. A user has high blood pressure if his systolic pressusure is more than 120 or diastolic pressure is higher than 80. The script should ask the users for both values and respond whether he has high blood pressure or not

```python
systolic = int(input("Give me your systolic pressure:"))
diastolic = int(input("Give me your diastolic pressure:"))
if (systolic > 120) or (diastolic > 80):
    print("High pressure")
else:
    print("Low pressure")

```

### Reading exercise
* What will happen? Try to guess before running it in the python shell

```python
(5 > 4) and (3 == 5)
not (5 > 4)
(5 > 4) or (3 == 5)
not ((5 > 4) or (3 == 5))
(True and True) and (True == False)
(not False) or (not True)
```

### University grading
* Make a script that takes a number between 0 and 100 (check it!) and returns an university grading

| Points | Grade |
|---|---|
|100 - 90| A |
|89 - 80| B |
|79 - 70| C |
|69 - 60| D |
|59 - 50| E |
|< 50| F |


### Simple ATM
* program a simple ATM @Dacos
* let the user input his card number, pin and how much money he wants
* If the card is not 43-1199223344, say "wrong card!"
* if the card is correct, proceed to check the pin. If the pin is not 3194, say "wrong pin!"
* if both card and pin are correct, check if he has enough money on his account (1000,- czk) he can take out
* If he has, say "Ok, paying [number] Kc, otherwise say "not enough money on your account"

# Hackaday #1
* Ifs are a big part of computing, we can show them examples of scripts that make our lives better. If someone has a good suggestion, you can do live coding

# Notes
* People often try to put the results of a function in a if statement
```
if x = input() < 3:
```

Discourage that
* People also tend to insert too many statements into one if
```
if x > 4 and 5:
    <code>
```
Is semantically wrong, because x > 4 gets evaluated to 4 and then you compare True and 5.
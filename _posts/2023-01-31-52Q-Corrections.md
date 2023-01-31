---
toc: true
layout: post
description: 52Q Practice Exam MCQ - Pranav
categories: [markdown]
title: AP CSA Test Corrections
---

# Score: 45/52

## Question 4
![image](https://user-images.githubusercontent.com/89223545/200725027-0ddd3aa8-0d29-4558-9c75-8b4461577e9d.png)
- Answer B
Incorrect. This would be the result if the division used was floating point division, instead of integer division. This would be the case if either x or y were of type double instead of type int or if either value was typecast as a double in the expression.
- Answer C
Correct. When we evaluate the express(x < 10) && (y < 0) for x having the value 7 and y having the value 3, x < 10 evaluates to true, since 7 is less than 10, and y < 0 evaluates to false, since 3 is not less than 0. The logic operator && evaluates to true when both conditions are true and evaluates to false otherwise. Since the second condition is false, the boolean expression is false. As a result, the compiler will skip the first output statement and execute the statement in the else. The expression x / y is integer division for 7 / 3, which is 2.
- This was more of a conceptual error as I didn't read the code segment thoroughly resulting in the wrong output being displayed when I looked at it.

## Question 11
![image](https://user-images.githubusercontent.com/89223545/200725117-f9e4cab8-ced9-4abd-88bd-9ad28380872b.png)
- Answer A
Incorrect. This will prevent an ArrayIndexOutOfBoundsException from being thrown if target does not appear in data, however if target is at element 0, -1 will be returned instead of 0 as intended.
- Answer B
Correct. The seqSearchRecHelper recursive method does not work as intended when target does not appear in data. In this case, when last becomes -1, the method will throw an ArrayIndexOutOfBoundsException in the first if statement after line 1. To prevent this, we should add a check to see if last is less than 0 and if it is, return -1 as expected.
- I did this wrong because if you look at the function, the main target wasn't displaying the correct output.

## Question 18
![image](https://user-images.githubusercontent.com/89223545/200725184-acda4587-ef65-442a-ae74-871fd7f26cdb.png)
- Answer D
Incorrect. The indices for myList are 0 through myList.size() – 1, for a total of myList.size() elements. Adding 1 to myList.size() and then multiplying Math.random() by this value results in a range that is from 0 to myList.size(), which is one element too many.
- Answer B
Correct. The indices for myList are 0 through myList.size() – 1, for a total of myList.size() elements. Using Math.random()generates a random floating point number between 0 and 1, not including 1. When this value is multiplied by the number of elements we want in our range, myList.size(), a random floating point number between 0 and myList.size(), not including myList.size(), is generated. When this value is typecast as an int, the result is an integer value between 0 and myList.size() – 1 inclusive.
- In order to get this correct in the future, I plan on studying both topic 2.9 and 7.2 as they cover Arraylists.

## Question 23
![image](https://user-images.githubusercontent.com/89223545/200725250-216fe022-a538-49a8-b9da-131f201e6045.png)
- Answer C
Incorrect. List is an interface, which an ArrayList implements. Please note that List is no longer tested as part of the AP CSA exam and ArrayList will be used instead. This would be the correct answer if the remove occurred before the size was calculated in the statement animals.add(animals.size()-k, animals.remove(k)); and only one iteration of the loop occurred.
- Answer B
Correct. List is an interface, which an ArrayList implements. Please note that List is no longer tested as part of the AP CSA exam and ArrayList will be used instead. The manipulate method contains a for loop with a loop control variable k that starts at the right most index of animals, decrements by 1 each time, until k is equal to 0. In the first iteration, when k is 5, if the element of animals at 5 (“baboon”) starts with a “b”, which it does, then this value is removed from the list and inserted at index 1. The list would then be {“bear”, “baboon”, “zebra”, “bass”, “cat”, “koala”}. 
- To fix this I will focus on topics 2.7 and 7.4 as they cover instatizing and initializing lists.

## Question 24
![image](https://user-images.githubusercontent.com/89223545/200725281-c7e46bb6-4757-42da-9f65-dcc58a5c135a.png)
- Answer C
Incorrect. The value 5 is at newArray[1][1].
- Answer D
Correct. The enhanced for loop iterates over the array oldArray. In the first iteration, newArray[0][0] is assigned the value 1. The value of row is incremented to 1. Since 1 % 3 does not equal 0, the statements in the if are not executed. In the next iteration, newArray[1][0] is assigned the value 2. The value of row is incremented to 2. The algorithm continues to fill column 0 with the subsequent values of oldArray. Once row is 3, the if condition is true and row is assigned 0 and col is incremented to 1. The algorithm proceeds to fill column 1. 
- Resources: 8.1: Daily Video 1 (Skill 3.E), 8.1: Daily Video 2 (Skill 3.E), 8.1: Daily Video 3 (Skill 1.B)

## Question 34
![image](https://user-images.githubusercontent.com/89223545/200725349-c765eeb1-f822-413c-8a52-2f73740eb48c.png)
- Answer D
Incorrect. Choice III uses the default Point constructor to assign center a new Point with x and y both equal to 0. It attempts to update x and y, however since they are private instance variables in Point, they are not able to be accessed directly in Circle. This code will cause a compile time error.
- Answer B
Correct. Choice I uses the no parameter Point constructor to assign center a new Point with x and y both equal to 0, instead of x assigned the value a and y assigned the value b. Choice II correctly uses the two parameter Point constructor to create a new Point with x assigned the value a and y assigned the value b. Choice III uses the no parameter Point constructor to assign center a new Point with x and y both equal to 0. It attempts to update x and y, however since they are private instance variables in Point, they are not able to be accessed directly in Circle. This code will cause a compile time error.
- There is a compiling error that comes out of the answer in option D due to the way in which the constructor assigns a new point.

## Question 52
![image](https://user-images.githubusercontent.com/89223545/200725027-0ddd3aa8-0d29-4558-9c75-8b4461577e9d.png)
- Answer B
Incorrect. This would be the result if the division used was floating point division, instead of integer division. This would be the case if either x or y were of type double instead of type int or if either value was typecast as a double in the expression.
- Answer C
Correct. When we evaluate the express(x < 10) && (y < 0) for x having the value 7 and y having the value 3, x < 10 evaluates to true, since 7 is less than 10, and y < 0 evaluates to false, since 3 is not less than 0. The logic operator && evaluates to true when both conditions are true and evaluates to false otherwise. Since the second condition is false, the boolean expression is false. As a result, the compiler will skip the first output statement and execute the statement in the else. The expression x / y is integer division for 7 / 3, which is 2.
- This was more of a conceptual error as I didn't read the code segment thoroughly resulting in the wrong output being displayed when I looked at it.
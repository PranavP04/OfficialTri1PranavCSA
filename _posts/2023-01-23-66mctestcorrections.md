---
toc: true
layout: post
description: 66 Questions MCQ
categories: [markdown]
title: AP CSA Test Corrections
---
# Score: 53/66
## Question 8
![image](https://user-images.githubusercontent.com/89223545/214115584-83c848bc-e4cb-49c7-913e-72f20c268228.png)
- Answer B
Incorrect. This would be the result if the division used was floating point division, instead of integer division. This would be the case if either x or y were of type double instead of type int or if either value was typecast as a double in the expression.
- Answer C
Correct. When we evaluate the express(x < 10) && (y < 0) for x having the value 7 and y having the value 3, x < 10 evaluates to true, since 7 is less than 10, and y < 0 evaluates to false, since 3 is not less than 0. The logic operator && evaluates to true when both conditions are true and evaluates to false otherwise. Since the second condition is false, the boolean expression is false. As a result, the compiler will skip the first output statement and execute the statement in the else. The expression x / y is integer division for 7 / 3, which is 2.
- This was more of a conceptual error as I didn't read the code segment thoroughly resulting in the wrong output being displayed when I looked at it.

## Question 19
![image](https://user-images.githubusercontent.com/89223545/214115905-3636d050-abe4-4a23-a4fd-c983d9087284.png)
- Answer E
Incorrect. This will prevent an ArrayIndexOutOfBoundsException from being thrown if target does not appear in data, however if target is at element 0, -1 will be returned instead of 0 as intended.
- Answer A
Correct. The seqSearchRecHelper recursive method does not work as intended when target does not appear in data. In this case, when last becomes -1, the method will throw an ArrayIndexOutOfBoundsException in the first if statement after line 1. To prevent this, we should add a check to see if last is less than 0 and if it is, return -1 as expected.
- I did this wrong because if you look at the function, the main target wasn't displaying the correct output.

## Question 21
![image](https://user-images.githubusercontent.com/89223545/214115999-f279b380-e352-4606-b18d-13ed31009b5d.png)
- Answer C
Incorrect. The indices for myList are 0 through myList.size() – 1, for a total of myList.size() elements. Adding 1 to myList.size() and then multiplying Math.random() by this value results in a range that is from 0 to myList.size(), which is one element too many.
- Answer D
Correct. The indices for myList are 0 through myList.size() – 1, for a total of myList.size() elements. Using Math.random()generates a random floating point number between 0 and 1, not including 1. When this value is multiplied by the number of elements we want in our range, myList.size(), a random floating point number between 0 and myList.size(), not including myList.size(), is generated. When this value is typecast as an int, the result is an integer value between 0 and myList.size() – 1 inclusive.
- In order to get this correct in the future, I plan on studying both topic 2.9 and 7.2 as they cover Arraylists.

## Question 35
![image](https://user-images.githubusercontent.com/89223545/214116215-a2a0b533-c727-47c3-97bf-5c89641a22f9.png)
- Answer C
Incorrect. List is an interface, which an ArrayList implements. Please note that List is no longer tested as part of the AP CSA exam and ArrayList will be used instead. This would be the correct answer if the remove occurred before the size was calculated in the statement animals.add(animals.size()-k, animals.remove(k)); and only one iteration of the loop occurred.
- Answer B
Correct. List is an interface, which an ArrayList implements. Please note that List is no longer tested as part of the AP CSA exam and ArrayList will be used instead. The manipulate method contains a for loop with a loop control variable k that starts at the right most index of animals, decrements by 1 each time, until k is equal to 0. In the first iteration, when k is 5, if the element of animals at 5 (“baboon”) starts with a “b”, which it does, then this value is removed from the list and inserted at index 1. The list would then be {“bear”, “baboon”, “zebra”, “bass”, “cat”, “koala”}. 
- To fix this I will focus on topics 2.7 and 7.4 as they cover instatizing and initializing lists.

## Question 42
![image](https://user-images.githubusercontent.com/89223545/214116362-fdf6a736-47e2-4d1e-a5a0-d1d90f18af3e.png)
- Answer C
Incorrect. The value 5 is at newArray[1][1].
- Answer D
Correct. The enhanced for loop iterates over the array oldArray. In the first iteration, newArray[0][0] is assigned the value 1. The value of row is incremented to 1. Since 1 % 3 does not equal 0, the statements in the if are not executed. In the next iteration, newArray[1][0] is assigned the value 2. The value of row is incremented to 2. The algorithm continues to fill column 0 with the subsequent values of oldArray. Once row is 3, the if condition is true and row is assigned 0 and col is incremented to 1. The algorithm proceeds to fill column 1. 
- Resources: 8.1: Daily Video 1 (Skill 3.E), 8.1: Daily Video 2 (Skill 3.E), 8.1: Daily Video 3 (Skill 1.B)

## Question 49
![image](https://user-images.githubusercontent.com/89223545/214116574-968760df-92ee-4c7f-8c63-e3dffea9e8a5.png)
- Answer D
Incorrect. Choice III uses the default Point constructor to assign center a new Point with x and y both equal to 0. It attempts to update x and y, however since they are private instance variables in Point, they are not able to be accessed directly in Circle. This code will cause a compile time error.
- Answer B
Correct. Choice I uses the no parameter Point constructor to assign center a new Point with x and y both equal to 0, instead of x assigned the value a and y assigned the value b. Choice II correctly uses the two parameter Point constructor to create a new Point with x assigned the value a and y assigned the value b. Choice III uses the no parameter Point constructor to assign center a new Point with x and y both equal to 0. It attempts to update x and y, however since they are private instance variables in Point, they are not able to be accessed directly in Circle. This code will cause a compile time error.
- There is a compiling error that comes out of the answer in option D due to the way in which the constructor assigns a new point.

## Question 56
![image](https://user-images.githubusercontent.com/89223545/214116716-2941c60d-ee7e-4cfd-b6db-b7b1f0ab74b3.png)
- Answer D
Incorrect. Choice III uses the default Point constructor to assign center a new Point with x and y both equal to 0. It attempts to update x and y, however since they are private instance variables in Point, they are not able to be accessed directly in Circle. This code will cause a compile time error.
- Answer B
Correct. Choice I uses the no parameter Point constructor to assign center a new Point with x and y both equal to 0, instead of x assigned the value a and y assigned the value b. Choice II correctly uses the two parameter Point constructor to create a new Point with x assigned the value a and y assigned the value b. Choice III uses the no parameter Point constructor to assign center a new Point with x and y both equal to 0. It attempts to update x and y, however since they are private instance variables in Point, they are not able to be accessed directly in Circle. This code will cause a compile time error.
- There is a compiling error that comes out of the answer in option D due to the way in which the constructor assigns a new point.


## Question 58
![image](https://user-images.githubusercontent.com/89223545/214116987-391b9185-a42e-4922-9a05-be848146f89e.png)
- Answer B
Incorrect. Choice III uses the default Point constructor to assign center a new Point with x and y both equal to 0. It attempts to update x and y, however since they are private instance variables in Point, they are not able to be accessed directly in Circle. This code will cause a compile time error.
- Answer E
Correct. Choice I uses the no parameter Point constructor to assign center a new Point with x and y both equal to 0, instead of x assigned the value a and y assigned the value b. Choice II correctly uses the two parameter Point constructor to create a new Point with x assigned the value a and y assigned the value b. Choice III uses the no parameter Point constructor to assign center a new Point with x and y both equal to 0. It attempts to update x and y, however since they are private instance variables in Point, they are not able to be accessed directly in Circle. This code will cause a compile time error.
- There is a compiling error that comes out of the answer in option D due to the way in which the constructor assigns a new point.

## Question 59
![image](https://user-images.githubusercontent.com/89223545/214117383-bc9da263-ba3e-466f-8c02-660c175cdc11.png)
- Answer C
Incorrect. Choice III uses the default Point constructor to assign center a new Point with x and y both equal to 0. It attempts to update x and y, however since they are private instance variables in Point, they are not able to be accessed directly in Circle. This code will cause a compile time error.
- Answer B
Correct. Choice I uses the no parameter Point constructor to assign center a new Point with x and y both equal to 0, instead of x assigned the value a and y assigned the value b. Choice II correctly uses the two parameter Point constructor to create a new Point with x assigned the value a and y assigned the value b. Choice III uses the no parameter Point constructor to assign center a new Point with x and y both equal to 0. It attempts to update x and y, however since they are private instance variables in Point, they are not able to be accessed directly in Circle. This code will cause a compile time error.
- There is a compiling error that comes out of the answer in option D due to the way in which the constructor assigns a new point.

## Question 63
![image](https://user-images.githubusercontent.com/89223545/214117543-3750777f-939e-40a6-853e-b100a588459d.png)
- Answer B
Incorrect. Choice III uses the default Point constructor to assign center a new Point with x and y both equal to 0. It attempts to update x and y, however since they are private instance variables in Point, they are not able to be accessed directly in Circle. This code will cause a compile time error.
- Answer C
Correct. Choice I uses the no parameter Point constructor to assign center a new Point with x and y both equal to 0, instead of x assigned the value a and y assigned the value b. Choice II correctly uses the two parameter Point constructor to create a new Point with x assigned the value a and y assigned the value b. Choice III uses the no parameter Point constructor to assign center a new Point with x and y both equal to 0. It attempts to update x and y, however since they are private instance variables in Point, they are not able to be accessed directly in Circle. This code will cause a compile time error.
- There is a compiling error that comes out of the answer in option D due to the way in which the constructor assigns a new point.




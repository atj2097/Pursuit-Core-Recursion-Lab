
# Recursion Exercises

- ### Sum of all from 1 to n

Write a function that takes in a number as input and recursively finds the sum of all numbers up to and including that number.

```js
input: 6
output: 21

func addRecur(at start: Int , to goal: Int) {
if goal < start {
return
}
print(start)
addRecur(at: start + 1, to: goal )
}
addRecur(at: 6, to: 21)
addRecur(start: 0, goal: 10)
21 = 6 + 5 + 4 + 3 + 2 + 1
```


- ### Multiply array

Write a function called `multArr` that takes in an array of numbers as an argument and recursively multiplies together all of the values in the array.

```js
func multArr(mult arr: [Int]) -> Int {
//   var array = arr
if arr.count == 1 {
return arr[0]
}
var zero = arr[0]
print(zero)
var remainingElements = Array(arr[1...])

print(remainingElements)
return zero * multArr(mult: remainingElements)
}
//multArr(mult: [5,5,1,2])

multArr([2, 3, 5]); // returns 30
multArr([5, 5, 1, 2]); //returns 50
```

- ### Concatenate array

Write a function called `concatArr` that takes in an array of strings as an argument and recursively concatenates the strings together into a single string, with spaces between each original string.
func concatArr(goal sentence: [String]) -> String {
if sentence.count == 1 {
return sentence[0]
}
var zero = sentence[0]
print(zero)
var remainingElements = Array(sentence[1...])
print(remainingElements)
return zero + concatArr(goal: remainingElements)
}
concatArr(goal: ["is ", "it ", "tomorrow"])
//
```js
func concatArr(goal sentence: [String]) -> String {
if sentence.count == 1 {
return sentence[0]
}
var zero = sentence[0]
print(zero)
var remainingElements = Array(sentence[1...])
print(remainingElements)
return zero + concatArr(goal: remainingElements)
}
concatArr(goal: ["is ", "it ", "tomorrow"])
concatArr(['is', 'it', 'tomorrow']); // returns 'is it tomorrow'
concatArr(['or', 'just', 'the', 'end', 'of', 'time']); //returns 'or just the end of time'
```
//
- ### Sum evens

Write a function called `sumEvens` that takes in an array of numbers as an argument and recursively sums only the even numbers in the array.

```js
func sumEvens(sum arr: [Int]) -> Int {

if arr.count <= 0 {
return 0
}
var zero = arr[0]
if arr[0] % 2 == 0 {
return arr[0] + sumEvens(sum: Array(arr.dropFirst()))
}
else {
return sumEvens(sum: Array(arr.dropFirst()))
}
}

sumEvens(sum: [2, 3, 5, 6])
sumEvens([2, 3, 5, 6]); // returns 8
sumEvens([10, 5, 1, 2, 12]); //returns 24
```

- ### Recursive range

Write a function called `range` which takes in two numbers (num1, num2) as arguments. The function should return an array of numbers between num1 and num2.

```js
//range(2,10); // returns [2, 3, 4, 5, 6,7, 8, 9, 10]
//range(17,20); // returns [17, 18, 19, 20]

func rang(num1 numberOne: Int , num2 numberTwo: Int) -> [Int] {
var array = [Int]()
if numberOne > numberTwo { return array }
array.append(numberOne)
return array + rang(num1: numberOne + 1, num2: numberTwo)
}
print(rang(num1: 2, num2: 10))
//```)
//
//
- ### Triple Step

A child is running up a staircase with n steps and can hop either 1 step 2 steps or 3 steps at a time. Write a function called 'tripleStep', that takes in an argument `n` that represents the number of steps in the staircase, and returns a count of how many possible ways the child can run up the stairs.

```js
func tripleStep( n: Int) -> Int {
if n == 0 {
return 1
}
if n < 0 {
return 0
}
return tripleStep(n: n-1) + tripleStep(n: n-2) + tripleStep(n: n-3)

}
print(tripleStep(n: 10))
tripleStep(n: 3); //returns 4
tripleStep(n: 4); //returns 7
tripleStep(n: 5); //returns 13
tripleStep(n: 10); //returns 274
//```
//
//Source: Cracking the Coding Interview
//
- ### Coin Combos

Given an infinite number of quarters, dimes, nickels, and pennies, write code to calculate the number of possible ways of giving exact change for `n` cents.

In other words, write a function called `coinCombos` that takes in one argument: `n`, which represents the total amount of money (in cents) that you need to make change for. Your function should return the amount of possible combinations you can make to return that exact amount of change.

//For example:
//```js
//coinCombos(5); //returns 2
//coinCombos(10); //returns 4
//coinCombos(25); //returns 13
//coinCombos(60); //returns 73
//```
//
//Source: CTCI
//
//# Resources
//- [JavaScript Recursion Exercises](http://www.w3resource.com/javascript-exercises/javascript-recursion-functions-exercises.php)
//- [Swift Recursion Exercises](https://www.weheartswift.com/recursion/)

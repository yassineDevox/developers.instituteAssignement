# Asignements
* [The logic behind a for loop](#explain-for-loop)
* [JavaScript Functions - 3-hour Lesson Outline](#javaScript-functions-3-hours-lesson-outline)

# Explain For Loop 
In this document, we will discuss how to explain the logic behind a for loop to students. We will consider what demonstrations and images could be used to make the concept more accessible and engaging.

## Demonstration
To demonstrate the concept of a for loop, we can use a simple real-life example. Imagine a teacher who wants to call out the names of each student in a class to check attendance. The teacher goes through the list of students one by one, starting from the first student until the last one is called. This repetitive action can be compared to a for loop in programming, where a set of instructions are executed for a specific number of iterations.

Using this analogy, we can explain the given code snippet:

```javascript
for (let i = 0; i < 4; i++) {
  console.log("the current number is " + i);
}
```
## Details
The for loop acts like the teacher calling out student names. 
The loop starts with `i = 0` and continues until `i < 4`, increasing the value of `i by 1 (i++)` after each iteration. 
The code inside the loop, `console.log("the current number is " + i)`, is executed for each iteration, printing the current value of i.

## FlowChart 
![flowChartLoop.png ](https://github.com/yassineDevox/developers.instituteAssignement/raw/main/flowChartLoop.png)


# JavaScript Functions 3 hours Lesson Outline
## Functions in JavaScript
### Theory
A function is a block of code that can be called and executed multiple times throughout a program. It helps to make code more modular and reusable. The syntax for creating a function in JavaScript is:
```javascript
function name(parameter1, parameter2, ... parameterN) {
 // body
}
```

+ `functionName`: the name of the function.
+ `parameters`: variables that are passed into the function when it's called.
+ `function body` : the code that executes when the function is called.
+ `return`: the value that the function outputs when it's called.

To call a function, use its name followed by parentheses with the required arguments (if any).
```javascript
functionName(arguments);
```
+ `Parameters and arguments` are often used interchangeably, but they are slightly different. Parameters are variables declared in the function definition, whereas arguments are the actual values passed into the function when it's called.

+ `The return keyword` is used to output a value from a function. When the function is called, the return value is passed back to the line of code that called the function.

+ `Default parameters` allow you to set default values for parameters in case they are not passed in. This can make your code more concise and easier to read.

+ `Scope` refers to the accessibility of variables within a program. Variables declared inside a function are only accessible within that function (local scope), whereas variables declared outside of a function can be accessed from anywhere in the program (global scope).


### Practice
#### Function Declaration
```javascript 
function greet(name) {
  console.log(`Hello, ${name}!`);
}

greet("John"); // Output: "Hello, John!"
```
#### Anonymous Function
You can also create anonymous functions, which can be used as arguments or assigned to variables:
```javascript 
const square = function(number) {
  return number * number;
};

console.log(square(5)); // Output: 25
```
#### Arrow Function
A more concise syntax for defining functions is the arrow function:

```javascript 
const square = number => {
  return number * number;
};

console.log(square(3)); // Output: 9
```
#### Parameters and Arguments
```javascript
function addNumbers(num1, num2) {
  return num1 + num2;
}

const result = addNumbers(3, 5);
console.log(result); // Output: 8

```
#### Return keyword
```javascript
function double(number) {
  return number * 2;
}

const result = double(5);
console.log(result); // Output: 10
```
#### Default Parameters
```javascript
function greet(name = "stranger") {
  console.log(`Hello, ${name}!`);
}

greet(); // Output: "Hello, stranger!"
greet("John"); // Output: "Hello, John!"

```
#### Variables Scope
```javascript 
const globalVariable = "I am global";

function printVariables() {
  const localVariable = "I am local";
  console.log(globalVariable); // Output: "I am global"
  console.log(localVariable); // Output: "I am local"
}

printVariables();
console.log(globalVariable); // Output: "I am global"
console.log(localVariable); // Output: Uncaught ReferenceError: localVariable is not defined

```
### Exercises
1. Write a function called sum that takes two numbers as parameters and returns their sum.
```javascript
function sum(a, b) {
  return a + b;
}

console.log(sum(3, 4)); // Output: 7

```
2. Write a function called double that takes a number as a parameter and returns its double.
```javascript
function double(number) {
  return number * 2;
}

console.log(double(5)); // Output: 10
```
3. Write a function called isAdult that takes a number as a parameter and returns true if the number is 18 or higher, and false otherwise.
```javascript 
function isAdult(age) {
  if (age >= 18) {
    return true;
  } else {
    return false;
  }
}

console.log(isAdult(20)); // Output: true
console.log(isAdult(16)); // Output: false

```
4. Create a function called getGrade that takes a number as a parameter and returns a letter grade based on the following conditions:
+ If the number is 90 or higher, return 'A'.
+ If the number is between 80 and 89 (inclusive), return 'B'.
+ If the number is between 70 and 79 (inclusive), return 'C'.
+ If the number is between 60 and 69 (inclusive), return 'D'.
+ If the number is below 60, return 'F'.
```javascript
function getGrade(score) {
  if (score >= 90) {
    return 'A';
  } else if (score >= 80 && score <= 89) {
    return 'B';
  } else if (score >= 70 && score <= 79) {
    return 'C';
  } else if (score >= 60 && score <= 69) {
    return 'D';
  } else {
    return 'F';
  }
}

console.log(getGrade(95)); // Output: A
console.log(getGrade(85)); // Output: B
console.log(getGrade(75)); // Output: C
console.log(getGrade(65)); // Output: D
console.log(getGrade(55)); // Output: F

```
5. Write a function called formatName that takes a first name and a last name as parameters and returns a formatted full name string. If no last name is provided, the function should use the default value of an empty string.

```javascript
function formatName(firstName, lastName = "") {
  if (lastName) {
    return `${firstName} ${lastName}`;
  } else {
    return firstName;
  }
}

console.log(formatName("John", "Doe")); // Output: John Doe
console.log(formatName("Jane")); // Output: Jane

```
6. Create a function called multiplyNumbers that takes two numbers as parameters and returns their product. If only one number is provided, the function should use the default value of 1 for the second number.

```javascript
function multiplyNumbers(number1, number2 = 1) {
  return number1 * number2;
}

console.log(multiplyNumbers(2, 3)); // Output: 6
console.log(multiplyNumbers(4)); // Output: 4

```
7. Write a function called printName that prints the value of a variable called name that is declared outside of the function.
```javascript
const name = "John";

function printName() {
  console.log(name);
}

printName(); // Output: John
```
8. What will be the output of the above code snippet?

```javascript
let count = 0;

function incrementCount() {
  let count = 1;
  count++;
  console.log(count);
}

incrementCount();
console.log(count);

```

The function incrementCount() declares a new variable called count within the function scope, which shadows the count variable declared in the outer scope. The output of the function is 2, because count is incremented from 1 to 2. The output of the last line is 0, because it prints the value of the count variable in the outer scope, which was not affected by the function.
```javascript
incrementCount(); // Output: 2
console.log(count); // Output: 0
```
## Authors
- [@yassineDevox](https://www.github.com/yasssineDevox)

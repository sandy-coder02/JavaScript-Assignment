# Assignment-1 :

**In programming**, loops are used to repeat a block of code.
For example , If you want to show a message 100 times, then you can use a loop.

## JavaScript - `for` loop

The **syntax**
 of the for
  loop is : 

```javascript
for( initial expression;  condition ; update expression){
	
   _// code block to be executed_

}
```




- The `Initial expression`  declares and initializes the variable and executes only once.
- The `condition` is evaluated
If the condition is True , the block of code inside the for loop is executed
If the condition is False, the for loop is terminated
- The `update expression` updates the value of the initial expression when the condition is True.
The condition is evaluated again, This process continues until the condition is False.


## Flowchart of JavaScript `for` loop


![ ](https://static.javatpoint.com/cpages/images/forloop.png)









Example 1 : Display a text five times

``` javascript
for(let i = 0; i <= 4; i++){
	console.log(“ Hello world”)
    }
```

Output: 
     Hello world
     Hello world
     Hello world
     Hello world
     Hello world


|Iteration|Variable|Condition: i<=4| Action|
|---|---|---|---|
| 1st |i = 0|True|Hello world is printed, i is incremented to 1|
|2nd|i = 1|True|Hello world is printed, i is incremented to 2|
|3rd|i = 2| True|Hello world is printed,i is incremented to 3|
|4th|i = 3|True|Hello world is printed,i is incremented to 4|
|5th|i = 4|True|Hello world is printed, i is incremented to 5|
|6th|i = 5|False|The loop is terminated|
|



**Example 2** :  Program to display a sum of N natural numbers
 ```Javascript
var sum = 0 ;
var N = 10 ;

for (var i = 0; i<N; i++) {
  sum = sum +  i;
}
console.log(sum) ; 
```
Output : 45

## Exercise to Practice: 
1.Write a program to display a sequence of numbers.

   2.Write a program to find the even numbers between 4 and 20.


*********************










# Assignment -2 :

## Functions 
A function is a block of code to perform a specific task.
It helps to divide   a complex program into smaller chunks and makes your program easy to understand and reusable.


## Function Declaration :
To create a function we use function declaration.

**Example 1** : Display a text
```Javascript
// declaring a function
function greet(){
	console.log(“Good Morning”);
}
// calling the function 
greet();
```
Output : 
Good Morning



**Syntax**:
```javascript
function   nameOfFunction( parameter1, parameter2,..){
	// code to be executed
}
```
![](https://s3.ap-south-1.amazonaws.com/s3.studytonight.com/tutorials/uploads/pictures/1587882057-1.png)
## Explanation: 
A JavaScript function is defined with the keyword function  , followed by a name, followed by parenthesis ()
Function name follows the rule of variable name.
The code to be executed by the function, inside the curly brackets,{ }.

**Function parameters** are listed inside the parentheses ( ) in the function definition
**Function arguments** are the values received by the function when it is called or invoked.

**Example 2** : Function with Parameters 


```javascript
// declaring a function
function greet ( name ){
	console.log(“Good Morning ”,  name );
}

let name = prompt(“Enter a name :”);

// calling the function 
greet(name);
```
Output : 
Enter a name : Rahul
Good Morning Rahul



## Difference between parameters and arguments :

- **Function parameters** are the names listed in the function’s definition .
- **Function arguments** are the real values passed to the function.
Parameters are initialized to the values of the arguments supplied.

For instance: 
```javascript
function area(width, height) {
  return width * height;
}

console.log(area(5, 6));
```
Output: 30

## Default parameters
Default function parameters allow named parameters to be initialized with default values if no value or undefined is passed.

For example : 
```javascript
// define a function
function  multiply( x, y =1) {
	return x * y ;        // return statement
}

// calling a function (function invocation)
console.log(multiply (5,2));

console.log(multiply (5));
```

Output: 
10
5


## Function return statement:
Function often computes return value, it is returned back to the caller.
A function immediately stops at the point where return is called.

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSGCDSlRl8wzGbuTwDLngAx5p3KBRPvTNoyVA&usqp=CAU)

**Example 3** : Program to calculate the product of two  numbers and return a result.
```javascript
// define a function
function  multiply( x, y) {
	return x * y ;        // return statement
}

// calling a function (function invocation)
product =  multiply (2,6) ;

console.log(“ Product :” , product);

```

## Scope
The **scope** is the current context of execution in which values and expressions are "visible" or can be referenced. If a variable or expression is not in the current scope, it will not be available for use. Scopes can also be layered in a hierarchy, so that child scopes have access to parent scopes, but not vice versa.

## Types of scopes :
- **Global scope**: The default scope for all code running in script mode.
- **Module scope**: The scope for code running in module mode.
- **Function scope**: The scope created with a function.
- **Block scope**: The scope created with a pair of curly braces { }.
  
A function creates a scope, so that (for example) a variable defined exclusively within the function cannot be accessed from outside the function or within other functions. 

For instance, the following is invalid:
```javascript
function greet() {
  const x = "Good Morning";       // declared inside a function  

  console.log("Hello");
  console.log(x);
}
console.log(x);           // Causes error
 ```
However, the following code is valid due to the variable being declared outside the function, making it global:
```javascript
const x = "good morning";       // declared outside a function

function greet() {
  console.log("Hello");
  console.log(x);
}
greet();
```
 
Blocks only scope let and const declarations, but not var declarations.
```javascript
{
  var x = 1;
}
console.log(x);              // 1
 
{
  const x = 1;
}
console.log(x);               // ReferenceError: x is not defined
```


## Local Variable vs Global Variable
**Local variable** declared inside the function. It can only be accessed from within the function.

**Global variable** declared outside a function. It can be accessed by any function.

**Example :  Global variable**
```javascript

let a = “hello” ;

function greet() {
	console.log(a);
}

greet();
```

**Example : Local variable**
```javascript

let a = “hello” ;

function greet() {
	let  b = “World”;
	console.log(a + b);
}

greet();
console.log( a+ b);  // ERROR
```
Output: 

helloWorld

Uncaught ReferenceError : b is not defined



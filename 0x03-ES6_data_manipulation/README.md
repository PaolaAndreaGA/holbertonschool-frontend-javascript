## Why Use Arrays?

If you have a list of items (a list of car names, for example), storing the cars in single variables could look like this:

let  car1 =  "Saab";  
let  car2 =  "Volvo";  
let  car3 =  "BMW";

However, what if you want to loop through the cars and find a specific one? And what if you had not 3 cars, but 300?

The solution is an array!

An array can hold many values under a single name, and you can access the values by referring to an index number.

----------

## Creating an Array

Using an array literal is the easiest way to create a JavaScript Array.

Syntax:

const  _array_name_  = [_item1_,  _item2_, ...];  

It is a common practice to declare arrays with the  const  keyword.

Learn more about  const  with arrays in the chapter:  [JS Array Const](https://www.w3schools.com/js/js_array_const.asp).

### Example

const  cars = ["Saab",  "Volvo",  "BMW"];

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array)

Spaces and line breaks are not important. A declaration can span multiple lines:

### Example

const  cars = [  
"Saab",  
"Volvo",  
"BMW"  
];

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_newlines)

You can also create an array, and then provide the elements:

### Example

const  cars = [];  
cars[0]=  "Saab";  
cars[1]=  "Volvo";  
cars[2]=  "BMW";  

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_add_elements)

----------

## Using the JavaScript Keyword new

The following example also creates an Array, and assigns values to it:

### Example

const  cars =  new  Array("Saab",  "Volvo",  "BMW");

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_new)

The two examples above do exactly the same.

There is no need to use  `new Array()`.

For simplicity, readability and execution speed, use the array literal method.

----------

ADVERTISEMENT

----------

## Accessing Array Elements

You access an array element by referring to the  **index number**:

const  cars = ["Saab",  "Volvo",  "BMW"];  
let  car = cars[0];

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_element)

**Note:**  Array indexes start with 0.

[0] is the first element. [1] is the second element.

----------

## Changing an Array Element

This statement changes the value of the first element in  `cars`:

cars[0] =  "Opel";

### Example

const  cars = ["Saab",  "Volvo",  "BMW"];  
cars[0] =  "Opel";

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_element_change)

----------

## Access the Full Array

With JavaScript, the full array can be accessed by referring to the array name:

### Example

const  cars = ["Saab",  "Volvo",  "BMW"];  
document.getElementById("demo").innerHTML  = cars;

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_full)

----------

## Arrays are Objects

Arrays are a special type of objects. The  `typeof`  operator in JavaScript returns "object" for arrays.

But, JavaScript arrays are best described as arrays.

Arrays use  **numbers**  to access its "elements". In this example,  `person[0]`  returns John:

### Array:

const  person = ["John",  "Doe",  46];

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_array)

Objects use  **names**  to access its "members". In this example,  `person.firstName`  returns John:

### Object:

const  person = {firstName:"John", lastName:"Doe", age:46};

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_object)

----------

## Array Elements Can Be Objects

JavaScript variables can be objects. Arrays are special kinds of objects.

Because of this, you can have variables of different types in the same Array.

You can have objects in an Array. You can have functions in an Array. You can have arrays in an Array:

myArray[0] = Date.now;  
myArray[1] = myFunction;  
myArray[2] = myCars;

----------

## Array Properties and Methods

The real strength of JavaScript arrays are the built-in array properties and methods:

cars.length // Returns the number of elements  
cars.sort() // Sorts the array

Array methods are covered in the next chapters.

----------

## The length Property

The  `length`  property of an array returns the length of an array (the number of array elements).

### Example

const  fruits = ["Banana",  "Orange",  "Apple",  "Mango"];  
let  length = fruits.length;

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_length)

The  `length`  property is always one more than the highest array index.

----------

## Accessing the First Array Element

### Example

const  fruits = ["Banana",  "Orange",  "Apple",  "Mango"];  
let  fruit = fruits[0];

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_first)

----------

## Accessing the Last Array Element

### Example

const  fruits = ["Banana",  "Orange",  "Apple",  "Mango"];  
let  fruit = fruits[fruits.length  -  1];

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_last)

----------

## Looping Array Elements

One way to loop through an array, is using a  `for`  loop:

### Example

const  fruits = ["Banana",  "Orange",  "Apple",  "Mango"];  
let  fLen = fruits.length;  
  
let  text =  "<ul>";  
for  (let  i =  0; i < fLen; i++) {  
text +=  "<li>"  + fruits[i] +  "</li>";  
}  
text  +=  "</ul>";

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_loop)

You can also use the  `Array.forEach()`  function:

### Example

const  fruits = ["Banana",  "Orange",  "Apple",  "Mango"];  
  
let  text =  "<ul>";  
fruits.forEach(myFunction);  
text +=  "</ul>";  
  
function  myFunction(value) {  
text +=  "<li>"  + value +  "</li>";  
}

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_loop_foreach)

----------

## Adding Array Elements

The easiest way to add a new element to an array is using the  `push()`  method:

### Example

const  fruits = ["Banana",  "Orange",  "Apple"];  
fruits.push("Lemon"); // Adds a new element (Lemon) to fruits

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_add_push)

New element can also be added to an array using the  `length`  property:

### Example

const  fruits = ["Banana",  "Orange",  "Apple"];  
fruits[fruits.length] =  "Lemon"; // Adds "Lemon" to fruits

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_add)

**WARNING !**  

Adding elements with high indexes can create undefined "holes" in an array:

### Example

const  fruits = ["Banana",  "Orange",  "Apple"];  
fruits[6] =  "Lemon"; // Creates undefined "holes" in fruits

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_holes)

----------

## Associative Arrays

Many programming languages support arrays with named indexes.

Arrays with named indexes are called associative arrays (or hashes).

JavaScript does  **not**  support arrays with named indexes.

In JavaScript,  **arrays**  always use  **numbered indexes**.

### Example

const  person = [];  
person[0] =  "John";  
person[1] =  "Doe";  
person[2] =  46;  
person.length; // Will return 3  
person[0]; // Will return "John"

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_associative_1)

**WARNING !!**  
If you use named indexes, JavaScript will redefine the array to an object.

After that, some array methods and properties will produce  **incorrect results**.

### Example:

const  person = [];  
person["firstName"] =  "John";  
person["lastName"] =  "Doe";  
person["age"] =  46;  
person.length; // Will return 0  
person[0]; // Will return undefined

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_associative_2)

----------

## The Difference Between Arrays and Objects

In JavaScript,  **arrays**  use  **numbered indexes**.

In JavaScript,  **objects**  use  **named indexes**.

Arrays are a special kind of objects, with numbered indexes.

----------

## When to Use Arrays. When to use Objects.

-   JavaScript does not support associative arrays.
-   You should use  **objects**  when you want the element names to be  **strings (text)**.
-   You should use  **arrays**  when you want the element names to be  **numbers**.

----------

## JavaScript new Array()

JavaScript has a built in array constructor  `new Array()`.

But you can safely use  `[]`  instead.

These two different statements both create a new empty array named points:

const  points =  new  Array();  
const  points = [];

These two different statements both create a new array containing 6 numbers:

const  points =  new  Array(40,  100,  1,  5,  25,  10);  
const  points = [40,  100,  1,  5,  25,  10];

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_literal)

The  `new`  keyword can produce some unexpected results:

// Create an array with three elements:  
const  points =  new  Array(40,  100,  1);

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_new_array_three)

// Create an array with two elements:  
const  points =  new  Array(40,  100);

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_new_array_two)

// Create an array with one element ???  
const  points =  new  Array(40);

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_new_error)

### A Common Error

const  points = [40];

is not the same as:

const  points =  new  Array(40);

// Create an array with one element:  
const  points = [40];

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_one)

// Create an array with 40 undefined elements:  
const  points =  new  Array(40);

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_new_error2)

----------

## How to Recognize an Array

A common question is: How do I know if a variable is an array?

The problem is that the JavaScript operator  `typeof`  returns "`object`":

const  fruits = ["Banana",  "Orange",  "Apple"];  
let  type =  typeof  fruits;

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_typeof)

The typeof operator returns object because a JavaScript array is an object.

### Solution 1:

To solve this problem ECMAScript 5 (JavaScript 2009) defined a new method  `Array.isArray()`:

Array.isArray(fruits);

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_isarray_method)

### Solution 2:

The  `instanceof`  operator returns true if an object is created by a given constructor:

const  fruits = ["Banana",  "Orange",  "Apple"];  
  
fruits  instanceof  Array;

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_instanceof)

## Complete Array Reference

For a complete Array reference, go to our:

[Complete JavaScript Array Reference](https://www.w3schools.com/jsref/jsref_obj_array.asp).

The reference contains descriptions and examples of all Array properties and methods.

## Test Yourself With Exercises

## Exercise:

Get the value "`Volvo`" from the  `cars`  array.

const cars = ["Saab", "Volvo", "BMW"];
let x = ;
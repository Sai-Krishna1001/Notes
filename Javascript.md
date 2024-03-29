# JavaScript Joyride 🚀✨

### Welcome to the JavaScript Joyride! 🏎️🌍 In this repository, you're about to embark on a thrilling journey through the fascinating world of JavaScript, where learning meets fun. 🌟🚀📚

## Introduction

JavaScript is not just a programming language; it's an exhilarating adventure that allows you to unlock the secrets of the digital universe. Whether you're a beginner or an experienced developer, hop on board for an unforgettable joyride through the realms of JavaScript. 🎢💡

Let's get started on this exciting journey!


## What is a Scripting Language?

A scripting language is a type of high-level programming language designed with ease of use and automation in mind. These languages offer a syntax that closely resembles natural language and provide powerful abstractions for handling intricate data structures and operations.

## JavaScript: More Than Just a Language

JavaScript stands out as a versatile high-level scripting language. It excels at simplifying complex tasks and automating repetitive jobs. Here's why:

- **Natural Language Syntax**: JavaScript's syntax is so approachable that it feels like conversing in plain English.

- **Automation**: It's built to automate frequently repeated tasks, saving you time and effort.

- **Data Handling**: With JavaScript, working with complex data structures becomes a breeze.

- **Simplicity**: It simplifies complex operations, making them more manageable.

- **Versatility**: JavaScript is your one-stop solution for scripting needs.

Embrace JavaScript for its power in simplifying the seemingly complex and automating your tasks. 🤖💡


-->JavaScript supports two types of objects: built-in objects and host objects.
-->The return type of typeof for standard JavaScript objects is "object".
--> prompt() method displays a dialog box that prompts the visitor for input.
-->The definition of an undefined value in JavaScript is that a variable is declared but not assigned to any value. When you try to access such a variable, JavaScript returns undefined. 

-->A function with no return value implicitly returns undefined.

-->When converting a string to a number, the engine first trims leading and trailing whitespace, \n, \t characters, returning NaN if the trimmed string does not represent a valid number. If string is empty, it returns 0.

-->null and undefined are handled differently: null becomes 0, whereas undefined becomes NaN.

-->Logical operators such as || and && do boolean conversions internally, but actually return the value of original operands, even if they are not boolean.

-->Any value that is not in the list is converted to true, including object, function, Array, Date, user-defined type, and so on. Symbols are truthy values. Empty object and arrays are truthy values as well:
Boolean('')           // false
Boolean(0)            // false     
Boolean(-0)           // false
Boolean(NaN)          // false
Boolean(null)         // false
Boolean(undefined)    // false
Boolean(false)        // false

-->When applying == to null or undefined, numeric conversion does not happen. null equals only to null or undefined, and does not equal to anything else.
null == 0               // false, null is not converted to 0
null == null            // true
undefined == undefined  // true
null == undefined       // true

-->NaN does not equal to anything even itself:
if (NaN !== NaN) { console.log("we're dealing with NaN here") }

--->tricky results
====================================================
true + false             // 1
12 / "6"                 // 2
"number" + 15 + 3        // 'number153'
15 + 3 + "number"        // '18number'
[1] > null               // true
"foo" + + "bar"          // 'fooNaN'
'true' == true           // false
false == 'false'         // false
null == ''               // false
!!"false" == !!"true"    // true
['x'] == 'x'             // true 
[] + null + 1            // 'null1'
[1,2,3] == [1,2,3]       // false
{}+[]+{}+[1]             // '0[object Object]1'
!+[]+[]+![]              // 'truefalse'
new Date(0) - 0          // 0
new Date(0) + 0          // 'Thu Jan 01 1970 02:00:00(EET)0'

-->Thread Vs Process
====================
Process
===========
--> It is a heavy weight process
--> It requires more resources
--> The program under execution is called a process
--> Processes run independent and don't share memory
--> The OS treats all different processes separately

Thread
==========
--> It is a light weight process that execute within a process
--> It requires less resources
--> Threads share memory with its peer threads
--> A process can contain single or multiple threads

-->Asynchronous Vs Synchronous
==================================
Synchronous
==============
--> Synchronicity in programming happens when the execution of operations is done sequentially
--> An Operation will only be executed after the previous one is done
--> Synchronous tasks are done in a single Thread. eg:preparing a meal alone

Asynchronous
===============
--> Asynchronous processing is done in parallel.
--> Tasks are not dependent on others and can be executed at the same time as a main operation(process).
--> Each Asynchronous tasks is done in a different thread that reports back to the main thread with the result when complete.
--> All the tasks in Asynchronous report back the result when they are done.


-->JavaScript is primarily an asynchronous programming language. However, it also supports synchronous execution when needed.

--> "Prototype Chaining" is used to build new types of objects based on existing ones. It is similar to inheritance in a class based language.

-->In JavaScript, call, apply, and bind are methods that can be used to manipulate the "this" value and invoke functions in different ways.

=====================================================================================
JSON
=============

-->JSON (JavaScript Object Notation) is a lightweight data interchange format commonly used for representing structured data. It is widely supported and used in web development and APIs due to its simplicity and readability.Here are some common operations related to JSON:

1. JSON Syntax:

-->JSON uses a simple and intuitive syntax to represent data in key-value pairs.
-->Properties are enclosed in double quotes: "key": value.
-->Data types supported include strings, numbers, booleans, objects, arrays, and null.

2. Converting to/from JSON:

-->JSON.stringify(): Converts a JavaScript object or value to a JSON string.
-->JSON.parse(): Parses a JSON string and converts it into a JavaScript object or value.

3. Accessing JSON Data:

-->Once parsed into a JavaScript object, you can access JSON data using dot notation or square brackets.
-->Example: data.property or data["property"].

4. Modifying JSON Data:

-->You can modify JSON data by directly assigning new values to properties or adding new properties to the object.
-->Example: data.property = newValue or data.newProperty = value.

5. JSON Array Operations:

-->JSON arrays are ordered collections of values enclosed in square brackets [ ].
-->Accessing elements: array[index].
-->Adding elements: array.push(value).
-->Removing elements: array.splice(index, 1).

6. Validating JSON:

-->To ensure the validity of JSON data, you can use JSON validators or methods like JSON.parse() to check for syntax errors.

-->>JSON is widely used for data exchange between client and server applications, storing configuration settings, and representing structured data in various contexts. Its simplicity, human-readability, and wide support make it a popular choice for data serialization and interchange.
==========================================================================================
Serialization Vs Deserialization
===================================
Serialization and deserialization are processes used to convert data into a format that can be easily transmitted or stored and then reconstructed back into its original form. Here's an explanation of the difference between serialization and deserialization with real-time examples:

Serialization:
===============
Serialization is the process of converting data structures or objects into a format suitable for storage or transmission.
It involves converting complex data, such as objects or data structures, into a standardized format like JSON or XML.
Serialized data can be stored in a file, sent over a network, or saved in a database.
Real-time example: Let's say you have an application where users can create and save documents. When a user creates a document, the data needs to be serialized into a format like JSON or XML to be stored in a database. This allows the data to be easily retrieved and reconstructed later.

Deserialization:
=================
Deserialization is the process of reconstructing serialized data back into its original form.
It involves taking the serialized data and converting it back into the appropriate data structures or objects.
Real-time example: Continuing with the previous example, when a user wants to view a saved document, the serialized data stored in the database needs to be deserialized. The deserialization process reconstructs the data from its serialized form, allowing it to be displayed to the user in the original format.

In summary, serialization is the process of converting data into a format suitable for storage or transmission, while deserialization is the process of reconstructing serialized data back into its original form. These processes are commonly used in various scenarios, such as storing data, transmitting data over networks, or exchanging data between different systems or platforms.
==================================================================================================
Q.What is the difference between slice and splice?
--> Some of the major difference in a tabular form
"Slice" 						"Splice"
Doesn't modify the original
array(immutable) 					Modifies the original array(mutable)
Returns the subset of original array 	Returns the deleted elements as array
Used to pick the elements from array	Used to insert or delete elements to/from array


splice method in array
===========================
-->The splice() method in JavaScript is used to change the contents of an array by removing, replacing, or adding elements at a specified position. It modifies the original array and returns an array containing the removed elements (if any). The splice() method can be used with two or more arguments:

-->splice(startIndex, deleteCount): Removes deleteCount number of elements from the startIndex and returns an array of the removed elements.
-->splice(startIndex, deleteCount, item1, item2, ...): Removes deleteCount number of elements from the startIndex and replaces them with the specified items. It returns an array of the removed elements.

Q. What is the use of defer keyword?
--> The 'defer' keyword is used in HTML script tags to indicate that the script should be executed after the HTML document has been parsed, but before the 'DOMContentLoaded' event is fired. It allows the HTML parsing and rendering to continue without blocking the script execution.
-->usage: <script src = "script.js" defer></script>

Q.) What is the difference between == and === operators?

JavaScript provides both strict(===, !==) and type-converting(==, !=) equality comparison. The
strict operators take type of variable in consideration, while non-strict operators make type
correction/conversion based upon values of variables. The strict operators follow the below
conditions for different types,
i. Two strings are strictly equal when they have the same sequence of characters, same length,
and same characters in corresponding positions.
ii. Two numbers are strictly equal when they are numerically equal. i.e, Having the same
number value. There are two special cases in this,
a. NaN is not equal to anything, including NaN.
b. Positive and negative zeros are equal to one another.
iii. Two Boolean operands are strictly equal if both are true or both are false.
iv. Two objects are strictly equal if they refer to the same Object.
v. Null and Undefined types are not equal with ===, but equal with ==. i.e, null===undefined
--> false but null==undefined --> true
Some of the example which covers the above cases,
0 == false // true
0 === false // false
1 == "1" // true
1 === "1" // false
null == undefined // true
null === undefined // false
'0' == false // true
'0' === false // false
[]==[] or []===[] //false, refer different objects in memory
{}=={} or {}==={} //false, refer different objects in memory

-->"Destructuring" that allows to unpack values from arrays or objects, into individual variables.

-->"Spread operator" takes an iterable objects and expands it into individual elements.

Q. Why do we call javascript as dynamic language?
A. Javascript is a loosely typed or a dynamic language because variables in javascript are not directly associated with any particular value type, and any variable can be assigned/reassigned with values of all types.
eg: 	let age = 50; // age is number now
	age = 'old'; // age is a string now
	age = true; // age is a boolean now


-->Javascript Core Concepts
1. closures
2. prototypes and inheritance
3. Asynchronous Programming
4. Modules and Modules Bundlers
5. Arrow Functions
6. Generators
7. Promises
8. Proxy and Reflect
9. Error Handling
10. Web API's


Closures: A closure is a combination of a function and the lexical environment within which that function was declared. It allows a function to access variables from its outer (enclosing) scope even after the outer function has finished executing.

Prototypes and Inheritance: JavaScript uses prototypes for object inheritance. Each object has a prototype, which serves as a template for creating new objects. Prototypal inheritance allows objects to inherit properties and methods from their prototypes.

Asynchronous Programming: JavaScript supports asynchronous programming through features like callbacks, promises, and async/await. These mechanisms allow handling asynchronous tasks, such as making API requests, without blocking the execution of other code.

Modules and Module Bundlers: Modules provide a way to organize code into reusable and manageable units. JavaScript has built-in module support through the ES modules syntax. Module bundlers like webpack or Rollup allow bundling modules into a single file for use in the browser.

Arrow Functions: Arrow functions are a concise syntax for writing function expressions. They provide a shorter syntax compared to traditional function expressions and capture the surrounding lexical scope automatically.

Generators: Generators are special functions that can be paused and resumed. They allow writing functions that can return multiple values over time, providing a convenient way to iterate through a sequence of values.

Promises: Promises are a way to manage asynchronous operations in JavaScript. They represent a value that may be available in the future, either successfully resolved or rejected with an error. Promises simplify the handling of asynchronous code and enable chaining multiple asynchronous operations.

Proxy and Reflect: Proxy and Reflect are powerful features that allow intercepting and customizing fundamental operations on objects. Proxies enable creating custom behavior for object operations like property access, method invocation, and more. Reflect provides methods for performing common object operations in a more controlled and flexible way.

Error Handling: JavaScript provides mechanisms for handling and throwing errors. The try-catch statement allows catching and handling exceptions, preventing the program from crashing when an error occurs. Errors can also be thrown explicitly using the throw statement.

Web APIs: JavaScript has extensive support for interacting with web APIs, such as the DOM API for manipulating HTML elements, the Fetch API for making HTTP requests, the Web Storage API for client-side storage, and many others. These APIs enable building interactive web applications.

--------------------------------------------------------------------------------------------------------------------------
Function transformations in JavaScript refer to different ways to manipulate, compose, and work with functions. Some key function transformations include:

Function composition - Creating a new function by composing multiple functions, where the output of one function becomes the input of the next. For example: const compose = (f, g) => x => f(g(x));

Currying - Transforming a function that takes multiple arguments into a function that takes them one at a time. For example: const curried = f => x => y => f(x,y);

Memoization - Caching the results of function calls to avoid unnecessary repeated computation. Useful for recursive functions.

Higher-order functions - Functions that take other functions as arguments or return functions as output. Examples are map, filter, reduce.

Partial application - Creating a new function by fixing some number of arguments to a function. The remaining arguments stay unapplied.

Pipelines - Chaining function calls together by piping the output of one as input to the next, often using compose. For example: const pipeline = compose(f, g, h);

Function decorators - Enhancing or modifying a function by wrapping it with another function. Used in object-oriented programming.

Function generators - Functions that can generate and return other functions.

So in summary, function transformations allow manipulating functions in different ways like combining, caching, changing arguments, etc. This enables writing reusable, modular code and is a key part of functional programming style in JS.
--------------------------------------------------------------------------------------------------------------------
-->

---
layout: cover
theme: the-unnamed
title: Cover Page
class: center middle
background: https://images.unsplash.com/photo-1581090700227-1e8e8d5d4f5d?auto=format&fit=crop&w=1950&q=80
transition: slide-up
fonts:
  sans: 'Roboto, sans-serif'
  serif: 'Roboto, serif'
  mono: 'Roboto Mono, monospace'
  provider: 'google'
  download: 'true'
  "unocss":  
  - |
    body { font-size: 12px; }
    h1 { font-size: 40px; }
    h2 { font-size: 30px; }
    h3 { font-size: 30px; }
    h4, h5, h6 { font-size: 24px; }
    p { font-size: 18px; }
    li { font-size: 18px; }
---

# **JavaScript Class Summary**

### Highlights from second semester classes so far 

Presented by **[CIRCLE 14]**  
TINYUKA —2025

<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  Press Space for next page <carbon:arrow-right />
</div>

<div class="abs-br m-6 text-xl">
  <button @click="$slidev.nav.openInEditor" title="Open in Editor" class="slidev-icon-btn">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

---
title: Circle Members
---

# Circle Members <br>
- Ajayi Gloria Alaba
- David Aruna
- Dumbiri Elizabeth
- Falore Oluwaseyi Akin
- Ibinabo Abraham
- Jari Michael
- Mariam Lawal
- Oluwamuyiwa Sogbetun
- Osasenaga Edosa
- Rasheed Damilola Abiodun

---

# Table of Contents

<Toc text-sm minDepth="1" maxDepth="2" />

---

# Introduction to JavaScript

- JavaScript is a versatile programming language for web development.
- It runs in the browser and enables interactive features.
- Created by Brendan Eich in 1995.
- Evolved into modern frameworks like React, Vue, and Angular.

## Data Types in Javascript

JavaScript has several core data types, including:

- **Primitive Types**: Number, String, Boolean, Null, Undefined, Symbol
- **Reference Types**: Objects, Arrays, Functions

---
## id: number
---
# Number

**Number Types**

- **Integers**: Whole numbers without decimals
- **Floating-point numbers**: Numbers with decimals

```js
let integer = 35;
let float = 4.57;
```

**Special numeric values:** e.g. NaN and Infinity

- NaN (Not a number): Represents an invalid or unreliable numeric result.

```js
let result = "hello" * 2;
console.log(result); // NaN
```

---

- Infinity: we have the positive infinity that represents a value larger than any other number and negative infinity that represents a value lesser than any other number.

```js
let a = 1
let b = 0
console.log (a/b); // Infinity

let a = -1
let b = 0
console.log (a/b); // -Infinity
```
---

**Number operations**

Refers to ways you can manipulate and work with numbers. Below are the most common number operations in JavaScript using arithmetic operators like +, -, *, /, %

Note an **operator** is a received syntax consisting of punctuation or alphanumeric characters that carries out built in functionalities while **operands** are the values the operator works on

       operator
           |
       20  +  7
       |      |
       operands

```js
let a = 20;
let b = 7;

console.log(a + b); // 27
console.log(a - b); // 13
console.log(a * b); // 140
console.log(a / b); // 2.857142857142857
console.log(a % b); // 6
```

---

- Numeric separator (\_) : They are used to improve readability of large numbers in JavaScript.

```js
let largeNumber = 1_000_000_000; // equivalent to 1000000000
console.log (largeNumber); // Output: 1000000000
```

They don't affect the value of the number but are just there to make the number easier to read.

```js
let float = 3.141_59; // No impact on the value
console.log(float); // 3.14159
```

- Number.parseInt(): Converts a string into an integer by removing any decimal point. It reads from left to right until it hits something that isn’t a number and then stops.

```js
let x = Number.parseInt("100px"); // 100
let y = Number.parseInt("3.14"); // 3
let z = Number.parseInt("Hello 12"); // NaN (can't convert text/can’t read if it starts with text)
```

- Number.parseFloat (): reads the string and keeps the decimal part if it exists.

```js
let x = Number.parseFloat("100.50px"); // 100.5 (reads until it sees non-numeric)
let y = Number.parseFloat("3.14"); // 3.14
let z = Number.parseFloat("Hello 12"); // NaN (no valid number to start with)
```

---

- .toString(): This is a method you can use to turn a number into text (a string).

```js

let age = 25;
let ageText = age.toString();
console.log(ageText); // "25"
console.log(typeof ageText); // string
```
You use .toString() when you need to:

- Display numbers as text (like in a sentence or on a webpage).
- Format output, like showing "You have 5 new messages"
---

# Strings

A string is a sequence of characters used to represent text.

```js
let greeting = "Hello, world!";
```  
They can be defined using:

- "double quotes"  
- 'single quotes'  
- `backticks` (template literals)

---

**Creating Strings**


```js
let single = 'Hello';
let double = "World";
let backtick = `Hey there!`;
```

Use backticks for template literals i.e mixing quotes inside each other:

```js
let mix = `It's a nice day`;
```

**Escape Characters**

Use backslashes (\) for special characters inside strings.

```js
let quote = "He said, \"Hello!\"";
let newline = "First line\nSecond line";
```

- \n – new line  
- \t – tab  
- \\ – backslash

---

**Common String Methods**

```js
let text = "  JavaScript is fun!  ";
```

| Method                   | Description                |
| ------------------------ | -------------------------- |
| `text.length`            | Total characters           |
| `text.trim()`            | Removes whitespace         |
| `text.toLowerCase()`     | Converts to lowercase      |
| `text.toUpperCase()`     | Converts to uppercase      |
| `text.includes("fun")`   | Checks if "fun" exists     |
| `text.indexOf("Script")` | Finds position of "Script" |

---

```js
let str = "JavaScript";
```

| Method                        | Example                     | Result                   |
| ----------------------------- | --------------------------- | ------------------------ |
| `str.slice(0, 4)`             | Returns "Java"              | "Java"                   |
| `str.substring(4)`            | From position 4 onward      | "Script"                 |
| `str.replace("Java", "Type")` | Replaces "Java" with "Type" | "TypeScript"             |
| `str.repeat(2)`               | Repeats the string twice    | "JavaScriptJavaScript"   |

---

**Template Literals**(`) 

Allows:

- Variable interpolation  
- Multi-line strings

```js
let name = "Sam";
let mood = "excited";
let message = `Hi ${name}, you're looking ${mood} today!`;
```

Cleaner and more readable than string concatenation.

---

**String Immutability**

Strings in JavaScript are immutable

```js
let word = "hello";
word[0] = "H";  // This won't work
```

To "change" a string, create a new one:

```js
word = "H" + word.slice(1);  // "Hello"
```
---

# Object

Objects are data types used to store data in key-value pair. 
Each key also called a property maps to a value which can be of any type including a primitive, object or function.

```js
let person = {
    name: “Tayo”,
    age: 18,
    isFemale: true
}:
```

There are two ways to create an object

Using the `Object()` constructor: (Rarely used)

```js
let user = new Object();
user.name = "Tayo";
```
---

Using object literal syntax: This is commonly used
```js
let person = {
name: "Tayo"
};
```
In order to access the property of an object, we can use two methods

**Dot notation:** it’s commonly used to access object property
```js
console.log(person.name); // Tayo
```
Bracket notation: This is required if the key is dynamic or not a valid identifier.
```js
console.log(person["age"]); // 18
```

**Adding a property**

Adding a new key-value pair to an existing object can be done in two ways:
```js
// Dot notation (most common)
person.school = "AltSchool";

// Bracket notation (useful for dynamic keys)
person["takesStudent"] = false;
```
---

**Modifying a property**

To change the value of an existing key in an object

```js
const user = { name: "Maxwell" };

// Using dot notation
user.name = "Maxwell Emma";

// Using bracket notation
user["name"] = "Emma Maxwell";
```

**Deleting a Property**

Removing a key-value pair entirely from an object:

```js
// Using dot notation
delete person.takesStudent;

// Using bracket notation
delete person["school"];
```
---

**Nested Objects**

Objects can contain other objects or arrays, creating a structured hierarchy.

```js
let student = {
    name: "Albert",
    scores: {
    physics: 80,
    english: 90
    }
};

// Accessing a nested property
console.log(student.scores.english); // 90
```
---

**Objects with Methods**

A method is simply a function defined as a property of an object. This allows the object to perform actions.

```js 
let person = {
    name: "David",
    greet: function() {
        return "Hello, " + this.name;
    }
};

console.log(person.greet()); // Hello, David
```

Here, the this keyword refers to the person object allowing the method to access the object's properties.

```js
let profile = {
    username: "Ozeni",
    show() {
        console.log(`Hi, I'm ${this.username}`);
    }
};

profile.show(); // Hi, I'm Ozeni
```
---

# Loop

A loop repeatedly executes a block of code as long as a condition is true. It’s useful for automating repetitive tasks.
Single execution of the loop body is called an iteration 

**Types of Loops**

- While loop

This execute condition before code. Any condition or variable can be a loop condition, if ++ is missing then the loop repeat. It's mostly used when the number of iterations isn’t known beforehand.

```js
let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}
```
---

- Do while loop

This is similar to while loop but code run at least once before the loop start. Meaning it execute code before checking conditions.  Condition check is just moved below the loop body.

```js

let i = 0;
do {
  console.log(i);
  i++;
} while (i < 5);

```
- For loop

This is more complex but it’s the most commonly used loop, this is best used when you know how many times to run the loop. Exit can be force anytime. 

```js

for (let i = 0; i < 5; i++) {
  console.log(i);
}
```
---

- For...of loop

It’s used to loop over iterable properties of an object, value of an iterable object can be counted e.g array, string.

```js
let colors = ["red", "blue", "green"];
for (let color of colors) {
  console.log(color);
}

```
Note: The for...of loop cannot be used directly on regular objects unless they are converted to an iterable form, like using 
```js 
Object.values()

```

---

# Functions 

Functions are reusable blocks of code designed to perform specific tasks. A function can accept inputs (parameters), perform operations and return an output.

**Function Declaration**

Functions are declared using the `function` keyword. They can take parameters and return values.

```js
function greet(name) {
  return `Hello, ${name}!`;
}
console.log(greet('Alice'));
```

**Output:**  
Hello, Alice!

---

**Basic Functions**

Functions allow for reusable logic, like this simple addition example.

```js
function add(a, b) {
  return a + b;
}
console.log(add(2, 3));
```

**Output:**  
5

**Arrow Functions**

They are a concise way to write functions. 

```js
const multiply = (a, b) => a * b;
console.log(multiply(4, 5));
```

**Output:**  
20

---

**Default Parameters**

You can define default values for parameters, which are used if no argument is provided.

```js
function bookRoom(roomType = 'Standard') {
  return `Room booked: ${roomType}`;
}
console.log(bookRoom());
```

**Output:**  
Room booked: Standard

**Optional Chaining**

Allows safe access to nested object properties without causing errors.

```js
const user = { profile: { name: 'Bob' } };
console.log(user?.profile?.name);
console.log(user?.contact?.email);
```

**Output:**  
Bob  
undefined

---

**Asynchronous Functions**

`async` and `await` simplify asynchronous operations and make them easier to read.

```js
async function fetchData() {
  const response = await fetch('https://api.example.com/data');
  const data = await response.json();
  console.log(data);
}
fetchData();
```

**Callback Pattern**

Before async/await, callbacks were used to handle asynchronous code.

```js
function getUserData(callback) {
  setTimeout(() => {
    callback({ name: 'Jane' });
  }, 1000);
}
getUserData(user => console.log(user.name));
```

**Output:**  
Jane (after 1 second)

---

**Closures**

Closures allow functions to retain access to their lexical scope even after the outer function has executed.

```js
function makeCounter() {
  let count = 0;
  return function() {
    count++;
    return count;
  };
}
const counter = makeCounter();
console.log(counter());
```

**Output:**  
1

---

**Lexical Scope**

Lexical scope defines how variable names are resolved in nested functions.

```js
function outer() {
  let outerVar = 'I am outer';
  function inner() {
    console.log(outerVar);
  }
  return inner;
}
const innerFunc = outer();
innerFunc();
```

**Output:**  
I am outer

---

**Hoisting**

Hoisting allows function declarations to be used before they are defined in the code.

```js
console.log(square(3));
function square(x) {
  return x * x;
}
```

**Output:**  
9

**Passing Functions as Arguments**

Functions can be passed as arguments, enabling high-order functions.

```js
function logGreeting(fn) {
  console.log(fn('Charlie'));
}
logGreeting(name => `Hello, ${name}!`);
```

**Output:**  
Hello, Charlie!

---

**Generator Functions**

Uses `yield` to pause and resume execution, producing a series of values.

```js
function* idGenerator() {
  let id = 1;
  while (true) {
    yield id++;
  }
}
const gen = idGenerator();
console.log(gen.next().value);
console.log(gen.next().value);
```

**Output:**  
1  
2

---

**Yield Keyword**

The `yield` keyword pauses a generator function and returns a value to the caller.

```js
function* fruitList() {
  yield 'Apple';
  yield 'Banana';
  yield 'Cherry';
}
const fruits = fruitList();
console.log(fruits.next().value);
console.log(fruits.next().value);
```

**Output:**  
Apple  
Banana

---

**yield Delegation**

`yield*` allows a generator to delegate part of its iteration process to another generator.

```js
function* numbers() {
  yield 1;
  yield 2;
}

function* moreNumbers() {
  yield* numbers();
  yield 3;
}
const genNums = moreNumbers();
console.log(genNums.next().value);
console.log(genNums.next().value);
console.log(genNums.next().value);
```

**Output:**  
1  
2  
3
---

# Arrays 
An array is a data structure that stores a collection of elements of the same data type in contiguous memory locations, meaning they are stored next to each other. Each element in the array can be accessed using its index, which is a numerical identifier starting from 0.

```js
 let fruits = ["apple", "banana", "cherry"];
console.log(fruits[0]); // prints "apple"
console.log(fruits[1]); // prints "banana"
console.log(fruits[2]); // prints "cherry"

let fruits = ["apple", "banana", "orange"];

``` 

Here

```js
  •	fruits[0] is "apple"
	•	fruits[1] is "banana"
	•	fruits[2] is "orange"
```
---

**Key features**

Can store multiple values (numbers, strings, objects, etc.)
You can add, remove, update, or loop through values

**reduce()** <br>
Reduces an array to a single value by applying a function accumulatively.

Example 

```js

let numbers = [1, 2, 3, 4];
let sum = numbers.reduce((accumulator, current) => accumulator + current, 0);
console.log(sum); // 10

```

**includes()** <br>

	Returns true if the array contains a certain value; otherwise false.

Example 

```js 

let fruits = ["apple", "banana", "orange"];
console.log(fruits.includes("banana")); // true
console.log(fruits.includes("grape")); // false

```

---

**push()** <br>

Adds one or more elements to the end of an array and returns the new length.

For example 

```js
let colors = ["red", "green"];
colors.push("blue");
console.log(colors); // ["red", "green", "blue"]

```


**map()** <br>

It changes every item in an array and gives you a new array with the changed items.
Example:
Imagine you have numbers and you want to add 1 to each:

Example: 
```js 

let numbers = [1, 2, 3];
let newNumbers = numbers.map(num => num + 1);
console.log(newNumbers); // [2, 3, 4]

```

---


**filter()**  <br>

It keeps only the items you want from an array.
E.G
Example

```js

let numbers = [3, 6, 8, 2];
let bigNumbers = numbers.filter(num => num > 5);
console.log(bigNumbers); // [6, 8]

```

**find()** <br>
It finds the first item that matches what is being searched   for.

Example:
Let’s find the first number bigger than 4:

```js

let numbers = [1, 3, 5, 7];
let firstBig = numbers.find(num => num > 4);
console.log(firstBig); // 5

```

---

**every()** <br>

Checks if all items in the array pass a test (all must be true).
Eg
Are all numbers on the greater than 0 

```js

let numbers = [1, 2, 3];
let allPositive = numbers.every(num => num > 0);
console.log(allPositive); // true

let numbers = [1, 2, 3];
let allPositive = numbers.every(num => num > 5);
console.log(allPositive); // false

```


**some()**  <br>
Checks if at least one item passes the test (only one needs to be true).

Example:
Is there any number bigger than 5?

```js

let numbers = [2, 4, 7];
let hasBig = numbers.some(num => num > 5);
console.log(hasBig); // true

```

---

**splice()**  <br>
Lets you remove or add items in the middle of the array.

```js 
let fruits = ["apple", "banana", "orange"];
fruits.splice(1, 1); // remove 1 item at index 1
console.log(fruits); // ["apple", "orange"]

let fruits = ["apple", "banana",”mango”, "orange"];
fruits.splice(1, 1); // remove 2 item at index 1
console.log(fruits); // ["apple", "orange"]

```

**forEach()** <br>
 An array method in JavaScript that executes a provided function once for each array element. It does not return a new array (unlike map() or filter()); it simply runs a function for every item in the array.

```js

et numbers = [10, 20, 30];
numbers.forEach(function(num) {
  console.log(num);
});
Output:
10
20
30

```

---

# Event

An event is any interaction or occurrence that happens in the browser. JavaScript uses events to respond to user actions.

**Common Properties of event objects**
- event.type : Type  of event (“click”, “keydown” etc.)
- event.target : This  element that triggered the event
- event.preventDefault() : This  stops default behavior
- event.stopPropagation() : This stops bubbling 

**Event Listener**

An event listener is a function that listens for a specific event and executes code when that event occurs.
```js
element.addEventListener("eventType", callbackFunction);

```
---

**Event Handler**

The function that is executed when an event occurs, it runs in response to an event. 

```js
function greetUser() {
  console.log("Hello, Gloria!");
}
```

**Ways to Assign Event Handlers**

- Assigning Handlers to DOM Properties (Inline or Direct)

You directly assign a function to an HTML element’s event property like ".onclick"
Assign a handler to elem.onclick, not elem.ONCLICK, because DOM properties are case-sensitive.

```js
let btn = document.getElementById("myBtn");
btn.onclick = function () {
  alert("Clicked!");
};

```
Note: this can only store one function at a time and it get replace when a new function is added by the new function addEventListener(). 

--- 

- Attaching multiple handlers to the same event, and it gives you more control. This is highly recommended.
```js
btn.addEventListener("click", function () {
  alert("Hello from listener!");
});
```
Note:  Handlers can also be remove later with removeEventListener().

**Event Object** <br>
The event object is passed automatically to every event handler. It holds all the details about what happened.
```js
btn.addEventListener("click", function (event) {
  console.log(event.type);
     //output
 "click"
  console.log(event.target); 
  //output
 The element that was clicked
});
```
---

**Object Handlers (Using Methods from an Object)**

A method of an object can be assigned as an event handler.
```js
let handler = {
  message: "Hello!",
  show() {
    alert(this.message);
  }
};
btn.addEventListener("click", handler.show.bind(handler));
```

**Event Propagation**

Propagation is how events travel through the DOM. It happens in three phases:
- Capturing phase : from the root down to the element.
- Target phase : the event reaches the actual target.
- Bubbling phase : event bubbles up from the target to the root.

```js
parent.addEventListener("click", () => console.log("Parent clicked"));
child.addEventListener("click", () => console.log("Child clicked"));
```
---

**Event Bubbling in JavaScript**

Event bubbling is a phase where an event starts from the target element and bubbles up to its parent elements. Almost all events in JavaScript bubble by default, which means they propagate upwards through the DOM hierarchy.

```js
// Event Bubbling Example
document.getElementById("child").addEventListener("click", () => {
  console.log("Child clicked");
});

document.getElementById("parent").addEventListener("click", () => {
  console.log("Parent clicked");
});
```

**UI Events**

These are events related to the user interaction with the web page or the browser window e.g Resize,
Load, Error, Focus/blur, Scroll

```js
window.addEventListener("resize", function () {
  console.log("Window resized!");
});

```
---

**Event Capturing**<br>
Event capturing is the first phase of event propagation. The event starts from document and travels down the DOM tree to the target element before bubbling back up.

How to use it:<br>
By default, addEventListener() listens during the bubbling phase. To catch it during the capturing phase, pass a third argument true.

```js

ddocument.getElementById("outer").addEventListener(
  "click",
  () => console.log("Outer - Capturing"),
  true // Enable capturing phase
);

```
---

# Forms
Forms are HTML elements used to collect user input. They typically contain text fields, checkboxes, radio buttons, submit buttons, and other interactive elements.

```js

form.addEventListener("submit", function (e) {
  e.preventDefault();
  console.log("Form submitted!");
});

```

**Form Submission**

By default, when a form is submitted:
	•	The browser reloads the page
	•	The form data is sent to the server via action/method.
To prevent this and handle it with JavaScript

```js
form.addEventListener("submit", function (e) {
  e.preventDefault(); // Stops page reload
  console.log("Data captured with JS!");
});

```
---

**Form Attributes**<br>
- Action: URl where form data should be sent
- Method: Get or Post
- Name: Name of the form or input 
- Required: Makes a field compulsory 
- Autocomplete: Helps a browser remember user input 

**JavaScript Form Handling Flow**

- Select the form with document.getElementById or similar.
- Add submit event listener.
- Use preventDefault() to stop real submission.
- Access form fields using form.elements or input names.
- Validate or send data with fetch() 
---

# Modules
**What is a Module?**
- A module is a file containing reusable code. Each module has its own scope and only what is exported can be accessed from outside

 **Why Modules?**
- Break code into smaller pieces
- Improve readability and maintenance
- Avoid naming conflicts

**Types of Modules**
- ES Modules (ESM) – import/export, standard
in modern JS
- CommonJS – require() /module.exports, used
in Node.js

---

Creating an ES Module
```js 
// math.js
export function add(a, b) {
return a + b;
}
```
Importing a Module
```js
// app.js
import { add } from './math.js';
console.log(add(2, 3));
```
Export Types
- Named Export: export function fn() {}
- Default Export: export default function() {}

```js
export default function greet() {
console.log("Hello!");
}
```
---

Benefits of Using Modules <br>
- Better code organization
- Reusability across files/projects
- Easier testing and debugging

**Browser vs Node.js**

ES Modules need 

```js 
<script type="module">
``` 
in browser

- Node.js supports ESM with .mjs or type: "module" in package.json

---

# Fetch API

The **Fetch API** is a built-in JavaScript interface that allows you to **make network requests** (like getting data from or sending data to a server). It is **promise-based**, making it cleaner and easier to handle asynchronous code 

**Basic Syntax**

```js
fetch(url, options)
  .then(response => {
    // handle the response
  })
  .catch(error => {
    // handle any errors
  });
```
---

**Making a GET Request**
```js

fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

**Making a Post Request**
```js
fetch('https://api.example.com/data', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
  },
  body: JSON.stringify(payload),
})
  .then(response => {
    if (!response.ok) {
      throw new Error(Server Error: ${response.status});
    }
    return response.json();
  })
  .then(data => console.log('Success:', data))
  .catch(error => console.error('Error:', error));
```
---

**Common HTTP Methods with Fetch**
- GET: Retrieve data.
- POST: Send data.
- PUT: Update data.
- DELETE: Remove data.

**Handling JSON Responses**

To read a JSON response, use: response.json() 

**Other methods**
- response.text()
- response.blob()
- response.formData()
---

**Setting Headers**
```js
  headers: {
  "Content-Type": "application/json",
  "Authorization": "Bearer token_here"
}
```

**Error Handling**

Fetch only rejects on **network errors**, not on HTTP status codes like 404 or 500.

So check status manually:
```js
 fetch('https://api.example.com/data')
  .then(response => {
    if (!response.ok) {
      throw new Error('Network response was not ok');
    }
    return response.json();
  }) 
```
---

**Async/Await Version**
```js
  fetchData() {
  try {
    const response = await fetch('https://api.example.com/data');
    if (!response.ok) throw new Error('Request failed');
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error('Error:', error);
  }
} 
```

**Use Cases**
* Fetching data from REST APIs
* Submitting form data
* Making authenticated requests
* Communicating with your own backend

---

# Javascript Promises

A JavaScript Promise is an object that represents the eventual completion (or failure) of an asynchronous operation and its resulting value. It serves as a placeholder for a value that may not be available yet but will be at some point in the future.

A Promise can be in one of three states:

- Pending: The initial state. The asynchronous operation is still in progress and the promise has neither been fulfilled nor rejected
- Fulfilled (or Resolved): The asynchronous operation completed successfully, and the promise now has a resulting value
- Rejected: The asynchronous operation failed, and the promise has a reason for the failure (an error).

---

The Promise object supports two properties: state and result.

While a Promise object is "pending" (working), the result is undefined.

When a Promise object is "fulfilled", the result is a value.

When a Promise object is "rejected", the result is an error object.

	
| myPromise.state          | myPromise.result           |
| ------------------------ | -------------------------- |
| "pending"                | undefined                  |
| "fulfilled"              | a result value             |
| "rejected"               | an error object            |


---


**JavaScript Promise Object**

A Promise contains both the producing code and calls to the consuming code:

```js
let myPromise = new Promise(function(myResolve, myReject) {
// "Producing Code" (May take some time)

  myResolve(); // when successful
  myReject();  // when error
});

// "Consuming Code" (Must wait for a fulfilled Promise)
myPromise.then(
  function(value) { /* code if successful */ },
  function(error) { /* code if some error */ }
);
```
When the producing code obtains the result, it should call one of the two callbacks:


| When                     | Call                     |
| ------------------------ | ------------------------ |
| Success                  | myResolve(result value)  |
| Error                    | myReject(error object)   |

---

**Promise How To**

- Here is how to use a Promise:

```js
myPromise.then(
  function(value) { /* code if successful */ },
  function(error) { /* code if some error */ }
);
```
Promise.then() takes two arguments, a callback for success and another for failure.

Both are optional, so you can add a callback for success or failure only.

---

Example

```js
function myDisplayer(some) {
  document.getElementById("demo").innerHTML = some;
}

let myPromise = new Promise(function(myResolve, myReject) {
  let x = 0;

// The producing code (this may take some time)

  if (x == 0) {
    myResolve("OK");
  } else {
    myReject("Error");
  }
});

myPromise.then(
  function(value) {myDisplayer(value);},
  function(error) {myDisplayer(error);}
);
```

---

**More JavaScript Promise Examples**
To demonstrate the use of promises, callback examples will be used:
- Waiting for a Timeout
- Waiting for a File

**Waiting for a Timeout**
Example Using Callback
```js
setTimeout(function() { myFunction("I love You !!!"); }, 3000);

function myFunction(value) {
  document.getElementById("demo").innerHTML = value;
}
```
Example Using Promise
```js
let myPromise = new Promise(function(myResolve, myReject) {
  setTimeout(function() { myResolve("I love You !!"); }, 3000);
});

myPromise.then(function(value) {
  document.getElementById("demo").innerHTML = value;
});
```
---

**Waiting for a file**

Example using Callback
```js
function getFile(myCallback) {
  let req = new XMLHttpRequest();
  req.open('GET', "mycar.html");
  req.onload = function() {
    if (req.status == 200) {
      myCallback(req.responseText);
    } else {
      myCallback("Error: " + req.status);
    }
  }
  req.send();
}

getFile(myDisplayer);
```

---

Example using Promise
```js
let myPromise = new Promise(function(myResolve, myReject) {
  let req = new XMLHttpRequest();
  req.open('GET', "mycar.html");
  req.onload = function() {
    if (req.status == 200) {
      myResolve(req.response);
    } else {
      myReject("File not Found");
    }
  };
  req.send();
});

myPromise.then(
  function(value) {myDisplayer(value);},
  function(error) {myDisplayer(error);}
);
```

---

# Javascript Async/Await <br>
**Javascript Async**
In JavaScript, "async" refers to the ability to perform tasks without blocking the main execution thread. This is crucial because JavaScript is inherently single-threaded, meaning it can only do one thing at a time.   

Here's a breakdown of what asynchronous JavaScript is all about:

**Synchronous vs. Asynchronous**
- Synchronous: In synchronous programming, code is executed line by line, in a strict sequence. Each operation must complete before the next one can begin. If a synchronous operation takes a long time (like fetching data from a server), the entire program will pause and become unresponsive until that operation finishes.   
- Asynchronous: Asynchronous programming allows certain tasks to be initiated, and while they are running in the background, the JavaScript engine can continue executing other code. Once the asynchronous task is complete, a mechanism is in place to handle its result or any errors that occurred.

---

**Async Syntax**

The keyword async before a function makes the function return a promise:

Example
```js
async function myFunction() {
  return "Hello";
}
```
is the same as

```js
function myFunction() {
  return Promise.resolve("Hello");
}
```
Here is how to use the Promise:
```js
myFunction().then(
  function(value) { /* code if successful */ },
  function(error) { /* code if some error */ }
);
```

---

**Await Syntax** <br>
The `await` keyword can only be used inside an `async` function.

The `await` keyword makes the function pause the execution and wait for a resolved promise before it continues:
```js
let value = await promise;
```
Example <br>
Basic Syntax
```js
async function myDisplay() {
  let myPromise = new Promise(function(resolve, reject) {
    resolve("I love You !!");
  });
  document.getElementById("demo").innerHTML = await myPromise;
}

myDisplay();
```
The two arguments (resolve and reject) are pre-defined by JavaScript.

We will not create them, but call one of them when the executor function is ready.

Very often we will not need a reject function.

---

- Example without reject
```js
async function myDisplay() {
  let myPromise = new Promise(function(resolve) {
    resolve("I love You !!");
  });
  document.getElementById("demo").innerHTML = await myPromise;
}

myDisplay();
```

---
layout: center
class: text-center text-8xl font-extrabold
---

<div class="text-yellow-600 animate-bounce">
  THANK YOU
</div>

<br/>

<p class="text-4xl text-gray-500 mt-4 animate-fade-in">

</p>

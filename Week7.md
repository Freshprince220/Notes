# HTML

## HTML-CSS

* <u>What is HTML?</u>
   - **HTML** stands for Hypertext Markup Language and consists of various tags to describe the content of a document - utilized as the basis for all web pages, along with CSS and JavaScript
* <u>What is the structure of an HTML document? List some tags. What is `<head>` used for? `<body>`?</u>
   - Start with the doctype declaration, then `<html>`, then `<head>` and `<body>`. The head contains the metadata for the page, while the body contains the content that is rendered to the screen. Other tags: div, span, p, ul, ol, li, strong, em, table
* <u>What is a doctype?</u>
   - First tag in the document - defines what type of file it is - whether html 4 or 5, etc
* <u>What is the tag for an ordered list? Unordered list?</u>
   - ordered list: `ol`, unordered list: `ul`. Both use `li` - list items
* <u>What are some HTML5 tags? Why were HTML5 tags introduced?</u>
   - HTML5 introduced semantic tags to more accurately reflect the content of the tags. Examples: `<strong>` instead of `<b>`, `<em>` instead of `<i>`, `<nav>`, `<header>`, `<footer>`, `<section>`, `<article>`, and `<aside>` instead of reusing `<div>` tags everywhere
* <u>Do all tags come in a pair?</u>
	- No 
	* <u>What are the other things inside tags called? list some.</u>
	   - tags either have a closing tag or are self-closing (`<tag />`). Attributes are contained within tags - examples: id, class, style, height, width, etc
* <u>What is the syntax for a comment in HTML?</u>
   - `<!-- comments go in here -->`
* <u>Give me the HTML markup for a table.</u>
```html
<table>
	<caption>
		optional
	</caption>
	<thead>
		<tr>
			<td>Heading 1</td>
			<td>Heading 2</td>
	    </tr>
	</thead>
	<tr>
		<td>Cell 1</td>
		<td>Cell 2</td>
	</tr>
	<tbody></tbody>
</table>
```
* <u>What are some tags you would use in a form?</u>
   - ***Form tags***: `<form>`, `<input>`, `<label>`, `<textarea>`, `<button>`, `<select>`, `<option>`
* <u>What is CSS?</u>
	- ***CSS*** stands for Cascading Style Sheets - it is a language for styling HTML documents by specifying certain rules for layout and display in key/value pairs. 
	* <u>What are the different ways of styling an HTML file?</u>
		-  There are 3 ways of styling an HTML file:
		    - (1) inline - in the `style` attribute
		    - (2) internal stylesheet - in the `<style>` tag in the `<head>`
		    - (3) external stylesheet - using external `.css` file, use `<link>` in the `<head>`
	* <u>Which is best? why?</u>
	    - External stylesheet is best practice due to separation of concerns, reusability, modularity
* <u>Describe the CSS box model.</u>
    - The box model consists of margin (outermost box), then border, then padding, then content (innermost). All box sizes / formatting can be styled with CSS
* <u>Which way has highest priority when styles cascade: inline, internal, or external?</u>
    - Inline has highest priority, then internal/external depending on order. Cascading rules are determined by (1) importance (`!important` flag), (2) specificity of selector (inline has no selector, highest specificity), then (3) source order.
* <u>What is the syntax for styling an element? </u>
```css
div {
	property: value;
}
``` 
* <u>What is a class and how to style them? </u>
		- ***class***: 
```css
.class {
	property: value;
}
```
* <u>What is an id? how to style? difference?</u>
	* ***id***:
```css
#id {
	property: value;
}
```
* <u>What if I want to select child elements, What syntax is that?</u>
    - use direct descendant selector (`>`) or space for any level nested element
* <u>Can I select multiple elements at once? How?</u>
    - yes, with a comma
* <u>What is a psuedo-class? What is syntax for selecting that?</u>
    - ***psuedo-class*** selects an element in a certain state - for example, when hovered over. Use colon (`:psuedoselector`) syntax
* <u>What is Bootstrap?</u>
    - ***Bootstrap*** is a CSS framework with pre-written CSS rules to easily style your page and incorporate responsive design seamlessly. Contains various utilities and components for making a great UI
* <u>Describe the Bootstrap grid system</u>
	- The Bootstrap grid is divided into 12 columns. You wrap the columns in a `.row` which is in a `.container` or `.container-flex`. The columns are responsive - there are classes for different screen sizes which collapse on smaller windows

# JavaScript

## Language Fundamentals

### Basic

* <u>What is JavaScript? What do we use it for?</u>
	- ***JavaScript*** is a programming language used both on the client-side and server-side that allows you to make web pages interactive. Where HTML and CSS are languages that give structure and style to web pages, JavaScript gives web pages interactive elements that engage a user.
* <u>Can we run JavaScript in a web browser, on a server, or both?</u>
	- Both
* <u>What are the benefits of JS over your core language? Drawbacks?</u>
	- JavaScript is an 'interpreted' language and reduces the time required compilation. JS supports features such as dynamic typing and smaller executable program size. Java uses Threads. JavaScript runs on a single thread that responds to events when they occur. JS handles concurrency using a queue system that is called the "event loop".
* <u>What programming paradigm(s) does JS support?</u>
	- JavaScript is a prototype-based, multi-paradigm scripting language that is dynamic, and supports object-oriented, imperative, and functional programming styles.
* <u>What are the data types in JS?</u>
	- 8 datatypes. 7 primitive 1 object  
		- Primitive values (immutable datum represented directly at the lowest level of the language)  
			- Boolean type  
			- Null type  
			- Undefined type  
			- Number type  
			- BigInt type  
			- String type  
			- Symbol type  
		- Objects (collections of properties)
 * <u>What is the type of NaN? What is the isNaN function?</u>
	  - NaN is number. NaN is a property of the global object. In other words, it is a variable in global scope. initial value of NaN is Not-A-Number  
The isNaN() function determines whether a value is NaN or not. Returns BOOLEAN
* <u>What is the data type of a function?</u>
	- You can logically think of Function as a subclass of Object
 * <u>What is the data type of an array?</u>
	  - Arrays are just regular objects
 * <u>What is the difference between undefined and null?</u>
	  - undefined means a variable has been declared but has not yet been assigned a value.  
null is an assignment value. It can be assigned to a variable as a representation of no value
* <u>What are JS objects? what is the syntax?</u>
	- JavaScript object is a standalone entity that holds multiple values in terms of properties and methods. Object property stores a literal value and method represents function. An object can be created using object literal or object constructor syntax. Object properties and methods can be accessed using dot notation or [ ] bracket. An object is passed by reference from one function to another. An object can include another object as a property. Use the object literal syntax to create an object with some properties
```javascript
let person = "John Doe";
```
```javascript
let person = {
	firstName:"John", 
	lastName:"Doe", 
	age:50, 
	eyeColor:"blue"
};
```
* <u>What are arrays in JS? Can you change their size?</u>
	- Arrays are objects. Can be resized
* <u>List some array methods and explain how they work.</u>
	- `toString()`: converts an array to a string of (comma separated) array values
	- `join()`: joins all array elements into a string but you can specify the separator
	- `pop()`: removes the last element from an array
	- `push()`: adds a new element to an array (at the end)
	- `shift()`: returns the value that was "shifted out"
	- `unshift()`: adds a new element to an array (at the beginning), and "unshifts" older elements
	- `length`: provides an easy way to append a new element to an array
	- `delete`: deletes element of array but leaves `undefined` holes in the array
	- `splice()`: can be used to add new items to an array at your desired positions. It can also be used to remove elements at a desired position.
* <u>What is JSON? Is it different from JS objects?</u>
	- Unlike JavaScript Object, a JSON Object has to be fed into a variable as a String and then parsed into JavaScript. A framework like jQuery can be very helpful when doing parsing.
* <u>What are some ways you can use functions in JS?</u>
	-  
* <u>What are the different scopes of variables in JS?</u>
	- Global Scope
	- Block Scope
	- Function Scope
 * <u>What are the different ways to declare global variables?</u>
	 - The variables declared outside any function are called global variables. They are not limited to any function. Any function can access and modify global variables. Global variables are automatically initialized to `0` at the time of declaration. Global variables are generally written before `main()` function.
 * <u>Is it a best practice to use global variables? Why or why not?</u>
	 - No. The best practice is to make a variables scope the smallest possible. This increases readability and reduces the chances or redefining the variable when not intended. 
* <u>What are some methods on the function prototype?</u>
	- `Object.getPrototypeOf(obj)`:  to access prototype object
	- `hasOwnProperty()`: Returns a boolean indicating whether an object contains the specified property as a direct property of that object and not inherited through the prototype chain.
	- `isPrototypeOf()`: Returns a boolean indication whether the specified object is in the prototype chain of the object this method is called upon.
	- `propertyIsEnumerable()`: Returns a boolean that indicates whether the specified property is enumerable or not.
	- `toLocaleString()`: Returns string in local format.
	- `toString()`: Returns string.
	- `valueOf`: Returns the primitive value of the specified object.
* <u>If you declare a variable `var` inside a for loop is that block scoped or function scoped?</u>
	- Function scoped because var is function scoped
 * <u>If you declare a variable `let` inside a for loop is that block scoped or function scoped?</u>
	 - Block scoped because let is block scoped
* <u>What will happen?</u>
```javascript
const hi;
hi = 3;
console.log(hi);
```
Solution:
```javascript
SyntaxError: Missing initializer in const declaration
``` 
*  <u>What are callback functions?</u>
	- ***callback*** is a function passed as an argument to another function. This technique allows a function to call another function. A callback function can run after another function has finished
* <u>What about self-invoking functions?</u>
	- ***self-involking***: expression is invoked (started) automatically, without being called. Function expressions will execute automatically if the expression is followed by (). You cannot self-invoke a function declaration. You have to add parentheses around the function to indicate that it is a function expression.
* <u>What is a truthy or falsy value? List the falsy values.</u>
	- A truthy value is a value that is considered true when encountered in a Boolean context, while a falsy value is considered false in a Boolean context. There are only a handful of falsy values.
	- *falsy values*: 
		- Boolean: `false`
		- Number: `0`, `-0`
		- BigInt: `0n`
		- String: `""`, `''`, ``
		- `null`
		- `undefined`
		- `NaN`
		- `document.all`
* <u>What prints?</u>
```javascript
let x = 5;
while(x) {
	x--;
	console.log(x);
}
```
Solution:
```javascript
4
3
2
1
0
```
* <u>What is the difference between == and ===? Which one allows for type coercion?</u>
	- `==` tests values against their "truthy/falsy" values, while `===` tests values against their actual values. In other words `==` will type coerce while `===` will not.
* <u>What is the difference between `for of` and `for in`?</u>
	- Both `for in` and `for of` are looping constructs which are used to iterate over data structures. The only difference between them is the entities they iterate over:  
`for in` iterates over all enumerable property keys of an object  
`for of` iterates over the values of an iterable object. Examples of iterable objects are arrays, strings, and NodeLists.
* <u>What does the following code do?</u>
```javascript
function addOne(value) {
	value + 1;
}
let x = 5;
addOne(x);
console.log(x);
```
Solution:
```javascript
5
```
* <u>What does the following code do?</u>
```javascript
function changeUsername(user) {
	user.username = 'new-username';
}
let user = {
	username: 'first-username'
};
changeUsername(user);
console.log(user.username);
```
Solution:
```javascript
new-username
```
**why?:** because objects are mutable (only objects and arrays are mutable, meaning they can be changed).
* <u>What is the difference between a do-while and a while loop?</u>
	- while tests condition first then executes. do-while executes first then tests condition. do-while ensures it runs at least once.
* <u>What does this do?</u>
```javascript
for(;;){
	console.log('a');
}
```
Solution:
```javascript
a
a
a
a
a
a
...
```
prints out `a` in an infinite loop.
* <u>What is fall-through with regard to switch statements?</u>
	- Is the behaviour of moving on to next case statement if break keyword is not used. Will keep moving down until broken
* <u>What is the difference between `console.log(++x)` and `console.log(x++)`?</u>
	- `++x` pre-increment - is incremented before value is used  
	- `x++` post-increment - is incremented after value is used
* <u>Explain what “strict mode” does.</u>
	- Eliminates some JavaScript silent errors by changing them to throw errors.  
Fixes mistakes that make it difficult for JavaScript engines to perform optimizations: strict mode code can sometimes be made to run faster than identical code that's not strict mode.  
Prohibits some syntax likely to be defined in future versions of ECMAScript  
* <u>What are the naming conventions for a variable used in JavaScript?</u>
	-  You should not use any of the JavaScript reserved keywords as a variable name. These keywords are mentioned in the next section. For example,  **break** or  **boolean** variable names are not valid.
	-  JavaScript variable names should not start with a numeral (0-9). They must begin with a letter or an underscore character. For example,  **123test** is an invalid variable name but  **_123test** is a valid one.
	-  JavaScript variable names are case-sensitive. For example,  **Name** and  **name** are two different variables.
* <u>What are the naming conventions for a function used in JavaScript?</u>
	- JavaScript functions are written in **camelCase** too, it’s a best practice to actually tell _what the function is doing by giving the_ **_function name a verb as prefix_**

### Intermediate

* <u>What is function and variable hoisting?</u>
	- refers to the process whereby the interpreter appears to move the  _declaration_  of functions, variables or classes to the top of their scope, prior to execution of the code. Hoisting allows functions to be safely used in code before they are declared. Variable and class  _declarations_  are also hoisted, so they too can be referenced before they are declared.
* <u>What is closure and when should you use it?</u>
	- ***closures*** are defined as inner functions that have access to variables and parameters of outer function even after the outer function has returned.
	- ***when***:
		- **Using private variables and methods:** In JavaScript, we can use private variables and methods using closures.
		- **Maintaining state between each function call:**  Suppose there is a function and one would like it to multiply multiple values together. This could be done with the help of a global variable as they are accessible throughout the program. However, a drawback is that they are prone to change from anywhere in the code. This can be done alternatively using closures. Closures help in maintaining the state between function calls without using a global variable.
* <u>What does the following code do?</u>
```javascript
let arr = [1, 2, 3, 4];
let x = arr.forEach(function(x){
	return x*x;
});
console.log(x);
```
Solution:
```javascript
undefined
```
* <u>What does the following code do?</u>
```javascript
let arr = [1, 2, 3, 4];
let x = arr.map(function(x){
	return x*x;
});
console.log(x);
```
Solution:
```javascript
[ 1, 4, 9, 16 ]
```
* <u>What does the "this" keyword refer to?</u>
	- `this`  is a special keyword in Javascript that refers to the executing environment of the function:
		- If you execute a function in the global scope,  `this`  will be bound to the window
		- If you pass the function to a callback for an event handler,  `this`  will be bound to the DOM element that raised the event
* <u>Explain the concept of lexical scope:</u>
	- Another name for lexical scope is _static scope_. An item's lexical scope is the place in which the item got _created_.
* <u>Explain how inheritance works in JS:</u>
	- inheritance is supported by using prototype object meaning that objects and methods can be shared, extended, and copied. 
* <u>How would you rewrite this using an anonymous function? Arrow function?</u>
```javascript
function hello(){
	console.log('hello');
}
document.getElementById('hi').addEventListener(hello);
```
***Anonymous Function***:
```javascript
let hello = function(){
	console.log('hello');
}
document.getElementById('hi').addEventListener(hello);
```
***Arrow Function***:
```javascript
let hello = () => {
	console.log('hello');
}
document.getElementById('hi').addEventListener(hello);
```
* <u>What is the difference between `setInterval()` and `setTimeout()`?</u>
	- ***setInterval***: method calls a function or evaluates an expression at specified intervals (in milliseconds).
	- ***setTimeout***: calls a function or evaluates an expression after a specified number of milliseconds
  * <u>How would you stop a `setInterval()` once it has been set?</u>
	  - method will continue calling the function until `clearInterval()` is called, or the window is closed.
  * <u>Advanced: How do they work with regards to the callback queue?</u>
	  - Internet Explorer versions 9 and below do not support the passing of arguments to the callback function in either `setTimeout()` or `setInterval()`.
	  - Another possibility is to use an anonymous function to call your callback
* <u>How would you handle an error in JS?</u>
	- The  `try`  statement lets you test a block of code for errors.
	- The  `catch`  statement lets you handle the error.
	- The  `throw`  statement lets you create custom errors.
	- The  `finally`  statement lets you execute code, after try and catch, regardless of the result.
* <u>What attributes does an Error object have?</u>
	- ***message***: Sets or retrieves the error message as a string.
	- ***name***: Sets or retrieves the name of the error.
	- ***protoype***: Returns a reference to the **Error.prototype** object. The **Error.prototype** object allows adding properties and methods to the **Error** object that can be used with instances of the **Error** object, like any predefined property or method. The **prototype** property is static, it cannot be accessed from an instance of the **Error** object, only **Error.prototype** is allowed.
* <u>What is an Immediately Invoked Function Expression?</u>
	-  Functions that are executed as soon as they are mounted. This type of function is called immediately invoked as these functions are executed as soon as they are mounted to the stack, it requires no explicit call to invoke the function. JavaScript lets us use Functions as Function Expression if we Assign the Function to a variable, wrap the Function within parentheses or put a logical not in front of a function.
  * <u>How would you write one?</u>
```javascript
(function() {})();
```

### Advanced

* <u>What are some characteristics of the functional programming paradigms?</u>
	- 
* <u>What does it mean for a function to have no side effects?</u> (what is a pure function?)
	- 
* <u>What are the advantages to using a functional approach?</u> (as opposed to OOP)
	- 
* <u>Explain how the guard and default operators work:</u>
	- 
* <u>What happens?</u>
```javascript
let h = 'hello';
function process(input) {
	return input || 'goodbye';
}
console.log(process(h));
console.log(process());
```
Solution:
```javascript
hello
goodbye
```

### Bonus

* <u>What will happen when I try to run this code: `console.log(0.1+0.2==0.3)` ?</u>
Solution:
```javascript
false
```
**why?**: `.1+.2= 0.30000000000000004` because of floating point math 
* <u>What happens?</u>
```javascript
h = 3;
function hello(){
	h = 6;
}
hello();
console.log(h)
```
Solution:
```javascript
6
```
* <u>What prints?</u>
```javascript
let x = 5;
let b = 2;
for(let i = 0; i < 5; i++) {
	b = b + 1;
}
if(b = x) {
	console.log(b);
} else {
	console.log('Oh no. :(');
}
```
Solution:
```javascript
5
```
The if statement sets b equal to x so the for loop doesn't do anything.

## ES6+

### Basic

* <u>What standard is JS based off of?</u>
	- ECMAScript Language Specification
* <u>What is the difference between var, let, and const keywords?</u>
	- ***var***: function-scoped
	- ***let***: block-scoped
	- ***const***: block-scoped The value of a constant can't be changed through reassignment (i.e. by using the assignment operator), and it can't be redeclared (i.e. through a variable declaration). However, if a constant is an object or array its properties or items can be updated or removed.
* <u>How would we rewrite this code with a template literal?</u>
```javascript
let n = 'Dorian';
let message = 'My name is '+ n;
console.log(message);
```
Solution:
```javascript
let n = `Dorian`;
let message = `My name is `+ n;
console.log(message);
```
Template literals are enclosed by the backtick (` `)
* <u>What will print?</u>
```javascript
let arr = ['chicken', 'pig', 'cow'];
for(let i in arr) {
	console.log(i);
}
for(let i of arr) {
	console.log(i);
}
```
Solution:
```javascript
0
1
2
chicken
pig
cow
```
* <u>What will happen?</u>
```javascript
let arr = ['chicken', 'pig', 'cow'];
for(const i in arr) {
	console.log(i);
}
```
Solution:
```javascript
0
1
2
```

### Intermediate

* <u>What’s the difference between a normal function declaration and an arrow function?</u>
	- ***arrow functions*** do not have their own `this`.
	- Arguments objects are not available in ***arrow functions***, but are available in ***normal functions***.
	- Regular functions created using function declarations or expressions are ‘constructible’ and ‘callable’. Since regular functions are constructible, they can be called using the ‘new’ keyword. However, the arrow functions are only ‘callable’ and not constructible. Thus, we will get a run-time error on trying to construct a non-constructible arrow functions using the new keyword.
* <u>Does JS have classes?</u>
	- yes
	* <u>How does this relate to Prototypal inheritance in JS?</u>
		- 
	* <u>What is the difference between a Prototype and a Class?</u>
		- 
* <u>How would you set default values for parameters to a function?</u>
	- within the function or in the function declaration (ECMAScript 2015 allows the latter)
```javascript
function myFunction(x, y) {  
	if (y === undefined) {  
		y = 2;  
	}  
}
```
```javascript
function myFunction (x, y = 2) {  
	// function code  
}
```
* <u>What’s the benefit of computed property names?</u>
	- 
* <u>What is a promise?</u>
	* The `Promise` object represents the eventual completion (or failure) of an asynchronous operation and its resulting value.  A `Promise` is a proxy for a value not necessarily known when the promise is created. It allows you to associate handlers with an asynchronous action's eventual success value or failure reason. This lets asynchronous methods return values like synchronous methods: instead of immediately returning the final value, the asynchronous method returns a *promise* to supply the value at some point in the future.
* <u>Explain the `async`/`await` keywords. Why is it preferred to use this instead of `.then()` methods?</u>
	- ***async***  makes a function return a Promise
	- ***await***  makes a function wait for a Promise
	- preferred over `then` because these other two save you a bunch of lines of code making your code simpler to read, test and maintain.
* <u>How could you make the program print out the statements in order?</u>
```javascript
function getData(){
	console.log("2. Getting data from internet, please wait.")
	return setTimeout(function(){
		console.log("3. Returning data from internet after 1000 milliseconds.")
		return [{name: "Avi"}, {name: "Grace"}]
	}, 1000)
}
function main(){
	console.log("1. Starting Script")
	const data = getData()
	console.log(`4. Data is currently ${data}`)
	console.log("5. Script Ended")    
}
main();
```
Solution:
```javascript
function getData(){
	console.log("2. Getting data from internet, please wait.")
	return new Promise(function(resolve){
		setTimeout(function(){
			console.log("3. Returning data from internet.")
			resolve([{name: "Avi"}, {name: "Grace"}])
		}, 1000)
	})
}
async function main(){
	console.log("1. Starting Script")
	const data = await getData()
	console.log(`4. Data is currently ${JSON.stringify(data)}`)
	console.log("5. Script Ended")
}
main()
```
* <u>How do you interact with a Promise?</u>
	- 
	* <u>When would it be appropriate to use a Promise?</u>
		- 
* <u>Write a method that would print to the console the value returned by the promise?</u>
```javascript
function helloPromise() {
	let p = new Promise();
	setTimeout(p.resolve(`Hello World`), 500);
	return p;
}
```
Solution:
```javascript
helloPromise().then(r -> console.log(r));
```
* <u>Convert this function to use named parameters?</u>
```javascript
function add(x, y) {
	return x + y;
}
```
Solution:
```javascript
function add(options) {
	return options.x + options.y;
}
```
    
### Advanced

* <u>What is a Symbol?<u> 
	- A JavaScript Symbol is a primitive datatype just like Number, String, or Boolean. It represents a unique "hidden" identifier that no other code can accidentally access. Symbols are always unique. If you create two symbols with the same description they will have different values.
	* <u>What is the advantage using Symbol?</u>
		-  They are always unique.
* <u>How could you reference this module in your code?</u>
```javascript
export const qcScore = `RED`;
```
Solution:
```javascript
import {qcScore} from './filenameTheyShouldAskForFromQC.js';
```
* <u>What is object and array destructuring?<u>
	- 
	* <u>Give me an example using the rest/spread operator?</u>
		-  **Spread operator** allows an iterable to expand in places where 0+ arguments are expected: `var variablename1 = [...value];`
* <u>What is a generator function?</u>
	- 
	* <u>What’s the point of the yield keyword?</u>
		- 
* <u>What built-in advanced objects does JavaScript provide?</u>
	- 
* <u>What will this print?</u>
```javascript
let fname = "Bobbert";
let lname = "Bobbertson";
let role = "manager";
let status = "active";
let user = {
	fname,
	lname,
	[role]: status,
	fullname: () => `${fname} ${lname}`
};
console.log(user);
console.log(user.fullname());
```
Solution:
```javascript
{ fname: 'Bobbert',
	lname: 'Bobbertson',
	manager: 'active',
	fullname: [Function: fullname] }
Bobbert Bobbertson
```

## DOM Manipulation

* <u>Explain the following code:</u>
```javascript
document.getElementById("myid").addEventListener('click', (e) => {
	e.stopPropagation();
});
```
**answer:** looks for a click then `stopPropagation()` method of the `Event` interface prevents further propagation of the current event in the capturing and bubbling phases
* <u>What is the global object in client-side JavaScript?</u>
	- 
	* <u>What are some built-in functions on this object?</u>
		- 
**example answers**: `window` is the correct answer (document is a field on the window object), but `document` is also acceptable.
* <u>What is the DOM?</u>
	- When a web page is loaded, the browser creates a **D**ocument **O**bject **M**odel of the page. The HTML DOM is an object based interface that allows JavaScript and other entities manipulate and create HTML elements dynamically.
	* <u>How is it represented as a data structure?</u>
		- 
	* <u>What object in a browser environment allows us to interact with the DOM?</u>
		- 
* <u>List some ways of querying the DOM for elements</u>
	-  `getElementById`: Finding HTML elements by id
	- `getElementsByTagName`: Finding HTML elements by tag name
	-  `getElementsByClassName`: Finding HTML elements by class name
	-  `querySelectorAll`: Finding HTML elements by CSS selectors
	-  Finding HTML elements by HTML object collections
* <u>How would you insert a new element into the DOM?</u>
	- 
* <u>What are event listeners?</u>
	- The  `addEventListener()`  method attaches an event handler to an element without overwriting existing event handlers. You can add many event handlers of the same type to one element, i.e two "click" events. You can add event listeners to any DOM object not only HTML elements. i.e the window object.
	* <u>What are some events we can listen for?</u>
		- `onchange`: An HTML element has been changed
		- `onclick`: The user clicks an HTML element
		- `onmouseover`: The user moves the mouse over an HTML element
		- `onmouseout`: The user moves the mouse away from an HTML element
		- `onkeydown`: The user pushes a keyboard key
		- `onload`: The browser has finished loading the page
	* <u>What are some different ways of setting event listeners?</u>
		- 
* <u>What is bubbling and capturing and what is the difference?</u>
	- **Event bubbling** is a method of event propagation in the HTML DOM API when an event is in an element inside another element, and both elements have registered a handle to that event. It is a process that starts with the element that triggered the event and then bubbles up to the containing elements in the hierarchy. In event bubbling, the event is first captured and handled by the innermost element and then propagated to outer elements.
	- **Event capturing** is one of two ways to do event propagation in the HTML DOM. In event capturing, an event propagates from the outermost element to the target element. It is the opposite of **event bubbling**.
* <u>What are some methods on the event object and what do they do?</u>
	- 
* <u>Why is `Hello` not visible on the page after calling this function?</u>
```javascript
function addElementToBody() {
	let body = document.getElementsByTagName('body');
	body.innerHTML = '<p>Hello</p>';
}
```
**answer:** You can't append a child to an `htmlCollection`.

### Bonus
* <u>What happens?</u>
```javascript
location = 'www.google.com';
console.log(location);
```
Solution:
```javascript
www.google.com
```

## Asynchronous Web

* <u>What is AJAX? Why do we use it? </u>
	- AJAX =  **A**synchronous  **J**avaScript  **A**nd  **X**ML. 
	- AJAX is not a programming language.
	- AJAX just uses a combination of:
		-   A browser built-in XMLHttpRequest object (to request data from a web server)
		-   JavaScript and HTML DOM (to display or use the data)
	* <u>What are the benefits of using AJAX?</u>
		- 
	* <u>Are there any downsides of using AJAX?</u>
		- 
* <u>Explain why it is important that AJAX is asynchronous</u>
	- 
* <u>List the steps to sending an AJAX request</u>
	- 
* <u>What are steps to sending an AJAX request?</u>
	- `open(method, url, async)`: Specifies the type of request.
		- _method_: the type of request: GET or POST
		- _url_: the server (file) location
		-  _async_: true (asynchronous) or false (synchronous)
	- `send()`: Sends the request to the server (used for GET)
	- `send(string)`: Sends the request to the server (used for POST)
* <u>List the different ready states of the XmlHttpRequest object</u>
	- Holds the status of the XMLHttpRequest.  
0: UNSENT - Client has been created. `open()` not called yet.
1: OPENED - `open()`  has been called.
2: HEADERS_RECIEVED - `send()`  has been called, and headers and status are available.
3: LOADING - Downloading;  `responseText`  holds partial data.
4: DONE - The operation is complete.
* <u>How would retrieve JSON data from an AJAX request?</u>
	- 
* <u>How do you handle a failed request in AJAX?</u>
	- 
* <u>What is the Fetch API?</u>
	- The Fetch API is a modern interface that allows you to make HTTP requests to servers from web browsers. 
* <u>How do you send a Fetch request?</u>
	-  Calling fetch returns a promise, with a Response object.
	- A sample FETCH request -
```javascript
fetch(url)
  .then(response => response.json())
  .catch(err => console.log(err))
```
* <u>What is the difference between Fetch and AJAX?</u>
	- 
* <u>How would you retrieve JSON data from a Fetch request?</u>
	- 
* <u>How do you handle a failed request in Fetch?</u>
	- 

### Bonus

* <u>How would you retrieve XML data from an xhr object?</u>
	- 

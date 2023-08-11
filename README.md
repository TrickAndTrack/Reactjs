# Reactjs

What is React ?
A library for building user interface.
A JavaScript library for building user interface.
React is all about components.
| First Img  | Second Img |
| ------------- | ------------- |
|![image](https://github.com/TrickAndTrack/Reactjs/assets/73180409/4f792a18-15a5-45f9-ac0c-cb98cb8aec8a) |![image](https://github.com/TrickAndTrack/Reactjs/assets/73180409/cb7d5e8d-2b46-459d-8951-e894a63d0d63)|
| ![image](https://github.com/TrickAndTrack/Reactjs/assets/73180409/a46dab2c-d2ca-4d58-81a5-95bea33b3918) | ![image](https://github.com/TrickAndTrack/Reactjs/assets/73180409/9718107d-2703-42d6-83df-3e14e3519a91)|

> but why wolud use it?
> why not just JavaScript?

| First Img  | Second Img |
| ------------- | ------------- |
|![image](https://github.com/TrickAndTrack/Reactjs/assets/73180409/59e298d1-7586-4926-8e5b-cfc7142d2e38) |![image](https://github.com/TrickAndTrack/Reactjs/assets/73180409/77c58181-6ea5-4ba5-97ae-3c558790d66e)|

# React Topic
![image](https://github.com/TrickAndTrack/Reactjs/assets/73180409/2e2a9b79-9b39-4c99-9349-a6403aa46d38)

#### Two way to create a react project 
![image](https://github.com/TrickAndTrack/Reactjs/assets/73180409/2673abd2-21f5-4e62-8a7c-3d10c055b095)

### React & components

JSX stand for JavaScript XML

### How React work?
We ultimately built our own custom HTML elements & React is all about components.
we built those components and a componentis basically just a custom HTML elements.

> App.js is special kind of components, it will be our so-called, root Component.

- Organize our soruce code in components folder
- Common convention in react application to name it like this Starting with captila character in one word where if you coombin multiple words in one word so every sub word starts with new Capital character 
> a) Expense.js b)ExpernseItem.js 

## We build A Component Tree
```
<App/> ------><Tasks/>
   |         <Task/> <Task/><Task/>
<Header/>       
```
-app.js rendered into single HTMl page


# props

props simply stands for propertites.


## Question

#### Question 1 Why Components ?

Answer 
- Reusability {Don't repeat yourself}
- Sepration of concearn {Don't do too many things in one and same place (function)} 
> split big chunks of code into multiple smalller function] 


#### Question 2 How is A Components build ? or how a exactly Components build?

Answer a) Combination of HTML CSS & JavaScript

#### Question 3 How is A Components written in react?
Answer
- It's just s function 
- A Component in react is just  a JavaScript function.
```
  function App() {
  return (
    <div className="App">
     
    </div>
  );
}

export default App;
```
# JavaScript Refresher
1) Basic Syntax & Rules
2) Vaerables, Value & Operators
3) Function
4) Objects
5) Arrays
6) Control Structures
7) Brower APIs & The DOM
8) Essential Features Used by React 
9) Tricky Parts



# JavaScript Can be excuted in many Environments
1) in the browser
2) on any Computer
3) On mobile Dervices


### Adding JavaScript code To A website
![image](https://github.com/TrickAndTrack/Reactjs/assets/73180409/1c3b1a18-b126-4027-a520-9c3509742e48)
Via <Srcipt> Import is a best way to apply JS.
bewtween<Srcipt> Tags
typically onl used for evry short scripts.

> React Project use a build process.
# ES6 Import and Export
The ES6 is a JavaScript standard. With the help of ES6, we can create modules in JavaScript. In a module, there can be classes, functions, variables, and objects as well. To make all these available in another file, we can use export and import. The export and import are the keywords used for exporting and importing one or more members in a module.

Export: You can export a variable using the export keyword in front of that variable declaration. You can also export a function and a class by doing the same.
```
// Syntax for variable:
export let variable_name;
// Syntax for function:
export function function_name() {
  // Statements
}
// Syntax for class:
export class Class_Name {
  constructor() {
    // Statements
  }
}
```
Import: You can import a variable using import keyword. You can specify one of all the members that you want to import from a JavaScript file.
```
Syntax:
import member_to_import from “path_to_js_file”;
// You can also use an alias while importing a member.
import Greeting as Greet from "./export.js";
// If you want to import all the members but don’t
// want to Specify them all then you can do that using
// a ' * ' star symbol.
import * as exp from "./export.js";
```
# Arrow Function
More on the Arrow Function Syntax
When working with Arrow Functions, you have a couple of "syntax shortcuts" available.

Most importantly, you should know about the following alternatives:

1) Omitting parameter list parentheses

If your arrow functions takes exactly one parameter, you may omit the wrapping parentheses.

Instead of

(userName) => { ... }
you could write

userName => { ... }
Please note: 

If your function takes no parameters, parentheses must not be omitted - () => { ... } is the only correct form in that case.

If your function takes more than one parameter, you also must not omit parentheses - userName, userAge => { ... } would be invalid ((userName, userAge) => { ... } is correct)!

2) Omitting function body curly braces

If your arrow function contains no other logic but a return statement, you may omit the curly braces and the return keyword.

Instead of

number => { 
  return number * 3;
}
you could write

number => number * 3;
The following code would be invalid:

number => return number * 3; // invalid because the return keyword must also be omitted!
number => if (number === 2) { return 5 }; // invalid because if statements can't be returned
3) Special case: Just returning an object

If you go for the shorter alternative explained in 2) and you're trying to return a JavaScript object, you may end up with the following, invalid code:

number => { age: number }; // trying to return an object
This code would be invalid because JavaScript treats the curly braces as function body wrappers (not as code that creates a JS object).

To "tell" JavaScript that an object should be created (and returned) instead, the code would need to be adjusted like this:

number => ({ age: number }); // wrapping the object in extra parentheses
By wrapping the object and its curly braces with an extra pair of parentheses, JavaScript understands that the curly braces are not there to define a function body but instead to create an object. Hence that object then gets returned.

# REVISITING Objct & Class 
# Arrays & Array method like Map()
# Distruchering
## Destructuring in Function Parameter Lists
The destructuring syntax explained in the previous lecture can also be used in function parameter lists.

For example, if a function accepts a parameter that will contain an object it can be destructured to "pull out" the object properties and make them available as locally scoped variables (i.e., variables only available inside the function body).

Here's an example:

function storeOrder(order) {
  localStorage.setItem('id', order.id);
  localStorage.setItem('currency', order.currency);
}
Instead of accessing the order properties via the "dot notation" inside the storeOrder function body, you could use destructuring like this:

function storeOrder({id, currency}) { // destructuring
  localStorage.setItem('id', id);
  localStorage.setItem('currency', currency);
}
The destructuring syntax is the same as taught in the previous lecture - just without creating a constant or variable manually.

Instead, id and currency are "pulled out" of the incoming object (i.e., the object passed as an argument to storeOrder).

It's very important to understand, that storeOrder still only takes one parameter in this example! It does not accept two parameters. Instead, it's one single parameter - an object which then just is destructured internally.

The function would still be called like this:

storeOrder({id: 5, currency: 'USD', amount: 15.99}); // one argument / value!

# Spread operator
# Revisiting Control statement 
# Manipulating The DOM
# Using function as a value.
```
function greeter(greentFn){
    greentFn();
}
greeter(() => console.log("Hi"));
```
# Defining Function Inside of Function
```

function init(){
   function greet(){
 console.log("T&T");
}
grret();
}
greet();// u can not access outside the function it is valid only inside the function.
init(); you can access
```
# Refrance Vs primative Value
# React Section
# React Module introduction
Component -Driven user interface
Building Interactive * Scalable UIs
1) React Core Syntax & JSX
2) working with Components
3) Working with Data 
> Q What is a Component?
> 1) Reusability 2) Separation of Concerns
> Q How ia A Component Built? -> HTML CSS JS


## Extention required to React js Project
1) preitte 
2)

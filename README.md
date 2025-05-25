# JAVASCRIPT FUNDAMENTALS #

Javascript is giving instructions to a computer.
It is case sensitive.

## Common commands ##

alert() -> popup in a website
    example: alert('Good job);
document.body.innerHTML= 'Hello'; -> Removes everything on the page and replaces with the text 'Hello'
   (Modifying the page)
console.log(); -> text inside the brackets is displayed in the console.
typeof() -> tells what type a value is.
Math.round() -> rounds of a number to the nearest integer.
Math.random() -> generates a random number between 0 and 1.

SYNTAX- refers to rules that we have to follow when using a programming language.

## order of operation ##

1. (...)        -> have the highest priority
2. multiplication * , division /
3. addition + , subtruction -
4. Comparison operators
5. logical operators  -> have the lowest priority

CONCATENATION - refers to combining strings together.
    example: 'items('+( 1 + 1) + '): $' + (2095 + 779) / 100
    results in: 'items(2): $28.74'
Type Coercion -> is the automatic type conversion.
    ie. 'hello' + 3 = 'hello3' =>3 is converted into a string.
Character -> 1 letter, number or symbol.
Escape characters => they are: \' , \" , and \n

## 3 ways to create a string ##

1. '... '  single quotes
2. "...."  double quotes
3. `...`   back ticks  (template string) also for multi-line string
    example: `some
              text`  => results in => 'some\ntext'

INTERPOLATION- inserting value directly into a string using: ${} 
    example: `Items (${ 1+ 1}): $${(2095 + 799) / 100}`
    results in: 'Items (2): $28.94'

NESTING - elements inside an element.
-Multiple spaces are combineed into 1 space in a webpage.
-Webpage is a single page in a website eg. Home page & Cart page, altogether called a website.

TOOLTIP - HTML attribute eg. 
    <button title="Good job!">Hello</button>
    -it shows up when you hover over your mouse on a button.

## VARIABLES ##

 It is like a container. We can save a value in it and use it later.
 Variables are created by using the word let, const or var.
 let is the most common, while const makes our code safer and easier to understand. Just like let, var also creates a variable that can be changed.

 ### Variable name restrictions ###

 1. Can't use special names like 'let'.
 2. Can't start with a number.
 3. Can't use special characters except: $_

SCOPE => limits where a variable exists. Any variable created inside the curly brackets {...} will only exist inside the curly brackets.
 -Scope helps us avoid naming conflicts.
 -var doesn't follow the rules of scope, thus we use let and const.

## Naming Convention ##

 1. camelCase eg. cartQuantity (common in JS).
 2. PascalCase eg. CartQuantity (works in only one case in JS).
 3. kebab-case eg. cart-quantity (doesn't work in JS).
 4. snake_case eg. cart_guantity (not used in JS).

## BOOLEANS ## 

 (true , false) they represent whether something is true or false. 
 Note: No quotes around them!

-Logical operators help us combine boolean values. 
 && (and operator) => Both sides should be true.
 || (Or operator) => At least one side should be true.
 ! (Not operator)=> Uses only one boolean value and flips it into the opposite value.

 ### truthy and falsy values ###

 -Used as shortcut in our code.
 falsy values  => false, 0 , ' ' , NaN, undefined, null.
 All the other numbers and words are truthy values.
 - We get 'NaN' (Not A Number) if we do some invalid math like: console.log('text' / 5);
  -Undefined - something doesn't have a value.
    let variable1;
    console.log(variable1);
 Note: this syntax can only be used with let. when you use const it will result in an error.
 -null and undefined work in the same way in most cases but we use null when we INTENTIONALLY want something to be empty.

## If statements ##

 -Lets us write multiple groups of code then decide which code to run.
 syntax:
    If (boolean value) {
        ..condition..
    } else {
        ...
    }
 
 ### Shortcuts for if-statements ###

 1. Ternary operator ?:
 2. Guard operator &&
 3. Default operator ||

## FUNCTIONS ##

 -a function lets us reuse code.
 Rules for functions are similar to variable names restrictions above.
 syntax:
    function function1() {
        console.log('hello');
        console.log(2 + 2);
    }
    function1();  => calling/running/executing the function.

 -By reusing code, our code becomes a lot cleaner by removing all the duplication thus makes it easier to update our code (inside the function).
 * Return statement - lets us get a value OUT of a function.
 When we use return statement, it ends the function immediately.
 * Parameters -puts a value INTO a function. (opposite of functions)
 Parameter nammes follow same rules as variable names.
 A parameter only exists inside the function's scope.
 A function can have more than one parameter.

## OBJECTS ##

 -An object groups multiple values together.
    console.log(product2.name);   => dot notation
    console.log(product2['name']); => bracket notation. Lets us use properties that don't work with dot notation.
        example: console.log(product2['delivery-time']);  because javascript thinks it is a minus sign if we use dot notation thus results in an error.

-Destructuring is an easier way to take properties out of an object.

## METHOD ##

 -It is a function inside an object.
 Object + Function = Method eg. Math.random(), console.log().
 Built-in objects - are provided by the language. They are: console, Math, JSON, local storage.

 * JSON - helps us work with JSON (Javascript Object Notation). It is a syntax similar to Javascript object, but has less features.
 In JSON, all properties and strings must use double quotes. It also doesn't support functions.
 The syntax to Javascript object only makes sense in Javascript while Json syntax can be understood by almost every programming language.
 We use Json when: 1. We send data between computers.
                   2. We store data.
 *Built-in Json object  converts Javascript object to Json.
 *JSON.parse() converts JSON to Javascript object.

 * local storage - stores values more permanently and only supports strings.

 AUTO-BOXING - eg. console.log('hello'.length);
                   console.log('hello'.toUpperCase);

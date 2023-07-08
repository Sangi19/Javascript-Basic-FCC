# Javascript-Basic-FCC
Derived important Basic notes of Javascript from Free Code Camp Learning.


<h1 align="center"> FCC-Javascript Basics </h1>

## Getting Started
-   javascript comments:
    -   Comments are lines of code that JavaScript will intentionally ignore.
    -   // This is an in-line comment.
    -   /* This is a multi-line comment */
-   Data Types:
    -   JavaScript provides eight different data types which are undefined, null, boolean, string, symbol, bigint, number, and object.
    -   When JavaScript variables are declared, they have an initial value of undefined.
    -   If we do a mathematical operation on an undefined variable your result will be NaN which means "Not a Number".
    -   If we concatenate a string with an undefined variable, you will get a string of undefined.
    -   with the var keyword is that you can easily overwrite variable declarations:var camper = "James"; var camper = "David"; 
-   why use 'let' instead of 'var':
    -    unlike var, when you use let, a variable with the same name can only be declared once.
-   var:
    -   We should always name variables you don't want to reassign using the const keyword. This helps when you accidentally attempt to reassign a variable that is meant to stay constant.
    -   Use let when you want the variable to change.
    -   const when you want the variable to remain constant.
    -   '+' symbol as an addition operator when placed between two numbers
    -   '-' symbol for subtraction.
    -   '*' symbol for multiplication of two numbers.
    -   '/' symbol for division.
    -   You can easily increment or add one to a variable with the ++ operator.
    -   backslash (\\) is used when we need a quoted string inside a string.
    -   when you need a literal quote: " or ' inside of your string, at the end of string quote by placing a backslash (\).
    -   when the + operator is used with a String value, it is called the concatenation operator.
    -   Access Array Data with Indexes; We can access the data inside arrays using indexes.
        -   Unlike strings, the entries of arrays are mutable and can be changed freely, even if the array was declared with const.
    -   Access Multi-Dimensional Arrays With Indexes:
        -   One way to think of a multi-dimensional array, is as an array of arrays.
    -   Array methods:
        -   An easy way to append data to the end of an array is via the push() function.
        -   .pop() is used to pop a value off of the end of an array
        -   .unshift() always removes the first element of an array. 
        -   .shift()
        -
        local scope:
        - Variables which are declared within a function, as well as the function parameters, have local scope. That means they are only visible within that function.  
        -   we can take the return value of a function and assign it to a variable. > ourSum = sum(5, 12);
        -   assignment (=), which assigns the value on the right of the operator to a variable on the left.
        -   The equality operator (==) compares two values and returns true if they're equivalent or false if they are not.
        -   Type Coercion: In order for JavaScript to compare two different data types (for example, numbers and strings), it must convert one type to another. Here 1=='1' is true. This operator attempts to convert both values being compared to a common type(type conversion).
        -   Strict equality (===) doesn't use type conversion.If the values being compared have different types, they are considered unequal, and the strict equality operator will return false.
        -   Operators :
            -   the Assignment operator "=," - Assignment operator assigns values to a variable.
            -   Loose Equality operator "==" and Assignment operator assigns values to a variable.
            -   Strict Equality operator "===" operators.the two variables having the same data type, then it returns a "true,""
            -   The inequality operator (!=) is the opposite of the equality operator.
            -   The strict inequality operator (!==) is the logical opposite of the strict equality operator. The strict inequality operator will not convert data types.
            -   The greater than operator (>) compares the values of two numbers.If the number to the left is greater than the number to the right, it returns true. the greater than operator will convert data types of values while comparing. Eg: 3>'3' // true.
            -   The logical and operator (&&) returns true if both of the operands are true.
            -   The logical or operator (||) returns true if either of the operands is true.
            -   The .hasOwnProperty() method : To check if a property on a given object exists or not. Syntax: object.hasOwnProperty(property)
            -    Recursion is the concept that a function can be expressed in terms of itself.
            

<h1 align="center"> ES6 </h1>

### Prevent Object Mutation:
-   To ensure your data doesn't change, JavaScript provides a function Object.freeze to prevent data mutation.
-   Any attempt at changing the object will be rejected, with an error thrown if the script is running in strict mode.
-   ex: Object.freeze(MATH_CONSTANTS)
### Use Arrow Functions to Write Concise Anonymous Functions:
-   when passing a function as an argument to another function, we create inline functions (anonymous functions).
-   With ES6, arrow function syntax allows you to omit the keywords 'function' & 'return' as well as the brackets surrounding the code. 
### Write Arrow Functions with Parameters:
-   Just like a regular function, you can pass arguments into an arrow function.
-   const doubler = (item) => item * 2;
### Set Default Parameters for Your Functions
-    ES6 introduces default parameters for function tocreate more flexible functions.
-   The default parameter kicks in when the argument is not specified (it is undefined).
### Use the Rest Parameter with Function Parameters:
-   ES6 introduces the spread operator, which allows us to expand arrays and other expressions in places where multiple parameters or elements are expected. ex: arr2 = [...arr1]; 
-   the spread operator only works in-place, like in an argument to a function or in an array literal.
### Use Destructuring Assignment to Extract Values from Objects:
-   Destructuring assignment is special syntax introduced in ES6, for neatly assigning values taken directly from an object.
-   ES5: 
    -   const user = { name: 'John Doe', age: 34 };
    -   const name = user.name;
    -   const age = user.age;
- ES6:
    -   const { name, age } = user;
    -   Here, the name and age variables will be created and assigned the values of their respective values from the user object. 
-  destructure values from nested objects:
    -   const { johnDoe: { age, email }} = user;
    -   we assign the variables lowToday and highToday the values of today.low and today.high from the LOCAL_FORECAST object.
    -   const {today:{low:lowToday, high:highToday}}=LOCAL_FORECAST
### Use Destructuring Assignment to Assign Variables from Arrays
-   Destructuring an array is the best way to choose which elements you want to assign to variables.
-   spread operator unpacks all contents of an array into a comma-separated list where we can't choose which elements you want to assign . 
-   let a = 8, b = 6;
-   [b,a]=[a,b] //values have been swapped.

### Destructuring via rest elements
-   const [a, b, ...arr] = [1, 2, 3, 4, 5, 7]; a, b values and arr values respectively 1, 2 and [3, 4, 5, 7].

### Template Literals:
-   a special type of string that makes creating complex strings easier/
-   We use it to create multi-line strings and to use string interpolation features to create strings.
    -   const greeting = `Hello, my name is ${person.name}! and I am ${person.age} years old.`;
### Object Literal Declarations Using Object Property Shorthand:
-   Using object property shorthand with object literals to create and return an object x,y
-   const getMousePosition = (x, y) => ({ x, y });
### Concise Declarative Functions with ES6:
    -   const person = {
            name: "Taylor",
            sayHello: function() {
                return `Hello! My name is ${this.name}.`;
            }
        };
    -   const person = {
            name: "Taylor",
            sayHello() {
                return `Hello! My name is ${this.name}.`;
            }
        };
### Create a Module Script:
    -   A script that uses this module type can now use the import and export features
    -   <script type="module" src="filename.js"></script>
### Use export to Share a Code Block (named export)
-   When you export a variable or function, you can import it in another file and use it without having to rewrite the code
        -   export const add = (x, y) => {return x + y;}   
        -   export { add, subtract };
### Reuse JavaScript Code Using import:
-   import allows you to choose which parts of a file or module to load.
-   The exported file can be used by importing them in the another file.
        -   import { add, subtract } from './math_functions.js';
-   To import all the contents from the file we can use the below.
        -   import * as myMathModule from "./math_functions.js";
### export default:
-   This is used to create a fallback value for a file or module.
        -   export default function add(x, y) {return x + y;}
### Create a JavaScript Promise:
-   As the name says, we use it to make a promise to do something, usually asynchronously.
-   When the task completes, you either fulfill your promise or fail to do so.
-   Promise is a constructor function, so you need to use the new keyword to create one.
        -   const myPromise = new Promise((resolve, reject) => { });   
-   A promise has three states: pending, fulfilled, and rejected.
### Handle a Fulfilled Promise with then
-   Promises are most useful when you have a process that takes an unknown amount of time in your code (i.e. something asynchronous), often a server request
-    The 'then' method is executed immediately after your promise is 'fulfilled' with resolve.
        -   myPromise.then(result => { });
        -   result comes from the argument given to the resolve method.
-   The 'catch' is the method used when your promise has been 'rejected'.
        -   myPromise.catch(error => { });
        -   error is the argument passed in to the reject method.

<h1 align="center"> Regular Expressions </h1>

<p>Regular expressions, often shortened to "regex" or "regexp", are patterns that help programmers match, search, and replace text. Regular expressions are very powerful, but can be hard to read because they use special characters to make more complex, flexible matches.</p>

### Match Literal Strings

-   Regular expressions are used in programming languages to match parts of strings. You create patterns to help you do that matching.
        -   let testStr = "freeCodeCamp";
        -   let testRegex = /Code/;
        -   testRegex.test(testStr); //returns true
        -   the regex /Kevin/ will not match kevin or KEVIN.
### Match a Literal String with Different Possibilities
    -   We can search for more than just two patterns. You can do this by adding more patterns with more OR operators separating them, like /yes|no|maybe/. let petRegex = /dog|cat|bird|fish/; 
### Ignore Case While Matching - case insensitive flag (i)
    -   the i flag- This regex can match the strings with different cases.
        -   let myString = "freeCodeCamp";
        -   let fccRegex = /freecOdecamp/i; // 
        -   let result = fccRegex.test(myString);
    -   We can extract the actual matches you found with the .match() method.
        -   "Hello, World!".match(/Hello/);
        
- FYI:    
    -   'string'.match(/regex/);
    -   /regex/.test('string');
    -   To search or extract a pattern more than once, you can use the global search flag: g.
    -   'string'.match(/regex/gi); - To serach the pattern globally.
### Match Anything with Wildcard Period
-   The wildcard character . will match any one character. The wildcard is also called dot and period.
-   /hu./.test("hum") // result will be true.
### Match Letters of the Alphabet

Inside a character set, you can define a range of characters to match using a hyphen character: -.
let bgRegex = /[a-e]at/;

### Match Numbers and Letters of the Alphabet
- /[0-5]/ matches any number between 0 and 5, including the 0 and 5. 
### Match Single Characters Not Specified

-  create a set of characters that you do not want to match. These types of character sets are called negated character sets.
-   caret character (^) - /[^aeiou]/gi matches all characters that are not a vowel
### Match Characters that Occur One or More Times
- a single match in 'aabc' and return ["aa"]. ex: 'aa'.match(/[a+]/gi)
- the character(+) has to repeat one after the other 

### Find character with lazy matching
- There's also an option that matches characters that occur zero or more times. (asterisk or star: *)
- Aaaaaaaaaaaaaaaarrrgh.match(/Aa*/g)

### Find one or more Char
-  a greedy match finds the longest possible part of a string that fits the regex pattern and returns it as a match. 
-  The alternative is called a lazy match, which finds the smallest possible part of the string that satisfies the regex pattern.
- ? character to change it to lazy matching./t[a-z]*?i/ returns ["ti"]. in greeedy match 'cdeCCCC'.match(/E+/g) returns =CCCC
### Match Beginning String Patterns
- we  used the caret character (^) inside a character set to create a negated character set in the form [^thingsThatWillNotBeMatched]
-   Outside of a character set, the caret is used to search for patterns at the beginning of strings.
- /^Ricky/.test("You can't find Ricky now.") // returns false.
### Match Ending String Patterns
-You can search the end of strings using the dollar sign character $ at the end of the regex.
- /story$/

### Match to find alphaNumeric characters:
-The closest character class in JavaScript to match the alphabet is \w.This shortcut is equal to [A-Za-z0-9_]
-/[A-Za-z0-9_]+/ === /\w+/
-to count the number of alphanumeric characters /\w/g match.
### Match Everything But Letters and Numbers
- count the number of non-alphanumeric characters in various quotes (/\W/)
### Match All Numbers
-The shortcut to look for digit characters is \d. (/\d/g)
### Match All Non-Numbers
-The shortcut to look for non-digit characters is \D. 
### Match Whitespace
-You can search for whitespace using \s,  also search for carriage return, tab, form feed, and new line charactersas like  [ \r\t\f\n\v].
-ex: /\s/
### Match Non-Whitespace Characters
- You can also search for everything except whitespace with this. ex: /\S/g

### Specify Upper and Lower Number of Matches
the plus sign + to look for one or more characters 
the asterisk * to look for zero or more characters.
to match only the letter a appearing between 3 and 5 times in the string ah, your regex would be /a{3,5}h/.
### Specify Upper and Lower Number of Matches
-Change the regex ohRegex to match the entire phrase Oh no only when it has 3 to 6 letter h's.
-/Oh{3,6}\sno/.test("Ohhh no")
### Specify Only the Lower Number of Matches
-We only want to specify the lower number of patterns with no upper limit.
- to match only the string hah with the letter a appearing at least 3 times, your regex would be /ha{3,}h/.
### Specify Exact Number of Matches
-Sometimes you only want a specific number of matches.
-to match only the word hah with the letter a 3 times, your regex would be /ha{3}h/
- /colou?r/.test("color") //true
### Positive and Negative Lookahead
- useful when you want to search for multiple patterns over the same string.
    - let quit = "qu";
    - let noquit = "qt";
    - let quRegex= /q(?=u)/;
    - let qRegex = /q(?!u)/;
    - quit.match(quRegex);
    - noquit.match(qRegex);
    EX: /(?=\w{3,6})(?=\D*\d)/.test("abc123")
    /(?=\w{6})(?=\w*\d{2})/.test("astronaut")
###     Check For Mixed Grouping of Characters
- to check for groups of characters,we use parentheses ().
- creating regex so that it checks for the names of Franklin Roosevelt or Eleanor Roosevelt in a case sensitive manner and it should make concessions for middle names.
- EX: /(Franklin|Eleanor) (([A-Z]\.?|[A-Z][a-z]+) )?Roosevelt/.test( "Eleanor Roosevelt")
### Reuse Patterns Using Capture Groups
- capture groups can be used to find repeated substrings.
- to capture a word consisting of alphanumeric characters : /(\w+)/.
    - let repeatStr = "row row row your boat";
    - let repeatRegex = /(\w+) \1 \1/;
    - repeatRegex.test(repeatStr); // Returns true
    - repeatStr.match(repeatRegex); // Returns ["row row row", "row"]
- Using the .match() method on a string will return an array with the matched substring, along with its captured groups.
- Use capture groups in reRegex to match a string that consists of only the same number repeated exactly three times separated by single spaces. EX: /^(\d+) \1 \1$/.test( "42 42 42") 
### Use Capture Groups to Search and Replace
-  access capture groups in the replacement string with dollar signs ($).
- "Code Camp".replace(/(\w+)\s(\w+)/, '$2 $1'); // Camp Code.
### Remove Whitespace from Start and End
- Write a regex to remove whitespace at the beginning and end of strings.
- EX: "   Hello, World!  ".replace(/^\s+|\s+$/g, "")

<h1 align="center"> Debugging </h1>
### Use the JavaScript Console to Check the Value of a Variable
- to print the string Hello world! to the console:
    -   console.log('Hello world!');
- There are many methods to use with console to output messages. log, warn, and clear to name a few.
### Use typeof to Check the Type of a Variable
-   You can use typeof to check the data structure, or type, of a variable.
        -   console.log(typeof "");-string
### Catch Misspelled Variable and Function Names
- The console.log() and typeof methods are the two primary ways to check intermediate values and types of program output. 
### Catch Use of Assignment Operator Instead of Equality Operator
-   to assign a value to the variable use = operator and while checking the equality of the two, we should use === operator.
### Catch Arguments Passed in the Wrong Order When Calling a Function
-   on calling functions, the next bug to watch out for is when a function's arguments are supplied in the incorrect order
### Catch Off By One Errors When Using Indexing
- JavaScript indexing starts at zero, not one.
- If we try to access an index equal to the length, the program may throw an "index out of range" reference error or print undefined.
### Prevent Infinite Loops with a Valid Terminal Condition
- This topic is the dreaded infinite loop.

## Basic Data Structures
<h1 align="center"> Basic Data Structures </h1>
<p>Data can be stored and accessed in many ways. You already know some common JavaScript data structures — arrays and objects.
We will learn more about the differences between arrays and objects, and which to use in different situations. 
We'll also learn how to use helpful JS methods like splice() and Object.keys() to access and manipulate data.
</p>

### Use an Array to Store a Collection of Data
-   one-dimensional array, meaning it only has one level, or that it does not have any other arrays nested within it
    -   let simpleArray = ['one', 2, 'three', true, false, undefined, null];
-   multi-dimensional array, or an array that contains other arrays.  this array also contains JavaScript objects
-   arrays are also capable of storing complex objects.
### Access an Array's Contents Using Bracket Notation
-   In an array, each array item has an index. JavaScript arrays are zero-indexed.
-    We use bracket notation to access an item fro0m the array.

### Add Items to an Array with push() and unshift()
- the push() method adds elements to the end of an array, and unshift() adds elements to the beginning.
### Remove Items from an Array with pop() and shift()
- We can also return the value of the removed element with either method like this:
        - let popped = greetings.pop();
### Remove Items Using splice()
We use splice() method 
-  to remove an element from somewhere in the middle
-  to remove more than one element at once
-  remove any number of consecutive elements from anywhere in an array.
    - array.splice(index, no of element to remove);
-   splice() modifies the array, it also returns a new array containing the value of the removed elements:
    - let newArray = array.splice(3, 2); // contains 2 elements from 3rd index
- the third parameter, comprised of one or more element(s), to add to the array.
    -   numbers.splice(startIndex, amountToDelete, 13, 14);
### Copy Array Items Using slice()
-  slice() takes only 2 parameters — the first is the index at which to begin extraction, and the second is the index at which to stop extraction
    -   let newArr = arr.slice(startIndex, endingIndex); //ending Index will be excluded.
### Copy an Array with the Spread Operator
- spread operator has the ability to combine arrays, or to insert all the elements of one array into another, at any index    
    - let thatArray = ['basil', 'cilantro', ...thisArray, 'coriander'];
### Check For The Presence of an Element With indexOf()
-   indexOf() takes an element as a parameter, and when called, it returns the position, or index, of that element, or -1 if the element does not exist on the array.
-   arrray.indexOf(element) // returns -1 of the element is not present in the array, otherwise will return its index position.
### Iterate Through All an Array's Items Using For Loops
- we can also use Each(), forEach(), map() methods but for loop will give the all possibilities to work on.
- Add Key-Value Pairs to JavaScript Objects



## Built by

👤 **Sangeetha Ramkumar**

- [LinkedIn](https://www.linkedin.com/in/sangeetharamkumar)
- [GitHub](https://github.com/Sangi19)
- [E-mail](sangiammu1020@gmail.com)

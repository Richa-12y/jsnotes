
# JavaScript Date Methods Cheat Sheet

JavaScript provides a robust set of methods for working with dates through the `Date` object. This cheat sheet outlines some of the most commonly used methods along with examples of their usage.

## Creating a Date Object

```javascript
new Date(): // Creates a new Date object representing the current date and time.
const currentDate = new Date();
console.log(currentDate);

Getting Different Components of a Date

getDate(): // Returns the day of the month (1-31).
getMonth(): // Returns the month (0-11).
getFullYear(): // Returns the year (4 digits).
getDay(): // Returns the day of the week (0-6).
Example:


const date = new Date();
const day = date.getDate();
const month = date.getMonth() + 1; // Note: Month is zero-indexed
const year = date.getFullYear();
const dayOfWeek = date.getDay(); // 0 is Sunday, 1 is Monday, and so on

console.log(`Today is ${day}/${month}/${year}, which is a ${dayOfWeek}`);
Setting Different Components of a Date

setDate(): // Sets the day of the month (1-31).
setMonth(): // Sets the month (0-11).
setFullYear(): // Sets the year (4 digits).
Example:


const date = new Date();
date.setDate(15); // Sets the date to the 15th
date.setMonth(11); // Sets the month to December (remember: zero-indexed)
date.setFullYear(2025); // Sets the year to 2025

console.log(date);
Formatting Date to String

toDateString(): // Returns the date portion of a Date object as a human-readable string.
toISOString(): // Returns a string in simplified extended ISO format.
Example:


const date = new Date();
console.log(date.toDateString());
console.log(date.toISOString());
Calculating Differences Between Dates

getTime(): // Returns the numeric value corresponding to the time for the specified date according to universal time.

Example:


const date1 = new Date('2024-01-01');
const date2 = new Date('2024-12-31');
const differenceInMilliseconds = Math.abs(date2.getTime() - date1.getTime());
const differenceInDays = Math.ceil(differenceInMilliseconds / (1000 * 60 * 60 * 24));

console.log(`There are ${differenceInDays} days between ${date1.toDateString()} and ${date2.toDateString()}`);
These methods provide a foundational understanding of how to manipulate dates in JavaScript. For more specific use cases, consult the JavaScript documentation for additional methods and functionalities.

----
JavaScript's Math object provides a set of methods for performing mathematical operations. Here are some of the commonly used methods along with explanations and examples:

Math.abs(): Returns the absolute value of a number.


console.log(Math.abs(-5)); // Output: 5
Math.ceil(): Rounds a number up to the nearest integer.


console.log(Math.ceil(4.3)); // Output: 5
Math.floor(): Rounds a number down to the nearest integer.


console.log(Math.floor(4.7)); // Output: 4
Math.round(): Rounds a number to the nearest integer.


console.log(Math.round(4.5)); // Output: 5
console.log(Math.round(4.2)); // Output: 4
Math.max(): Returns the largest of zero or more numbers.


console.log(Math.max(10, 20, 30)); // Output: 30
Math.min(): Returns the smallest of zero or more numbers.


console.log(Math.min(10, 20, 30)); // Output: 10
Math.pow(): Returns the base to the exponent power, that is, base^exponent.


console.log(Math.pow(2, 3)); // Output: 8 (2 to the power of 3)
Math.sqrt(): Returns the square root of a number.


console.log(Math.sqrt(25)); // Output: 5
Math.random(): Returns a pseudo-random number between 0 and 1.


console.log(Math.random()); // Output: a random number between 0 and 1
Math.sin(), Math.cos(), Math.tan(): Trigonometric methods to calculate sine, cosine, and tangent of an angle (in radians).


const angleInRadians = Math.PI / 4; // 45 degrees
console.log(Math.sin(angleInRadians)); // Output: approximately 0.7071
console.log(Math.cos(angleInRadians)); // Output: approximately 0.7071
console.log(Math.tan(angleInRadians)); // Output: approximately 1

 These are some of the methods provided by the Math object in JavaScript. They are useful for performing various mathematical calculations in your code.


Certainly! JavaScript provides the Math.random() method to generate pseudo-random numbers between 0 (inclusive) and 1 (exclusive). You can use this method to create random numbers for various purposes, such as games, simulations, or randomized algorithms. Here's how you can use Math.random() with examples:

Generating Random Floating-Point Numbers between 0 and 1:


const randomNumber = Math.random();
console.log(randomNumber); // Output: a random number between 0 (inclusive) and 1 (exclusive)
Generating Random Integers within a Range:
To generate random integers within a specific range, you can use Math.floor() or Math.ceil() along with Math.random().


// To generate a random integer between min (inclusive) and max (inclusive)
function getRandomInteger(min, max) {
    return Math.floor(Math.random() * (max - min + 1)) + min;
}

const min = 1;
const max = 100;
const randomInteger = getRandomInteger(min, max);
console.log(randomInteger); // Output: a random integer between 1 and 100
Generating Random Choices from an Array:
You can use Math.random() to randomly select an element from an array.


const choices = ['apple', 'banana', 'orange', 'grape', 'kiwi'];
const randomIndex = Math.floor(Math.random() * choices.length);
const randomChoice = choices[randomIndex];
console.log(randomChoice); // Output: a random element from the array
Shuffling an Array:
You can shuffle an array randomly using Math.random() to reorder its elements.


function shuffleArray(array) {
    for (let i = array.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [array[i], array[j]] = [array[j], array[i]];
    }
    return array;
}

const originalArray = [1, 2, 3, 4, 5];
const shuffledArray = shuffleArray(originalArray.slice()); // Using slice to create a copy of the original array
console.log(shuffledArray); // Output: the original array shuffled randomly
These examples demonstrate how you can utilize Math.random() to generate random numbers, select random elements, and shuffle arrays in JavaScript.


JavaScript Booleans with example
In JavaScript, a Boolean is a data type that can have one of two values: true or false. Booleans are often used in conditional statements, loops, and other control structures to determine the flow of execution in a program. Here's an explanation of JavaScript Booleans with examples:

Boolean Values:

true: Represents a true condition.
false: Represents a false condition.
Creating Boolean Variables:
You can create Boolean variables directly by assigning either true or false to them.


let isTrue = true;
let isFalse = false;

console.log(isTrue); // Output: true
console.log(isFalse); // Output: false
Boolean Expressions:
Boolean expressions are expressions that evaluate to either true or false.


const age = 25;
const isAdult = age >= 18; // Evaluates to true if age is 18 or older
console.log(isAdult); // Output: true

const isTeenager = age >= 13 && age <= 19; // Evaluates to true if age is between 13 and 19
console.log(isTeenager); // Output: true
Boolean Operators:
JavaScript provides several operators for working with Boolean values:

Logical AND (&&): Returns true if both operands are true, otherwise false.
Logical OR (||): Returns true if at least one of the operands is true, otherwise false.
Logical NOT (!): Returns the opposite Boolean value of the operand.
javascript
Copy code
const isRaining = true;
const isCold = false;

// Logical AND
const takeUmbrella = isRaining && !isCold; // Only take an umbrella if it's raining and not cold
console.log(takeUmbrella); // Output: true

// Logical OR
const wearCoat = isRaining || isCold; // Wear a coat if it's raining or cold
console.log(wearCoat); // Output: true

// Logical NOT
const isNotRaining = !isRaining; // Opposite of isRaining
console.log(isNotRaining); // Output: false
Truthy and Falsy Values:
In JavaScript, values that are not false, undefined, null, 0, NaN, or an empty string ("") are considered truthy. All other values are considered falsy.


const truthyValue = "Hello";
const falsyValue = 0;

console.log(Boolean(truthyValue)); // Output: true
console.log(Boolean(falsyValue)); // Output: false
Booleans are fundamental in programming and are extensively used for making decisions and controlling the flow of execution in JavaScript programs.


JavaScript Sets with exmaple
In JavaScript, a Set is a collection of unique values, where each value may occur only once. Sets can be used to efficiently store and manage a collection of distinct elements. Here's an explanation of JavaScript Sets with examples:

Creating a Set:
You can create a Set using the new Set() constructor and passing an iterable object like an array or another Set.


const mySet = new Set(); // Creating an empty Set
const numbers = new Set([1, 2, 3, 4, 5]); // Creating a Set with initial values
Adding and Removing Elements:

add(value): Adds a new element to the Set. If the element already exists, it won't be added again.
delete(value): Removes the specified element from the Set.
clear(): Removes all elements from the Set.

const mySet = new Set();
mySet.add(1);
mySet.add(2);
mySet.add(3);
mySet.add(2); // This won't add another 2, as Sets only allow unique values
console.log(mySet); // Output: Set(3) { 1, 2, 3 }

mySet.delete(2);
console.log(mySet); // Output: Set(2) { 1, 3 }

mySet.clear();
console.log(mySet); // Output: Set(0) {}
Checking if an Element Exists:

has(value): Returns true if the Set contains the specified element, otherwise false.

const mySet = new Set([1, 2, 3]);
console.log(mySet.has(2)); // Output: true
console.log(mySet.has(4)); // Output: false
Iterating Over a Set:
You can iterate over the elements of a Set using a for...of loop or by using the forEach() method.


const mySet = new Set(['a', 'b', 'c']);

// Using for...of loop
for (const item of mySet) {
    console.log(item);
}

// Using forEach() method
mySet.forEach(item => {
    console.log(item);
});
Set Size:

size: Returns the number of elements in the Set.

const mySet = new Set([1, 2, 3]);
console.log(mySet.size); // Output: 3
Converting Set to Array:
You can convert a Set to an Array using the Array.from() method or the spread operator (...).


const mySet = new Set([1, 2, 3]);
const myArray = Array.from(mySet);
console.log(myArray); // Output: [1, 2, 3]

// Or using spread operator
const newArray = [...mySet];
console.log(newArray); // Output: [1, 2, 3]
Sets are useful when you need to store a collection of unique values and perform operations like adding, removing, and checking for the presence of elements efficiently.


JavaScript Maps with exmaple
ChatGPT
In JavaScript, a Map is a collection of key-value pairs where each key may occur only once. Unlike Objects, Maps can have any data type as a key or value, making them more versatile. Here's an explanation of JavaScript Maps with examples:

Creating a Map:
You can create a Map using the new Map() constructor and passing an iterable object of key-value pairs (such as an array of arrays).


const myMap = new Map(); // Creating an empty Map
const fruits = new Map([
    ['apple', 5],
    ['banana', 3],
    ['orange', 7]
]); // Creating a Map with initial key-value pairs
Adding and Updating Entries:

set(key, value): Sets the value for the specified key in the Map. If the key already exists, its value will be updated.

const myMap = new Map();
myMap.set('apple', 5);
myMap.set('banana', 3);
myMap.set('orange', 7);

myMap.set('apple', 10); // Update the value of 'apple' to 10
console.log(myMap); // Output: Map(3) { 'apple' => 10, 'banana' => 3, 'orange' => 7 }
Getting Values:

get(key): Returns the value associated with the specified key in the Map. Returns undefined if the key doesn't exist.

console.log(myMap.get('banana')); // Output: 3
console.log(myMap.get('grape')); // Output: undefined
Deleting Entries:

delete(key): Removes the entry with the specified key from the Map.

myMap.delete('banana');
console.log(myMap); // Output: Map(2) { 'apple' => 10, 'orange' => 7 }
Checking if an Entry Exists:

has(key): Returns true if the Map contains the specified key, otherwise false.

console.log(myMap.has('apple')); // Output: true
console.log(myMap.has('banana')); // Output: false
Iterating Over a Map:
You can iterate over the entries of a Map using a for...of loop or by using the forEach() method.


for (const [key, value] of myMap) {
    console.log(`${key}: ${value}`);
}

myMap.forEach((value, key) => {
    console.log(`${key}: ${value}`);
});
Map Size:

size: Returns the number of key-value pairs in the Map.

console.log(myMap.size); // Output: 2
Maps are useful for storing key-value pairs and provide methods for efficient retrieval, addition, deletion, and iteration over entries. They are especially handy when you need to store arbitrary data types as keys or values.

JavaScript typeof with exmaple

In JavaScript, the typeof operator is used to determine the type of a variable or expression. It returns a string representing the data type of the operand. Here are examples of using typeof with various data types:

typeof for Numbers:


const num = 42;
console.log(typeof num); // Output: "number"
typeof for Strings:

javascript
Copy code
const str = "Hello, World!";
console.log(typeof str); // Output: "string"
typeof for Booleans:


const bool = true;
console.log(typeof bool); // Output: "boolean"
typeof for Objects:


const obj = { name: "John", age: 30 };
console.log(typeof obj); // Output: "object"
typeof for Arrays:


const arr = [1, 2, 3];
console.log(typeof arr); // Output: "object"
typeof for Functions:


function greet() {
    console.log("Hello!");
}
console.log(typeof greet); // Output: "function"
typeof for Undefined Values:


let undefinedVariable;
console.log(typeof undefinedVariable); // Output: "undefined"
typeof for Null Values:


const nullValue = null;
console.log(typeof nullValue); // Output: "object"
typeof for Symbols:


const sym = Symbol("description");
console.log(typeof sym); // Output: "symbol"
typeof for BigInt:


const bigIntValue = 123n;
console.log(typeof bigIntValue); // Output: "bigint"
It's important to note that typeof null returns "object", which is considered a quirk in JavaScript and not a perfect representation of null's type. Similarly, arrays are also considered objects when using typeof. Additionally, typeof returns "function" for function objects, but not for functions created using arrow syntax (() => {}).

JavaScript Type Conversion
with exmaple
JavaScript performs type conversion automatically when values of different data types are used together in operations or comparisons. This process is also known as type coercion. Here are some examples of type conversion in JavaScript:

Implicit Type Conversion:


const num = 10;
const str = "20";
const result = num + str; // Implicitly converts num to a string and performs concatenation
console.log(result); // Output: "1020"
Explicit Type Conversion:
JavaScript provides functions and methods to explicitly convert values from one type to another:

String(value): Converts the value to a string.
Number(value): Converts the value to a number.
Boolean(value): Converts the value to a boolean.

const num = 10;
const str = "20";
const result = num + Number(str); // Explicitly converts str to a number
console.log(result); // Output: 30
String Conversion:


const num = 10;
const str = String(num); // Converts num to a string
console.log(str); // Output: "10"
Number Conversion:


const str = "20";
const num = Number(str); // Converts str to a number
console.log(num); // Output: 20
Boolean Conversion:


const value = "Hello";
const bool = Boolean(value); // Converts value to a boolean
console.log(bool); // Output: true (non-empty strings are truthy)
Falsy and Truthy Values:
JavaScript has falsy values (which evaluate to false in Boolean context) and truthy values (which evaluate to true in Boolean context).


console.log(Boolean(0)); // Output: false
console.log(Boolean("")); // Output: false
console.log(Boolean(null)); // Output: false
console.log(Boolean(undefined)); // Output: false
console.log(Boolean(NaN)); // Output: false
console.log(Boolean(false)); // Output: false
console.log(Boolean("Hello")); // Output: true
console.log(Boolean(42)); // Output: true
Type conversion is a fundamental concept in JavaScript, and understanding it is crucial for writing robust and predictable code.


teach me JavaScript Regular Expressions

Regular expressions (often abbreviated as regex or regexp) are patterns used to match character combinations in strings. They provide a powerful and flexible way to search, match, and manipulate text. Here's a basic overview of JavaScript regular expressions:

Creating Regular Expressions:
Regular expressions can be created using two methods:

Using a regular expression literal, enclosed in forward slashes (/pattern/).
Using the RegExp constructor.


// Using a regular expression literal
const pattern1 = /hello/;

// Using the RegExp constructor
const pattern2 = new RegExp('world');
Basic Patterns:
Regular expressions can consist of simple characters or special characters with special meanings:

Normal characters match themselves.
Special characters like . (dot), * (asterisk), + (plus), ? (question mark), etc., have special meanings.

const pattern = /hello/;
Matching Strings:
Regular expressions can be used with methods like test() or match() to check if a string matches a pattern.

test(): Returns true if the pattern matches any part of the string, otherwise false.
match(): Returns an array containing the matched substrings, or null if no matches are found.

const pattern = /hello/;
const str = 'hello world';

console.log(pattern.test(str)); // Output: true
console.log(str.match(pattern)); // Output: ['hello']
Flags:
Regular expressions can include optional flags that change how the pattern is matched:

i: Case-insensitive matching.
g: Global matching (find all matches rather than stopping after the first match).
m: Multiline matching.

const pattern = /hello/gi; // Matches 'hello' case-insensitively and globally
Character Classes:
Character classes match specific sets of characters:

[abc]: Matches any character in the set (a, b, or c).
[^abc]: Matches any character not in the set (any character except a, b, or c).
\d: Matches any digit (equivalent to [0-9]).
\w: Matches any word character (alphanumeric character plus underscore).
\s: Matches any whitespace character.

const pattern = /[aeiou]/; // Matches any vowel
Quantifiers:
Quantifiers specify the number of occurrences of the preceding character:

*: Matches zero or more occurrences.
+: Matches one or more occurrences.
?: Matches zero or one occurrence.
{n}: Matches exactly n occurrences.
{n,}: Matches n or more occurrences.
{n,m}: Matches between n and m occurrences.

const pattern = /o+/; // Matches one or more 'o's
Anchors:
Anchors match positions rather than characters:

^: Matches the start of a string.
$: Matches the end of a string.
\b: Matches a word boundary.
\B: Matches a non-word boundary.

const pattern = /^hello/; // Matches 'hello' only if it occurs at the start of the string
Regular expressions are a vast topic with many more features and options. Mastering regular expressions can greatly enhance your ability to manipulate and process text efficiently in JavaScript.


if else,switch,loop for,loop in while break with real time exmaple

1. if...else:

// Real-time example: Checking if a user is eligible to vote based on their age
const age = 20;

if (age >= 18) {
    console.log("You are eligible to vote.");
} else {
    console.log("You are not eligible to vote yet.");
}
2. switch:

// Real-time example: Determining the day of the week based on a number
const dayNumber = 3;
let day;

switch (dayNumber) {
    case 1:
        day = "Monday";
        break;
    case 2:
        day = "Tuesday";
        break;
    case 3:
        day = "Wednesday";
        break;
    // More cases for other days...
    default:
        day = "Invalid day";
}

console.log(`The day is ${day}.`);
3. for Loop:

// Real-time example: Printing numbers from 1 to 5 using a for loop
for (let i = 1; i <= 5; i++) {
    console.log(i);
}
4. while Loop:

// Real-time example: Printing numbers from 1 to 5 using a while loop
let i = 1;
while (i <= 5) {
    console.log(i);
    i++;
}
5. do...while Loop:

// Real-time example: Asking the user to enter a number until they enter a positive number
let num;
do {
    num = prompt("Enter a positive number:");
} while (num <= 0);

console.log(`You entered ${num}.`);
6. break Statement:

// Real-time example: Finding the first even number in an array
const numbers = [1, 3, 5, 8, 9, 10];
let firstEvenNumber;

for (let number of numbers) {
    if (number % 2 === 0) {
        firstEvenNumber = number;
        break; // Exit the loop once the first even number is found
    }
}

console.log(`The first even number is ${firstEvenNumber}.`);
These examples illustrate how if...else, switch, for, while, do...while loops, and the break statement can be used in real-life scenarios to control the flow of your JavaScript programs.


Operator precedence determines the order in which operators are evaluated in an expression. JavaScript follows a specific precedence order, where operators with higher precedence are evaluated first. Here's a summary of JavaScript operator precedence:

Member Access (Left-to-right):

. (dot notation)
[ ] (bracket notation)
Function Call (Left-to-right):

( ) (function invocation)
Postfix Increment/Decrement (Right-to-left):

++ (postfix increment)
-- (postfix decrement)
Logical NOT (Right-to-left):

! (logical NOT)
Unary Plus/Minus (Right-to-left):

+ (unary plus)
- (unary minus)
Multiplication/Division/Remainder (Left-to-right):

* (multiplication)
/ (division)
% (remainder)
Addition/Subtraction (Left-to-right):

+ (addition)
- (subtraction)
Relational Operators (Left-to-right):

<, <= (less than, less than or equal to)
>, >= (greater than, greater than or equal to)
instanceof (instanceof operator)
in (in operator)
Equality Operators (Left-to-right):

==, === (equality)
!=, !== (inequality)
Logical AND (Left-to-right):

&& (logical AND)
Logical OR (Left-to-right):

|| (logical OR)
Conditional (Ternary) Operator (Right-to-left):

? : (conditional)
Assignment Operators (Right-to-left):

=, +=, -=, *=, /=, %= (assignment)
**= (exponentiation assignment)
Let's see a real-time example demonstrating JavaScript operator precedence:

javascript
Copy code
// Real-time example: Using various operators in an expression
const a = 10;
const b = 5;
const c = 2;

const result = a * b + c; // Multiplication (*) has higher precedence than addition (+)

console.log(result); // Output: 52 (10 * 5 + 2 = 52)
In this example, the multiplication operation (*) is evaluated first due to its higher precedence, followed by the addition operation (+). Understanding operator precedence helps ensure that expressions are evaluated correctly in JavaScript.


-- You can create an arrow function to generate a random name using arrays of first names and last names. Here's an example:


const getRandomName = () => {
    const firstNames = ['Alice', 'Bob', 'Charlie', 'David', 'Emma', 'Frank', 'Grace', 'Henry', 'Ivy', 'Jack'];
    const lastNames = ['Smith', 'Johnson', 'Williams', 'Jones', 'Brown', 'Davis', 'Miller', 'Wilson', 'Moore', 'Taylor'];

    const randomFirstNameIndex = Math.floor(Math.random() * firstNames.length);
    const randomLastNameIndex = Math.floor(Math.random() * lastNames.length);

    const randomFirstName = firstNames[randomFirstNameIndex];
    const randomLastName = lastNames[randomLastNameIndex];

    return `${randomFirstName} ${randomLastName}`;
};

// Example usage
console.log(getRandomName()); // Output: e.g., "Grace Taylor"
In this example, the getRandomName arrow function selects a random first name and last name from predefined arrays and combines them to form a random full name. Each time you call getRandomName(), you'll get a different random name.


ChatGPT 3.5

User
teach me JavaScript Errors
Throw, and Try...Catch...Finally with real time exmaple 

let's delve into JavaScript errors and how to handle them using throw, try...catch, and finally.

1. throw Statement:
In JavaScript, you can manually generate errors using the throw statement. This is particularly useful when you encounter a situation where your code cannot proceed due to some unexpected condition. Here's a basic example:

javascript
Copy code
function divide(x, y) {
    if (y === 0) {
        throw new Error("Cannot divide by zero!");
    }
    return x / y;
}

try {
    console.log(divide(10, 0));
} catch (error) {
    console.error("Error caught:", error.message);
}

JavaScript's reduce() method is used to reduce an array to a single value. It executes a reducer function (that you provide) on each element of the array, resulting in a single output value. Here's a simple example to demonstrate how reduce()

const numbers = [1, 2, 3, 4, 5];

const sum = numbers.reduce((accumulator, currentValue) => accumulator + currentValue, 0);

console.log(sum); // Output: 15 (1 + 2 + 3 + 4 + 5)

Here are a few scenarios where you might use reduce():

Calculating Sum, Product, Average, etc.: As demonstrated above, you can use reduce() to calculate the sum, product, average, or any other mathematical operation on an array of numbers.

Flattening Arrays: You can flatten an array of arrays into a single array using reduce(). This is useful when you have nested arrays and you want to work with a single flat array.

Counting Instances: You can count the number of occurrences of each item in an array by using reduce().

Grouping Data: You can group objects in an array based on a certain criteria using reduce(). For example, you might want to group a list of transactions by date.

Data Transformation: You can transform data in an array using reduce(). For example, you can convert an array of strings to an object where each string is a property with a count.

Overall, reduce() is a versatile method that can be used in various scenarios where you need to process an array and produce a single value or a transformed array. It's particularly useful when you need to perform complex operations that can't be easily achieved with other array methods like map() or filter().


1. Flattening Arrays:
---
const nestedArray = [[1, 2], [3, 4], [5, 6]];

const flattenedArray = nestedArray.reduce((accumulator, currentValue) => accumulator.concat(currentValue), []);

console.log(flattenedArray); // Output: [1, 2, 3, 4, 5, 6]
In this example, reduce() is used to flatten the nestedArray into a single array.

2. Counting Instances:
---

const fruits = ['apple', 'banana', 'apple', 'orange', 'banana', 'apple'];

const fruitCount = fruits.reduce((acc, fruit) => {
    acc[fruit] = (acc[fruit] || 0) + 1;
    return acc;
}, {});

console.log(fruitCount);
// Output: { apple: 3, banana: 2, orange: 1 }
Here, reduce() counts the number of occurrences of each fruit in the fruits array and stores them in an object.

3. Grouping Data:
---
const transactions = [
    { id: 1, date: '2024-03-07', amount: 100 },
    { id: 2, date: '2024-03-07', amount: 200 },
    { id: 3, date: '2024-03-06', amount: 300 },
    { id: 4, date: '2024-03-06', amount: 150 },
];

const groupedTransactions = transactions.reduce((acc, transaction) => {
    const date = transaction.date;
    if (!acc[date]) {
        acc[date] = [];
    }
    acc[date].push(transaction);
    return acc;
}, {});

console.log(groupedTransactions);
/*
Output:
{
  '2024-03-07': [
    { id: 1, date: '2024-03-07', amount: 100 },
    { id: 2, date: '2024-03-07', amount: 200 }
  ],
  '2024-03-06': [
    { id: 3, date: '2024-03-06', amount: 300 },
    { id: 4, date: '2024-03-06', amount: 150 }
  ]
}
*/
This example groups transactions by date.

4. Data Transformation:
---
const words = ['apple', 'banana', 'orange', 'grape'];

const wordObject = words.reduce((acc, word) => {
    acc[word] = word.length;
    return acc;
}, {});

console.log(wordObject);
// Output: { apple: 5, banana: 6, orange: 6, grape: 5 }
Here, reduce() transforms the words array into an object where each word is a property and its value is the length of the word.







console.log("Hello, World!");

// Var , let , const

// | Keyword   | Scope             | Can Reassign?      | Can Redeclare? | Hoisted?                     | Real-Life Analogy                                                                                                                                                |
// | --------- | ----------------- | ------------------ | -------------- | ---------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
// | **var**   | Function-scoped   | ✅ Yes              | ✅ Yes          | ✅ Yes                        | 📝 **Classroom Notice Board** → everyone in class (function) can see it, and you can rewrite it multiple times.                                                  |
// | **let**   | Block-scoped `{}` | ✅ Yes              | ❌ No           | ⚠️ Yes (but not initialized) | 📋 **Meeting Room Whiteboard** → only people inside the room (block) can see it, you can erase & update but can’t bring another board with the same name inside. |
// | **const** | Block-scoped `{}` | ❌ No (value fixed) | ❌ No           | ⚠️ Yes (but not initialized) | 📜 **Birth Certificate** → once written, the main info (variable binding) can’t change, though details inside (like address on a file = object) can be updated.  |

// *****VARIABLES*****
// var , let , const
// var is function-scoped (leaks outside block)
if (true) {
  var fruit = "apple";
}
console.log(fruit);  // "apple" (leaked!)




// let is block-scoped
if (true) {
  let fruit = "apple";
  console.log(fruit);  // "apple"
}
console.log(fruit);    // Error: fruit is not defined


// const is block-scoped and cannot be reassigned
const city = "London";
console.log(city);  // "London"

city = "Paris";     // Error: Assignment to constant variable

// var hoisting issue
console.log(color);  // undefined
var color = "blue";
// In JavaScript, "hoisting" means:
// ➡️ Declarations (like var, let, const, functions, and classes) are moved to the top of their scope before execution.


// String
let name = "Alice";
console.log("String:", name);             // Alice
console.log("Type:", typeof name);        // string

// Number
let age = 25;
console.log("Number:", age);              // 25
console.log("Type:", typeof age);         // number

// Boolean
let isStudent = true;
console.log("Boolean:", isStudent);       // true
console.log("Type:", typeof isStudent);   // boolean

// Null
let car = null;
console.log("Null:", car);                // null
console.log("Type:", typeof car);         // object  <-- (historical JS bug)

// Undefined
let city1;
console.log("Undefined:", city1);          // undefined
console.log("Type:", typeof city);        // undefined



let a;           // declared but not assigned → undefined
let b = null;    // explicitly assigned → null

console.log("a:", a);        // undefined
console.log("typeof a:", typeof a); // "undefined"

console.log("b:", b);        // null
console.log("typeof b:", typeof b); // "object" (bug)


// undefined = “JavaScript doesn’t know the value yet.”
// null = “I (the developer) say this should be empty.”

// *****DATATYPES*****

//Primitive datatypes in JavaScript
/*Basic Built in datatypes / defined by language
store actual values , faster less memory 
immutable can not be changed
Number / String / Boolean / Null / Undefined 
*/


//Non primitive datatypes in JavaScript
/* complex datatypes user defined using the default datatypes 
objects / Arrays / Functions
store reference to the value , slower more memory 
mutable can be changed
*/

// ================= Primitive Data Types =================
let num = 42;                       // Number
let str = "Hello";                  // String
let isActive = true;                // Boolean
let emptyValue = null;              // Null
let notAssigned;                    // Undefined
let bigNumber = 12345678901234567890n; // BigInt
let uniqueId = Symbol("id");        // Symbol

console.log("Number:", num);
console.log("String:", str);
console.log("Boolean:", isActive);
console.log("Null:", emptyValue);
console.log("Undefined:", notAssigned);
console.log("BigInt:", bigNumber);
console.log("Symbol:", uniqueId);

// ================= Non-Primitive Data Types =================
let person = { name: "Alice", age: 25 }; // Object
let numbers = [10, 20, 30];              // Array
function greet(name) { return "Hi " + name; } // Function

console.log("Object:", person);
console.log("Array:", numbers);
console.log("Function:", greet("Alice"));

//********************Less used but available datatypes********************//
let user = { name: "Alice" };

let id = Symbol("id");  // unique key
user[id] = 101;         // attach hidden property

console.log(user);       
// → { name: 'Alice', [Symbol(id)]: 101 }
console.log(user.id);    // undefined (not a normal key)

// Normal Number
let normal = 9007199254740991;   // Max safe integer
console.log("Normal:", normal);

// Going beyond safe integer
console.log("Normal + 1:", normal + 1);  // 9007199254740992
console.log("Normal + 2:", normal + 2);  // 9007199254740992 ❌ (wrong!)

// Using BigInt
let bigNum = 9007199254740991n; 
console.log("BigInt:", bigNum);

console.log("BigInt + 1n:", bigNum + 1n);  // ✅ 9007199254740992n
console.log("BigInt + 2n:", bigNum + 2n);  // ✅ 9007199254740993n



// ===============================
// JavaScript Array Functions
// ===============================

// 1. push() → Add item at the end
let fruits = ["apple", "banana"];
fruits.push("orange"); 
console.log(fruits); // ["apple", "banana", "orange"]


// 2. pop() → Remove last item
fruits.pop();
console.log(fruits); // ["apple", "banana"]


// 3. shift() → Remove first item
fruits.shift();
console.log(fruits); // ["banana"]


// 4. unshift() → Add item at the start
fruits.unshift("apple");
console.log(fruits); // ["apple", "banana"]


// 5. map() → Creates a new array by applying a function to each element
let numbers1 = [1, 2, 3];
let squares = numbers1.map(num => num * num);
console.log(squares); // [1, 4, 9]


// 6. filter() → Filters elements based on a condition
let nums = [1, 2, 3, 4, 5];
let evens = nums.filter(num => num % 2 === 0);
console.log(evens); // [2, 4]


// 7. reduce() → Reduces array to a single value
let values = [1, 2, 3, 4];
let sum = values.reduce((acc, curr) => acc + curr, 0);
console.log(sum); // 10


// 8. forEach() → Loops through array (no return value)
let colors = ["red", "green", "blue"];
colors.forEach(color => console.log(color));
// red
// green
// blue


// 9. find() → Returns the first element that matches condition
let ages = [10, 20, 30, 40];
let firstAbove25 = ages.find(age => age > 25);
console.log(firstAbove25); // 30


// 10. includes() → Checks if array contains a value
let pets = ["dog", "cat", "rabbit"];
console.log(pets.includes("cat"));    // true
console.log(pets.includes("elephant")); // false

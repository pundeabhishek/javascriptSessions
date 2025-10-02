console.log("Hello, World!");

// var is function-scoped (leaks outside block)
if (true) {
  var fruit = "apple";
}
console.log(fruit);  // "apple"

// let is block-scoped
if (true) {
  let fruit = "apple";
  console.log(fruit);  // "apple"
}
// console.log(fruit); // Error: fruit is not defined

// const is block-scoped and cannot be reassigned
const city = "London";
console.log(city);  // "London"
// city = "Paris"; // Error: Assignment to constant variable

// var hoisting issue
console.log(color);  // undefined
var color = "blue";

// Primitive Data Types
let name = "Alice";
console.log("String:", name);
console.log("Type:", typeof name);

let age = 25;
console.log("Number:", age);
console.log("Type:", typeof age);

let isStudent = true;
console.log("Boolean:", isStudent);
console.log("Type:", typeof isStudent);

let car = null;
console.log("Null:", car);
console.log("Type:", typeof car);

let city1;
console.log("Undefined:", city1);
console.log("Type:", typeof city1);

let a;
let b = null;
console.log("a:", a);
console.log("typeof a:", typeof a);
console.log("b:", b);
console.log("typeof b:", typeof b);

// More primitive types
let num = 42;
let str = "Hello";
let isActive = true;
let emptyValue = null;
let notAssigned;
let bigNumber = 12345678901234567890n;
let uniqueId = Symbol("id");

console.log("Number:", num);
console.log("String:", str);
console.log("Boolean:", isActive);
console.log("Null:", emptyValue);
console.log("Undefined:", notAssigned);
console.log("BigInt:", bigNumber);
console.log("Symbol:", uniqueId);

// Non-Primitive Data Types
let person = { name: "Alice", age: 25 };
let numbers = [10, 20, 30];
function greet(name) { return "Hi " + name; }

console.log("Object:", person);
console.log("Array:", numbers);
console.log("Function:", greet("Alice"));

// Symbol property in object
let user = { name: "Alice" };
let id = Symbol("id");
user[id] = 101;
console.log(user);
console.log(user.id); // undefined

// Number vs BigInt
let normal = 9007199254740991;
console.log("Normal:", normal);
console.log("Normal + 1:", normal + 1);
console.log("Normal + 2:", normal + 2);

let bigNum = 9007199254740991n;
console.log("BigInt:", bigNum);
console.log("BigInt + 1n:", bigNum + 1n);
console.log("BigInt + 2n:", bigNum + 2n);

// Array Functions

let fruits = ["apple", "banana"];
fruits.push("orange");
console.log(fruits);

fruits.pop();
console.log(fruits);

fruits.shift();
console.log(fruits);

fruits.unshift("apple");
console.log(fruits);

let pets = ["dog", "cat", "rabbit"];
console.log(pets.includes("cat"));
console.log(pets.includes("elephant"));

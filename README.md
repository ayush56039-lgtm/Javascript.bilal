
JavaScript — Understanding Through Coding
1. JAVASCRIPT BASICS
console.log("Hello JavaScript");
console.log(10 + 20)
● What JavaScript does
● Statements
● console.log()
2. COMMENTS
// This is a single-line comment
/*
This is a
multi-line comment
*/
console.log("Hello");
3. VARIABLES — VAR, LET, CONST
var a = 10;
let b = 20;
const c = 30;
console.log(a);
console.log(b);
console.log(c);
REASSIGNMENT
let x = 10;
x = 20;
console.log(x);
const y = 10;
y = 20; // Error
fundamental difference:
var → function scoped
let → block scoped
const → block scoped + cannot be reassigned
4. SCOPE
GLOBAL SCOPE
let college = "United University";
function show() {
console.log(college);
}
show();
FUNCTION SCOPE
function test() {
let x = 10;
console.log(x);
}
test();
console.log(x); // Error
BLOCK SCOPE
if (true) {
let x = 10;
const y = 20;
console.log(x);
console.log(y);
}
console.log(x); // Error
VAR VS LET
if (true) {
var a = 10;
let b = 20;
}
console.log(a); // 10
console.log(b); // Error
5. SCOPE CHAIN
let college = "United University";
function teacher() {
let subject = "JavaScript";
function lecture() {
let topic = "Scope";
console.log(college);
console.log(subject);
console.log(topic);
}
lecture();
}
teacher();
lecture scope
↓
teacher scope
↓
global scope
JavaScript searches outward when a variable isn't found in the current scope.
6. DATA TYPES
let name = "Rahul"; // String
let age = 20; // Number
let passed = true; // Boolean
let x; // Undefined
let y = null; // Null
console.log(typeof name);
console.log(typeof age);
console.log(typeof passed);
console.log(typeof x);
console.log(typeof y);
let big = 12345678901234567890n; // BigInt
let id = Symbol("id"); // Symbol
7. PRIMITIVE VS REFERENCE TYPES
Primitivelet a = 10;
let b = a;
b = 20;
console.log(a); // 10
console.log(b); // 20
REFERENCE
let student1 = {
name: "Rahul"
};
let student2 = student1;
student2.name = "Amit";
console.log(student1.name);
Output:
Amit
8. TYPE CONVERSION
let x = "10";
console.log(typeof x);
let y = Number(x);
console.log(y);
console.log(typeof y);
Other conversions:
String(100);
Number("100");
Boolean(1);
Boolean(0);
9. OPERATORS
ARITHMETIC
let a = 10;
let b = 3;
console.log(a + b);
console.log(a - b);
console.log(a * b);console.log(a / b);
console.log(a % b);
console.log(a ** b);
INCREMENT / DECREMENT
let x = 10;
x++;
console.log(x);
x--;
console.log(x);
10. ASSIGNMENT OPERATORS
let x = 10;
x += 5;
console.log(x);
x -= 2;
console.log(x);
x *= 2;
console.log(x);
x /= 2;
console.log(x);
11. COMPARISON OPERATORS
console.log(10 > 5);
console.log(10 < 5);
console.log(10 >= 10);
console.log(10 == "10");
console.log(10 === "10");
Important concept:
== → loose equality
=== → strict equality
Show:
console.log(10 == "10"); // true
console.log(10 === "10"); // false
12. LOGICAL OPERATORS
console.log(a / b);
console.log(a % b);
console.log(a ** b);
INCREMENT / DECREMENT
let x = 10;
x++;
console.log(x);
x--;
console.log(x);
10. ASSIGNMENT OPERATORS
let x = 10;
x += 5;
console.log(x);
x -= 2;
console.log(x);
x *= 2;
console.log(x);
x /= 2;
console.log(x);
11. COMPARISON OPERATORS
console.log(10 > 5);
console.log(10 < 5);
console.log(10 >= 10);
console.log(10 == "10");
console.log(10 === "10");
Important concept:
== → loose equality
=== → strict equality
Show:
console.log(10 == "10"); // true
console.log(10 === "10"); // false
12. LOGICAL OPERATORS
let age = 20;
let student = true;
console.log(age >= 18 && student);
console.log(age >= 18 || student);
console.log(!student);
&& AND
|| OR
! NOT
13. IF
let marks = 75;
if (marks >= 40) {
console.log("Pass");
}
14. IF...ELSE
let marks = 35;
if (marks >= 40) {
console.log("Pass");
} else {
console.log("Fail");
}
15. ELSE IF
let marks = 78;
if (marks >= 90) {
console.log("A+");
} else if (marks >= 75) {
console.log("A");
} else if (marks >= 60) {
console.log("B");
} else if (marks >= 40) {
console.log("C");
} else {
console.log("Fail");
}
16. TERNARY OPERATOR
First:
let age = 20;
if (age >= 18) {
console.log("Adult");
} else {
console.log("Minor");
}
Then simplify:
let age = 20;
let result = age >= 18 ? "Adult" : "Minor";
console.log(result);
17. SWITCH
let day = 2;
switch (day) {
case 1:
console.log("Monday");
break;
case 2:
console.log("Tuesday");
break;
case 3:
console.log("Wednesday");
break;
default:
console.log("Invalid day");
}
18. FOR LOOP
for (let i = 1; i <= 5; i++) {
console.log(i);
}
Then:
for (let i = 1; i <= 10; i++) {
if (i % 2 == 0) {
console.log(i);
}
}
19. WHILE
let i = 1;
while (i <= 5) {
console.log(i);
i++;
}
20. DO...WHILE
let i = 1;
do {
console.log(i);
i++;
} while (i <= 5);
Then show the difference:
let i = 10;
while (i < 5) {
console.log(i);
}
Nothing happens.
But:
let i = 10;
do {
console.log(i);
} while (i < 5);
Output:
10
21. BREAKfor (let i = 1; i <= 10; i++) {
if (i == 5) {
break;
}
console.log(i);
}
22. CONTINUE
for (let i = 1; i <= 5; i++) {
if (i == 3) {
continue;
}
console.log(i);
}
23. FUNCTIONS
function greet() {
console.log("Hello Students");
}
greet();
24. FUNCTION PARAMETERS
function greet(name) {
console.log("Hello " + name);
}
greet("Rahul");
greet("Amit");
25. RETURN
function add(a, b) {
return a + b;
}
let result = add(10, 20);
console.log(result);
parameter → input
return → output
26. FUNCTION EXPRESSION
const add = function(a, b) {
return a + b;
};
console.log(add(10, 20));
27. ARROW FUNCTION
const add = (a, b) => {
return a + b;
};
console.log(add(10, 20));
Short form:
const add = (a, b) => a + b;
console.log(add(10, 20));
28. ARRAYS
let students = ["Rahul", "Amit", "Neha"];
console.log(students);
console.log(students[0]);
console.log(students[1]);
ndexing:
Rahul Amit Neha
0 1 2
29. MODIFY ARRAY
let students = ["Rahul", "Amit", "Neha"];
students[1] = "Priya";
console.log(students);
30. ARRAY METHODS
let students = ["Rahul", "Amit"];
students.push("Neha");
console.log(students);
students.pop();
students.shift();
students.unshift("Priya");
31. ARRAY LENGTH
let numbers = [10, 20, 30, 40];
console.log(numbers.length);
32. LOOP THROUGH ARRAY
let students = ["Rahul", "Amit", "Neha"];
for (let i = 0; i < students.length; i++) {
console.log(students[i]);
}
33. FOR...OF
let students = ["Rahul", "Amit", "Neha"];
for (let student of students) {
console.log(student);
}
34. FOREACH()
let numbers = [10, 20, 30];
numbers.forEach(function(number) {
console.log(number);
});
Arrow version:
numbers.forEach(number => console.log(number));
35. MAP()
let numbers = [1, 2, 3, 4];
let squares = numbers.map(function(number) {
return number * number;
});
console.log(squares);
Output:
[1, 4, 9, 16]
map() creates a new array.
36. FILTER()
let marks = [35, 67, 89, 42, 25];
let passed = marks.filter(function(mark) {
console.log("Welcome to JavaScript");
}
greet("Rahul", finish);
66. PROMISE
let promise = new Promise(function(resolve, reject) {
let success = true;
if (success) {
resolve("Task completed");
} else {
reject("Task failed");
}
});
promise
.then(result => console.log(result))
.catch(error => console.log(error));
67. ASYNC/AWAIT
function getData() {
return new Promise(resolve => {
setTimeout(() => {
resolve("Data received");
}, 2000);
});
}
async function showData() {
console.log("Waiting...");
let result = await getData();
console.log(result);
}
showData();
68. FETCH API
fetch("https://jsonplaceholder.typicode.com/users")
.then(response => response.json())class Student {
constructor(name, age) {
this.name = name;
this.age = age;
}
showDetails() {
console.log(this.name);
console.log(this.age);
}
}
let s1 = new Student("Rahul", 20);
s1.showDetails();
64. INHERITANCE
class Student {
study() {
console.log("Student is studying");
}
}
class BCAStudent extends Student {
code() {
console.log("Student is coding");
}
}
let s = new BCAStudent();
s.study();
s.code();
65. CALLBACK FUNCTION
function greet(name, callback) {
console.log("Hello " + name);
callback();
}
function finish() {
</script>
This combines many concepts students have already learned.
60. FORM VALIDATION
function validate() {
let name = document.getElementById("name").value;
if (name == "") {
alert("Name is required");
return false;
}
return true;
}
61. LOCALSTORAGE
localStorage.setItem("name", "Rahul");
let name = localStorage.getItem("name");
console.log(name);
Delete:
localStorage.removeItem("name");
Clear:
localStorage.clear();
62. JSON
let student = {
name: "Rahul",
age: 20
};
let jsonData = JSON.stringify(student);
console.log(jsonData);
Back to object:
let objectData = JSON.parse(jsonData);
console.log(objectData.name);
Object → JSON JSON.stringify()
JSON → Object JSON.parse()
63. CLASSES
</script>
Then:
document.getElementById("title").innerText = "Hello JavaScript";
57. CHANGE CSS WITH JAVASCRIPT
<h1 id="title">Hello</h1>
<script>
let heading = document.getElementById("title");
heading.style.color = "red";
heading.style.fontSize = "40px";
</script>
58. EVENTS
<button onclick="sayHello()">Click Me</button>
<script>
function sayHello() {
alert("Hello Students!");
}
</script>
Then teach modern event handling:
let button = document.querySelector("button");
button.addEventListener("click", function() {
console.log("Button clicked");
});
9. INPUT AND DOM
<input id="name">
<button onclick="showName()">Submit</button>
<p id="result"></p>
<script>
function showName() {
let name = document.getElementById("name").value;
document.getElementById("result").innerText =
"Hello " + name;
}
return mark >= 40;
});
console.log(passed);
37. FIND()
let marks = [35, 67, 89, 42];
let result = marks.find(mark => mark > 80);
console.log(result);
38. REDUCE()
let numbers = [10, 20, 30, 40];
let total = numbers.reduce(function(sum, number) {
return sum + number;
}, 0);
console.log(total);
difference:
forEach → perform something
map → transform
filter → select
find → find one
reduce → combine into one result
39. STRINGS
let name = "JavaScript";
console.log(name.length);
console.log(name.toUpperCase());
console.log(name.toLowerCase());
console.log(name.charAt(0));
40. STRING METHODS
let text = "Hello JavaScript";
console.log(text.includes("Java"));
console.log(text.startsWith("Hello"));
console.log(text.endsWith("Script"));
console.log(text.indexOf("Java"));
41. TEMPLATE LITERALS

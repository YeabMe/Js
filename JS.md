<!-- JS -->

-> Where To Put JS File
   ----- --
   . <script> 
     </script> <!-- on head or body -->

   . <script src="./src/script.js">
     </script> <!-- External or separate js file -->

-> Debug & Outputing elements 
   ----- - --------- --------
  - alert('Hello YeabMe');

-> Browser console
   ------- -------
  - Ctr + Shift + i   or
  - F12

  <!-- Console -->
  > alert('Hi YeabMe')
  > console.log('Hello YeabMe')
  > console.error('This is an error')
  > console.warn('This is a warning')

-> Variables
   ---------

  - var age = 0;


  - let age = 20; <!-- assign age value is 20 -->
    age = 21;  <!-- Re-assign the age value by 21 -->
    console.log(age); <!-- age = 21 -->
   
  - const age = 20; 
    age = 21;  
    console.log(age); <!-- The output is TypeError : Assignment to constant variable -->


----------------------------------------------------------------
  <!-- String, Numbers, Boolean, null, undefind-->
  const name = 'YeabMe'
  const age = '21'
  const rating = '4.5'
  const isCool = 'true'
  const x = 'null'
  const y = 'undefined'

  let z;

  consol.log(typeof name);
  <!-- end -->



----------------------------------------------------------------
 <!-- Cocatination -->
  const name = 'YeabMe'
  const age = '21'

  console.log('My name is' + name +'and I am ' + age);
  <!-- Template string -->
  const hello = 'My name is ${name} and I am ${age}';

  console.log(hello);
----------------------------------------------------------------
<!-- String methods  -->
----------------------------------------------------------------
<!-- Example -->
const y = 'Hello YeabMe';

console.log(y.length);    <!-- length of the string -->

console.log(y.toUpperCase());    <!-- Uppercase -->

console.log(y.toLowerCase());    <!-- Lowercase -->

console.log(y.substring(0, 5));    <!-- substring ,index values -->
console.log(y.substring(0, 5).toUpperCase());    <!-- substring + Uppercase -->

console.log(y.split(''));    <!-- split like array -->
<!-- const y = 'YeabMe, Git, github, website, developer
     consloe.log(y.split(','));

     output: Length (5) {"YeabMe", "Git", "github", "website","developer"}
-->



----------------------------------------------------------------
<!-- Array : variables that hold multiple values. --> 
<!-- Eg.1 -->
const numbers = new Array(1,2,3,4,5,);

console.log(numbers);

<!-- Eg.2 -->
const fruit = ['apples', 'oranges', 'banana'];

console.log(fruit);  // {"apples", "oranges", "banana"}

console.log(fruit[1]);      // oranges

<!-- En.3 -->
const fruit = ['apples', 'oranges', 'banana'];

fruits[3] = 'watermelon';

console.log(fruit);     // {"apples", "oranges", "banana", "watermelon"}



----------------------------------------------------------------
<!-- push, pop, unshift-->

fruits.push('mangos');       // add into the last 

fruits.unshift('mangos');       // add into the first

fruits.pop('mangos');       // the last one off

<!-- Array.isArray(value) -->

console.log(Array.isArray([1, 3, 5]));
// Expected output: true

<!-- indexOf(searchElement)
indexOf(searchElement, fromIndex) -->

const beasts = ['ant', 'bison', 'camel', 'duck', 'bison'];

console.log(beasts.indexOf('bison'));
// Expected output: 1

// Start from index 2
console.log(beasts.indexOf('bison', 2));
// Expected output: 4

console.log(beasts.indexOf('giraffe'));
// Expected output: -1

----------------------------------------------------------------
<!-- Objects literal: 're a key values pairs -->

const person = {
  firstName: 'YeabMe',
  lastName: 'Yeab',
  age: '21',
  hobbies: ['music', 'movies', 'coding'],
  address: {
    street: 'Ethio chain st'
    city: 'Addis Ababa'
  }
}

console.log(person);            // all values ...

console.log(person,firstName)  // "YeabMe"

console.log(person.address.city)  // "Addis Ababa"

<!-- Advanced -->
const { firstName, lastName} = person;
console.log(firstName);  // "YeabMe"

const { firstName, lastName, address:{street}} = person;
console.log(street);  // "Ethio chain st"

<!-- Property -->
person.email = 'yeabtsegamesfin2@gmail.com';
console.log(person);   // add email into person

----------------------------------------------------------------

<!-- Array with objects -->

const todos =[
  {
    id : 1,
    text: 'Take out trash';
    isCompleted: true
  },

    {
    id : 2,
    text: 'Meeting with boss';
    isCompleted: true
  },

  {
    id : 3,
    text: 'Dentist appt';
    isCompleted: false
  },
];

 console.log(todos);      // {},{},{}

 console.log(todos[1].text);  // index 1 object text value display

----------------------------------------------------------------
<!--# Loops -->
<!--  For loop -->
for (let i = 0; i<=10; i++){
  console.log(i);
  or
  console.log('For Loop Number: ${i}');
}

<!-- While loop -->
let i = 0;
while (i < 10){
  console.log('while Loop Number: ${i}');
  i++;
}

<!-- Loops on Array -->
for (let i = 0; i < todos.length; i++){
  console.log(todos[i].text);
}
<!-- for of -->
for(let todo of todos){
  console.log(todos.text);
}

----------------------------------------------------------------

<!-- forEach, map, filter -->

<!-- forEach -->
todos.forEach(function(todo){
  console.log(todo.text);
});

<!-- map -->
const todoText = todos.map(function(todo){
 return todo.text;
});

console.log(todoText);

<!-- filter -->
const todoCompleted = todos.filter(function(todo){
 return todo.isCompleted === true;
});

console.log(todoCompleted);

<!-- filter and map -Functional Programming -->
const todoCompleted = todos.filter(function(todo){
 return todo.isCompleted === true;
}).map(function(todo){
  return todo.text;
})

console.log(todoCompleted);

----------------------------------------------------------------

<!-- Conditional statements -->
<!-- === always use better -->

const x = 10;

<!-- if -->
if(x === 10){
  console.log('x is 10');
} 

<!-- if else -->
if(x === 10){
  console.log('x is 10');

} else{
  console.log('x is NOT 10');
}

<!-- if else if -->
if(x === 10){
  console.log('x is 10');

}else if(x > 10){
 console.log('x is greater than 10');

}else{
  console.log('x is less than 10');
}


<!-- Ex -->

const x = 4;
const y = 10;

if(x > 5 || y > 10) {
  console.log('x is more than 5 or y is more than 10');
}

<!-- Ternery operaters -->
const x = 10;

const color = x > 10 ? 'red' : 'blue';

console.log(color);

<!-- Switch -->

siwtch(color){
  case 'red':
  console.log('color is red');
  break;

  case 'blue':
  console.log('color is blue');
  break;

  default:
  console.log('color is Not Red or Blue');
  break;
}

---------------------------------------------------------------

<!-- Functions -->

function addNum1(num1, num2){
  console.log(num1 + num2);
}

addNums();

output: NAN

---------------------------

function addNum1(num1 = 1, num2 = 1){
  console.log(num1 + num2);
}

addNums();

output: 2

---------------------------

function addNum1(num1 = 1, num2 = 1){
  console.log(num1 + num2);
}

addNums(5, 5);

output: 10 // override

---------------------------

function addNum1(num1 = 1, num2 = 1){
  return num1 + num2;
}

console.log(addNums(5, 5));

output: 10

----------------------------
<!-- Arrow function ES-6 -->

function addNum1 = (num1 = 1, num2 = 1) =>{
  return num1 + num2;
}

console.log(addNums(5, 5));

output: 10

<!-- or -->

function addNum1 = (num1 = 1, num2 = 1) =>{
 console.log(num1 + num2);
}

console.log(addNums(5, 5));

output: 10

----------------------------------------------------------------
<!-- Constructor function -->
function Person(firstName, lastName, dob){
  this.firstName = firstName;
  this.lastName = lastName;
  this.dob = new Date(dob);
}

<!-- Instantiate object -->
const person1 = new person{'Yeab', 'doe', '3-4-2024'};
const person2 = new person{'Me', 'doe', '3-4-2023'};

console.log(person2.firstName);
// Me
console.log(person2.dob);
// Date & Time 
console.log(person2.dob.getFullYear());
// 2023

------------------------------------------------------------
function Person(firstName, lastName, dob){
  this.firstName = firstName;
  this.lastName = lastName;
  this.dob = new Date(dob);
  this.getBirrYear = function() {
    return this.dob.getFullYear();
  }
  this.getFullName = function() {
    return '${this.firstName} ${this.lastName}';
  }
}

const person1 = new person{'Yeab', 'me', '3-4-2024'};
const person2 = new person{'Me', 'doe', '3-4-2023'};

console.log(person1.getBirthYear());
// 2024

console.log(person1.getFullName());
// Yeab me

------------------------------------------------------------
<!-- Class -->
class Person {
  constructor (firstName, lastName, dob) {
    this.firstName = firstName;
    this.lastName = lastName
    this.dob = new Date(dob);
  }

  getBirthYear() {
    return this.dobFullYear();
  }

  getFullName() {
    return '${this.firstName} ${this.lastName}';
  }
}

------------------------------------------------------------
<!-- Selce items from the DOM -->

<!-- Single element -->
console.log(document.querySelectorAll('my-from'));
// select form 

console.log(getElementsByClassName('h1'));
// select h1

<!-- Multiple element -->
console.log(document.querySelectorAll('.item'));
// select item class 

console.log(document.getElementsByClassName('item'));
// select item class

------------------------------------------------------------
<ul class="items">
  <li class="item"> ITEM 1 </li>
  <li class="item"> ITEM 2 </li>
  <li class="item"> ITEM 3 </li>
  <li class="item"> ITEM 4 </li>
</ul>

<!-- Manipulating DOM -->

const ul = document.querySelector('.items');

ul.remove();

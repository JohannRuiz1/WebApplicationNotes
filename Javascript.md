### Variables
var is functioned scoped, mutable

function testVar() {
    var x = 1;
    if (true) {
        var x = 2; // same variable
        console.log(x); // 2
    }
    console.log(x); // 2
}
testVar();


let is blocked scoped, let cannot be redeclared in the same scope
function testLet() {
    let y = 1;
    if (true) {
        let y = 2; // different variable
        console.log(y); // 2
    }
    console.log(y); // 1
}
testLet();

Infinity and -Infinity are used for upper and lower bounds for integer

NaN is not a number

Booleans: true or false (all lowercase)

Are two variables the same, use === (Three equal signs)

const is immutable (const dozen = 12)

Java script doesn't have int/double, it has Numbers

### Objects

var emptyObject = {};

var nonEmptyObject = { label: "value1", sign: "value2 }

![[Pasted image 20240530195402.png]]

## Map and Set Object Types and Looping

let mySet = new Set();
- Store each value exactly once
- Must be accessed and changed using methods
mySet.add('juno')
mySet.has('juno')

Adding an array to a Set constructor will automatically remove duplicates
-> let mySet = new Set(myList);

let myMap = new Map();
- Map preserve the order of keys 
myMap.get('thing1')
myMap.set("key1", "value1")

Creating a map from an object
newMap = new Map(Object.entries(map));


### Functions

Always check what type your arguments are

if (typeof arg !=== "expectedType")

function speak() {

}

speak();


### Function Expression

// Function expression assigned to a variable
const speak = function() {

}

function speakSomething(what = "Default speech", howMany = 10){

}
### Alternative way of accessing arguments
function addingMachine() {
  arguments[i];
  arguments is an array
}

function addingMachine(...terms) {
	terms is an arrays, can be combined with other arguments if it's at the end
}

var obj = {
  sayHello: function () {
    console.log("Hello");
  }
}

### Function expression are variables that can be passed in argument 
Functions can be arguments
var speakSomething = function(what = 'Speaking!') {
    for (var i = 0; i < 10; i += 1) {
       console.log(what);
    }
};

setTimeout(speakSomething, 5000);

#### Writing shorter functions
var speakSomething = (what = 'Speaking!' ) => {

};

let isEven = (num) => {
	return num % 2 === 0
}

can become

isEven = (num) => num % 2 === 0; // Can remove the parenthesis too


#### Callback Functions



function doudleIt(number) {
	return (number*=2);
}

var myNumbers = [1, 2, 3, 4, 5]

var myDoubles = myNumbers.map(doubleIt)

// .map takes in a function and applies the function to each element in the array

myNumbers.forEach( function(number)) { // Doesn't need the function keyword if uses =>
	console.log("My array contains", number)
};

const myTextField = document.getElementById("myTextField")
myTextField.addEventListener( "keyup", () => {
	console.log("Someone is typing");
});
# Corrections

## Quiz 4

Question 7

The correct answer for declaring a variable for pi at the approximation of 3.14 that wouldn't change during the course of a program is to create a "const PI = 3.14;". By creating a constant, the variable can't be reassigned, meaning that it will stay the same throughout the program. Consts are declared in all capitals by convention, so te correct answer is const PI instead of const pi.

Question 8

The correct answer for initializing a variable "x" with a value of 27 is "let x; x = 27;" and "let x = 27;". There are two ways of doing this. The first way is to create the variable and it's vaule in one statement (let x = 27;), in this way creating the variable and giving it a value at the same time. YOu could also initalize the variable and give it a value later, as shown by (let x; x = 27;). Both statements are correct ways to answer the question.

Question 10

There are many different ways to state that a value is falsey. Nan, meaning not a number, is always a falsey value,as is undefined(no value), null(meaning none), ""(an empty string, no value) and false(falsey by nature). 0 is also a falsey value because like all of these other types, it means nothing/no value (a false value).

Question 11

```js
function offToCollege() {
  let favCollege = prompt("Enter your favorite college or University.");
  let collegeTut = Number(prompt("Enter the total tuition cost for all four years."));

  collegeTut = collegeTut/4;

  let p = getElementById("off-to-college");
  p.innerHTML = favCollege + " is a pretty expensive school! It'll cost you $" + collegeTut + " per year!";
}

function carpool() {
  let nFriends = Number(prompt("How many friends would you like to invite to the movies?"));
  let driversSUV = Number(prompt("How many of your friends parents drive SUVs with a capacity of 7?"));

  let nSuvSeats = driversSUV * 7;
  let nSedanSeats = nFriends - nSuvSeats;
if(nSedanSeats > 4) {
  nSedanSeats = Math.ceil(nSedanSeats / 4);
}

  consloe.log(nSuvSeats + " parents who drive SUVs and " + nSedanSeats + " parents who drive sedans are required to drive the " + nFriends + " friends to the movies.");
}

```

## Quiz 5

Question 1

Logical operators refer to operators that use logic. If you are using an if statement, you would the or (||) to say this statement or this one (x == 5 || x < 4). You could also say if it was not this number (!), as in a statement like !(x == y). You could also use and(&&), as in if (x > 10 && x < 100).

Question 2

Relational operators are comparison operators, which compare variables and numbers. Some are != (not equal, x != 6), >= (greater or equal to), !== (not equal value/type, x !== "5" in the case that x is a number this would be true), < (less than), == (equal to), > (greater than), <= (less than or equal to), === (strict equals, this is used with strings). These all compare variables/strings/numbers and return as true or false.

Question 5

When "let a = "hello"; console.log(!a); console.log(!!a);", false, true is entered to the console. This is because !a would be not "a", which would equal false. !! "a" would be not not "a", meaning "a", which is equal to true.

Question 8

```js
let ageGroup = (Number(prompt("How old are you?")) < 18) ? "CHILD" : "ADULT";
let status = (ageGroup === "CHILD" && prompt("Do you go to school here?") === "Y")
   ? "STUDENT"
   : "VISITOR";

let admission;
if (ageGroup === "CHILD") {
    admission = 10;

    if (status === "STUDENT") {
        admission = admission - (admission * 0.2);
    }
} else {
    admission = 20;
}
```

Running 17 and N through the code puts the user into the "Child" and "Visitor" categories, giving the user an admission of 10 with no student discount. Running 16 and Y through the code gives the user the "Child" and "Student" categories, which first gives the user an admission of 10, and then 10 - (10 * 0.2), which gives the user an admission of 8. Running 24 and N through the code  gives the user a status of "Adult" and "N", which means that the user is not a child, (goes into else category), and has an admission of 20. This means that the answer is 10, 8, and 20, respectively.

Question 12

Anything written in a while or do...while loop cannot be achieved with a for loop or vise versa. A while loop does a set of code while a statement is true, and only stops when that statement is not true. However, a for loop does a set of code for a specific amount of times by setting a variable and a statement, and adding to that variable ever time (let i; i < names.length; i++) {

}. These are not the same, and are used in different situations.

Question 13

The four components of a for loop in order are:

1. Setup
1. Expression
1. Loop body
1. Update
1. Return to Step 2

First you set up the loop variable (let i;), then you have the expression (i < names.length;), then the body ({
    //code
}), then the update (i ++;), then return to step 2 to double check the equation.

## Quiz 6

Question 2

Built in functions that accept parameters(these) include prompt(), alert(), and console.log(). You can use these to add variables or generally display text, and they accept variables to display/use.

Question 4

```js
function divide() {
    let a = Number(prompt("Enter a number."));
    let b = Number(prompt("Enter another number."));

    return a / b;
}
```

You would add (a, b) to be the parameters, which are in this case variables from ot side the equations. You woudn't need the prompts anymore, so the function would be function "divide(a, b) {
    return a / b;
}".

Question 5

A built in function already designed to return a value is the prompt function. This returns the value the user entered, letting the programmer use the value.

Question 7

```js
let product = multiply(5, 4, 5);" Three functions that declare and implement this include :
"function multiply(a, b, c, d) {
    if (a !== undefined && b !== undefined && c !== undefined && d !== undefined) {
        return a * b * c * d;
    else if (a !== undefined && b !== undefined && c !== undefined) {
        return a * b * c;
    } else if (a !== undefined && b !== undefined) {
        return a * b;
    } else if (a !== undefined) {
        return a;
    }
}
```

```js
"function multiply(x, y, z) {
    let product = x * y * z;

    return product;
}
```

```js
function multiply(x, y, z) {
    return x * y * z;
}
```

The first one works because it returns whatever values are declared multiplied together, giving the mutiplied value of 5, 4, 5. The second works because it declares the result of the three values as product and returns it, giving the program the value. The third one works because it simply returns the value, giving the program the value.

Question 13

```js
function example(a, b, c) {
    if (a === 1) {
        if (b === 2) {
            if (c === 3) {
                var d = 4;
            }
        }
    }

    console.log(d);
}
```

If a is 1 and b is 2 and c is 3 then d would equal 4. If one of these in this oder isn't true, then d would be undefined. Therefore, the result of this code is either 4 otr undefined being printed to the console.

## Quiz 7

Question 1

```js
let tripleDigits = numbers.every(function(num) {
   return num >= 100 && num <= 999;
});
```

Assumming numbers is "let numbers = [ 101, 202, 303, 4444, 505, 606, 707 ];", this would equal true. The function would return every number that is greater than 100 and less than 999, meaning every tripleDigit number. In this manner, tripleDigit will equal only triple digits, and so true.

Question 3

Elements of arrays can be iterated by for loops and for...each loops. For each loops does a block of code for each element of the array, therefore iterating over them.

Question 12

```js
let cars = [ "Audi", "BMW", "Mercedes", "Porsche", "Volkswagen" ];
let car = prompt("What kind of car do you drive?");

if (/* missing */) {
    console.log("You drive a German-made car.");
}
```

There are three possible replacements from the multiple choice: cars.includes(car), cars.lastIndexOf(car) !== -1, and cars.indexOf(car) !== -1. The first one simply asks the code if the car is included or not. The second asks if the lastIndexOf the car variable is not -1 (meaning there is an index), and therefore the car is or is not included. The third asks if the index of car exists, which shows whether or not it is included.

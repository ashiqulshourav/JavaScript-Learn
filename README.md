# JavaScript-Learn - "Learn with sumit".
Here I stored all JavaScript learning stage description with Bengali language


//==================== Javascript Scopes <br>
/* 
var x = 23;

// Global Scopes er dunia


function myFunc() {

    // my Func/child er dunia
    var y = 10;

    console.log(`${x} from myFunc()`)
}

myFunc();

console.log(x)


//Ending Summary
// 1. parent share everything for child but child not share for parent.
// 2. child can change parent value.
*/ <br>





//==================== var/let/const <br>
/*
var varVariable = "This is var";
console.log(varVariable);

if (true) {
    var varVariable = 'This is var again';
}

console.log(varVariable);


if (true) {
    let letVariable = "This is let";
    // let letVariable = "This is let again"; // This is totally impossible redefine for let but can change value
    letVariable = "This is let again";
    console.log(letVariable)


    // const constVariable = "Hello World!";
    // const constVariable = "Hello World! again"; // This is totally impossible redefine for const but can change value
    // constVariable = "Hello World agian"; This is also totally impossible reassign const but can change property value.


    const constVariable = {
        name: 'javascript',
        age: '25 years'
    }

    console.log(constVariable)

    constVariable.name = "JS" // this is changed const property value.

    console.log(constVariable)
}

// console.log(letVariable);

//Ending Summary
// 1. var is a function scoped, let & const is a block scoped.
// 2. var can redefine & can change value.
// 3. let can't redefine & can change value.
// 4. const can't redefine, reassign but can change property value.

*/ <br>


//==================== Closures <br>
/*
var num1 = 2; // This is global object

var sum = function() {
    var num2 = 3; // This is closure
    return function() {
        return num1 + num2;
    };
};

var myFunc = sum();

console.dir(myFunc)

function bankAccount(initialBalance) {
    var balance = initialBalance;

    return function() {
        return balance;
    }
}

var account = bankAccount(100000);

console.dir(account)

var num11 = 2;
var sum22 = function() {
    var num33 = 3;
    return num11 + num33; // There is no closure cause everything is local scope.
}

console.dir(sum22)

(function() {
    var fName = "Ashiqul"; // This is closure for fullName function. cause this whole function is blocked scopes

    var fullName = function() {
        var lastName = "Islam";
        return fName + lastName;
    };

    console.dir(fullName)
})();

function stopWatch() {
    var startTime = Date.now();

    function getDelay() {
        console.log(Date.now() - startTime);
    }

    return getDelay;
}

var timer = stopWatch();

for (var i = 0; i < 100000000; i++) {
    var a = Math.random() * 10000000;
}

timer();
console.dir(timer)

//Here var timer = stopWatch(); run first then huge operation & then timer() function run. but how js remember the start time (Ans: its only for closure)

timer = null;
timer();

//performance optimization - After timer done then if i set timer = null then js automatically clean the timer garbage



function apiFunction(url) {
    fetch(url).then((res) => {
        console.log(res)
    })
}

apiFunction('https://jsonplaceholder.typicode.com/todos/1')

//Ending Summary
// 1. Function er vitore bahirer kono variable access korte hole parameter pathiye access korte hoy
// 2. closure didn't store all global element or immediate parent element only store needed element.
// 3. Closure store variable reference not direct variable value
*/ <br>

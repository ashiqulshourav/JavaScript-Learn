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

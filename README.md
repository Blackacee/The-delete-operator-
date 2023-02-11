# The-delete-operator-


// Deleting a property
foo = 1; // a global variable is a property of `window`: `window.foo`
delete foo; // true
console.log(foo); // Uncaught ReferenceError: foo is not defined
// Deleting a variable
var foo = 1;
delete foo; // false
console.log(foo); // 1 (Not deleted)
// Deleting a function
function foo(){ };
delete foo; // false
console.log(foo); // function foo(){ } (Not deleted)
// Deleting a property
var foo = { bar: "42" };
delete foo.bar; // true
console.log(foo); // Object { } (Deleted bar)
// Deleting a property that does not exist
var foo = { };
delete foo.bar; // true
console.log(foo); // Object { } (No errors, nothing deleted)
// Deleting a non-configurable property of a predefined object
delete Math.PI; // false ()
console.log(Math.PI); // 3.141592653589793 (Not deleted)

## Chapter 3 - Functions

### Defining a Function

  * A function is created by an expression that starts with keyword `function`

  * Functions can take multiple parameters or none at all.

  * `return` without following expression --> `undefined`

### Parameters and Scopes

  * variables created within functions are local to the function

  * declaring a variable locally will overwrite global with the same name
  while inside function

### Nested Scope

  * Each local scope can see the local scopes that contain it - lexical scoping

  * Only functions - not blocks - create a new scope

### Functions as Values

  * Function values can do anything regular values can. Function names
  just regular variables

### Declaration Notation

  * Two ways to create a function:
  ```
    //Method 1:

    var future = function() {
      return "We STILL have no flying cars.";
    };

    //Method 2:

    function future() {
      return "We STILL have no flying cars.";
    }
  ```

  * Console.log(future()) before Method 1 --> error, before Method 2: --> ok

  * Function declarations moved to top of their scope

### The Call Stack

* When a function returns, control jumps back to the code that called it

* The place where the computer keeps track of this context is the call stack

* Too much on the stack --> `out of stack space`, `too much recursion`, etc

### Optional Arguments

* Pass too many arguments: extras ignored. Too few: assigned `undefined`

* Checking if arg is undefined --> optional arguments

### Closure

* A function that references a variable defined in a higher scope is a
closure

### Recursion

* A function that calls itself is recursive

* Recursion often more expensive than iteration, but better at solving
problems that require processing 'branches'

### Growing Functions

* One function, one job.

### Functions and Side Effects

* Pure functions have no side effects and do not rely on other functions'
side effects

* Pure functions often more useful because they're easier to combine

* Some things still easier using side effects 

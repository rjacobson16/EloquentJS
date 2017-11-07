# Eloquent JS - Study Notes

[Source](https://eloquentjavascript.net/)

## Chapter 1 - Values, Types, and Operators

### Bits

### Numbers

  * JS uses 64 bits to store numeric values.  

### Arithmetic

### Special Numbers

  * Special numbers Infinity and -Infinity are not precise, and calculations often lead to
NaN, the third special number

  * 0/0 --> NaN, Infinity - Infinity --> NaN, etc.

### Strings

### Unary Operators
  * operators which operate on only one value, e.g. `typeof`

### Comparisons
  * `NaN == NaN` `// => false`

### Logical Operators

  * Precedence (lowest to highest): `||` << `&&` << `>, ==, etc...`

### Undefined values

  * `null` and `undefined` usually interchangeable

### Automatic Type Conversions

  * JS wants to avoid crashing, and so will coerce types in order to make
  certain operations work. This often yields unexpected results, e.g.
  `("5" - 1)` --> 4, `("5" + 1)` --> 51

  * Use `===` to avoid type conversion

### Short-circuiting of logical operators

  * `||` returns value on left if it can be converted to true, item on the right otherwise.

  * `&&` returns value on left if it can be converted to false, item on the right otherwise.

  * expression to their right is evaluated only when necessary

---
## Chapter 2 - Program Structure

### Expressions and Statements
  * Expression like a sentence fragment. `22`, `'psychoanalysis'`, etc.

  * Statement like a complete sentence. `x = 5`, etc.

### Variables
  * var (es5) indicates variable definition

### Keywords and reserved words

    > break case catch class const continue
    > debugger default delete do else enum
    > export extends false finally for
    > function if implements import in instanceof
    > interface let new null package private
    > protected public return static super switch
    > this throw true try typeof var void while with yield

### The Environment

  * collection of variables and values is called Environment

  * when program starts, Environment is not empty. E.g. browser `window` variable

### Function

  * A function is a piece of program wrapped in a value

### Console.log

  * print to console

  * `console.log` is an expression that retrieves the `log` property from the `console` variable

### Return Values
  * Some functions good for side effects, others return value, others both

### Prompt and Confirm
  * ask ok/cancel questions with `confirm()`,
  open-ended with `prompt()`

### Control Flow

### While and Do Loops

  * `do` loop always executes its body at least once, `while` may not

### Indenting Code
  * two spaces for each open block. Styles differ

### For Loops

  * succinct alternative to `while` + counter

### Breaking out of a Loop

  * `break`

### Dispatching on a value with switch

  * syntax:
      ```
      switch (prompt("What is the weather like?")) {
        case "rainy":
          console.log("Remember to bring an umbrella.");
          break;
        case "sunny":
          console.log("Dress lightly.");
          break;
        case "cloudy":
          console.log("Go outside.");
          break;
        default:
          console.log("Unknown weather type!");
          break;
        }
      ```

### Comments

  * `// single line comment`

  * ```
    /*
      multi-
      line
      comment
    */
    ```

## Ch. 2 Exercises

### Exercise 1: Looping a triangle

*Write a loop that makes seven calls to console.log to output the following triangle:*

```
#
##
###
####
#####
######
#######
```

My Answer:

```
for (var i = 0; i < 8; i++) {
  str = ''
  for (var j=1; j < i+1; j++) {
    str += '#'
  }
  console.log(str,'\n')
}
```

### Exercise 2: FizzBuzz

My Answer:

```
for (var i = 1; i < 101; i++) {
  if (i % 3 == 0) {
    if (i % 5 == 0) {
      console.log("FizzBuzz")
    } else {
      console.log("Fizz")
    }
  } else if (i % 5 == 0) {
    console.log('Buzz')
  } else {
    console.log(i)
  }
}

```

### Exercise 3: Chess Board

*Write a program that creates a string that represents an 8×8 grid, using newline characters to separate lines. At each position of the grid there is either a space or a “#” character. The characters should form a chess board.*

*Passing this string to console.log should show something like this:*

```
# # # #
# # # #
 # # # #
# # # #
 # # # #
# # # #
 # # # #
# # # #
```

*When you have a program that generates this pattern, define a variable size = 8 and change the program so that it works for any size, outputting a grid of the given width and height.*

My Answer:

```
size = 8

for (var row = 0; row < size; row++) {
  str = ''
  for (var col = 0; col < size; col++) {
  	if (row % 2 == 0) {
      if (col % 2 == 0) str += ' '
      if (col % 2 != 0) str += '#'
    } else {
      if (col % 2 == 0) str += '#'
      if (col % 2 != 0) str += ' '
    }
  }
  console.log(str)
}
```

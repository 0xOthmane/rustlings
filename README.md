# rustlings

## Intro
- Rust uses the `print!` and `println!` macros to print text to the console.
- Positional arguments can be used `println!("Hello {}!", "world");`.

## Variables
In Rust, variables are immutable by default.
When a variable is immutable, once a value is bound to a name, you can’t change that value.
You can make them mutable by adding `mut` in front of the variable name.
- Declare a variable using `let`
- A variable should be given an explicit type and a value. `let x: i32 = 0;`
- Shadowing: you can declare a new variable with the same name as a previous variable.  https://doc.rust-lang.org/book/ch03-01-variables-and-mutability.html#shadowing
- Constants `const NUMBER: i32 = 3;`

## Functions
- Rust requires that all parts of a function's signature have type annotations.
- After the `->`. This is where the function's return type should be.
- Rust distinguishes between expressions and statements: expressions return a value based on their operand(s), and statements simply return a () type which behaves just like `void` in C/C++ language. To return the value, use `return` or remove the semicolon at the end.
- [How Functions Work](https://doc.rust-lang.org/book/ch03-03-how-functions-work.html)

## If statement (control flow)
- `if` condition does not need to be surrounded by parentheses.
- Each condition is followed by a `{}` block.
- Multiple conditions: `if condition {} else if condition2 {} else {}`.
- In Rust, every arm of an `if` expression has to return the same type of value.

## Primitive types
- Boolean `bool`
- Characters `char`: note the single quotes `let character = '/'`.
- Arrays `let _: [u8; 3] = [1, 2, 3];` or  `let _: [u8; 3] = [0; 3];`
- Tuple `let cat = ("Furry McFurson", 3.5);`. To destruct a tuple we can use pattern matching 
```console
let tup = (500, 6.4, 1);
let (x, y, z) = tup;

println!("The value of y is: {y}");
```
We can also access a tuple element directly by using a period (.) followed by the index of the value we want to access.
- [Data Types](https://doc.rust-lang.org/stable/book/ch03-02-data-types.html)
- [The Slice Type](https://doc.rust-lang.org/stable/book/ch04-03-slices.html)

## Vectors
- Two ways to define a Vector:
1. One way is to use the `Vec::new()` function to create a new vector
  and fill it with the `push()` method.
2. The second way, which is simpler is to use the `vec![]` macro and
  define your elements inside the square brackets
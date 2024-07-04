# What is Kotlin
Kotlin is a managed, strictly typed, multi-paradigm programming language.
- managed: presence of garbage collector, no need to free.
- strictly typed: Types and type checks are compile-time, even if most types can be inferred.
- multi-paradigm: procedural, OOP, functional elements

## Hello World!
```kt
fun main() {
  println("Hello World")
}
```

## functions
```
fun <function name>(param1: ParamType1, param2: ParamType2, ... <vararg paramOmega: ParamTypeOmega>): <ReturnType> { function content }
```
so

If there are no parameters, empty parenthesis, if no return type specified, defaults to `Unit` type.
Unit is like void in most other languages, we'll discuss why it's unique in a lession 6.

```kt

// main fun, printing hello world, explicit return type
fun main(): Unit {
 println("Hello World")
}

// function taking two integer parameters and returns an int
fun add(a: Int, b: Int): Int {
  return a + b
}
```
also, Kotlin doesn't need semicolons except if there are multiple expressions in a single line. (but it allows semicolons)
```kt
fun catInBox(cats: Int, boxes: Int) {
  val catPerBox = cats.toDouble() / boxes
  println("There are $catPerBox cats in each box.")
}
```

## Variables, Values

**var** for variables
**val** for values

```
var name < :Type > < = initial value >
```
initial value is mandatory if `val` is used.

Let's see some examples
```kt
// srting, final, initialized as the string "Hello World"
val hello = "Hello World!"

hello = "x" // compile error, val can't be modified later


// int, initialized as 0
var i = 0

i++ // works, i can be modified
i = 42 // also works
i = "X" // does not work, i is an integer type
i = 3.14 // also breaks

// variable with any possible type, not initialized
var a: Any
a = "Hello" // ok
a = 2 // also ok
a++ // not OK, type of A is not an int. (This is the biggest difference between a strictly or loosely typed language)
```

## Flow control
if (else)

```kt
val condition: Bool = true
if (condition) {
  if true?
} else if (false) {
  if no?
} else {
...
}
```

typical if else statement...

For
```kt
// for loop. Syntax:
for (i in 0..<10) {
  println(i)
}
```
```
syntax: for (<loopVar: <T>> in <Iterable<T>>) {
  loop content
}
```

While
it's like for, but with a condition.
```
// C like for loop
var i = 0
while (i < 10) {
  do something...
  i++
}
```

## String substitution

$ in string, content will be replaced with value. Auto string conversion
```kt
val i = 42;
// if a variable,
val str = "Hello $i"
// if an expression
val str2 = "${i + 27}, Nice!"
```



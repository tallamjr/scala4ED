# Programming in Scala, 4th Edition
Code snippets and notes from "Programming in Scala, 4th Edition" by M. Odersky, L. Spoon &amp; B. Venners

### Chapter 2: First Steps in Scala

#### Step 1: The `scala` interpretor:
```bash
18:06:32 ✔ ~/Github/origin/scala4ED (master) :: scala
Welcome to Scala 2.13.1 (Java HotSpot(TM) 64-Bit Server VM, Java 1.8.0_144).
Type in expressions for evaluation. Or try :help.

scala> 1 + 2
res0: Int = 3

scala> res0 + 10
res1: Int = 13
```
#### Step 2: Define some variables

```bash
scala> val msg = "Hello, World!"
msg: String = Hello, World!

```

> The type of `msg` is `java.lang.String`, becuase Scala strings are implemented by Java's `String`
> class

Note the type inference.
```bash

scala> val msg2: java.lang.String = "Hello again, World!"
msg2: String = Hello again, World!

scala> val msg3: String = "Hello, yet again, World!"
msg3: String = Hello, yet again, World!

scala> println(msg)
Hello, World!

scala> msg = "Goodbye cruel world!"
           ^
       error: reassignment to val

```
Multi-line:

```bash
scala> val multiLine =
     | "This is the next line."
multiLine: String = This is the next line.

scala> val blankLines =
     |
     |
You typed two blank lines.  Starting a new command.
```

#### Step 3: Define some functions

```scala
scala> def max(x: Int, y: Int): Int = {
     | if (x > y) x
     | else y
     | }
max: (x: Int, y: Int)Int

scala> max(3, 5)
res3: Int = 5

scala> def greet() = println("Hello, World!")
greet: ()Unit

```
> When you define the `greet()` function, the interpretor will respond with `greet: ()Unit`.
> "`greet`" is, of course, the name of the function. The empty parentheses indicate the function
> takes no parameters. And `Unit` is `greet's`result type. A result type of `Unit` indicates the
> function returns no interesting value. Scala's `Unit` type is similar to Java's `void` type; in
> fact, every `void` returning method in Java is mapped to a `Unit`-returning method in Scala.
> Methods with the result type of `Unit`, therefore are only executed for the side effects. In the
> case of `greet()`, the side effect is a friendly greeting printed to standard output.

```bash
scala> :quit
```

#### Step 4: Write some scala scripts

```bash
11:12:39 ✔ ~/Github/origin/scala4ED (master) :: cat ./src/main/scala/chapter01/hello.scala
println("Hello, World!, from a script")

11:12:19 ✘ ~/Github/origin/scala4ED (master) :: scala ./src/main/scala/chapter01/hello.scala
Hello, World!, from a script
```

#### Step 5: Loop with `while`; decide with `if`

### Chapter 3: Next Steps in Scala

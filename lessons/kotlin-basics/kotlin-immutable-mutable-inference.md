---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: lesson
title: Screencast 1 - immutable, mutable, and type inference in variables
excerpt: Our first beginner's lesson focuses on immutable, mutable, and type inference in variables.
youtube: https://www.youtube.com/embed/6mK3xSEgwXQ?rel=0
type: Screencast
author: Michael Rice
difficulty: Easy
length: Short
---

In this brief lesson, you're going to get a feel for why Kotlin is so different from Java and a taste for how it adds both concision and clarity to the JVM. Specifically, we'll talk about:

1. Defining variables in Kotlin
2. Immutable variables
3. Type inference in Kotlin
4. Mutable variables

Let's start with an immutable variable with an implied type -- the clearest distinction from Java. There are two awesome things to explore about this one, first example. First, you'll notice that the variable starts with the word ```val```, not a variable data type like you find in Java. The ```val``` keyword tells the Kotlin compiler that the data stored in the variable be reassigned.

```kotlin
val immutableVariableWithImpliedType = 1
```

Immutability has become an important concept lately because we've learned, as an industry, that mutability in high performance, multithreaded applications creates situations where it's easy to introduce bugs, bugs that are very hard to debug. Kotlin has it baked right in, so this code won't compile:

```kotlin
immutableVariableWithImpliedType = 2
```

Note that we don't have to initialize the val variable right away, we can do it later. For example, the following code compiles. We'll learn later that there are better ways in Kotlin to do the following code, but this should be a familiar example.

```kotlin
val immutableValue: Int

if (x == true)
    immutableValue = 1
else
    immutableValue = 2
```

Notice we added the data type after the definition of the variable, which brings us to our a big learning objective in this mini lesson. Kotlin, unlike Java, can be written much more succintly without being too obscure while still being a strongly typed language.

For example in Java, we might write the following:

```java
final int immutableValue = 1; 
```
In Kotlin, we simply say:

```kotlin
val immutableValue = 1
```

Kotlin inferred that you want ```immutableValue``` to be an ```Int``` If we have a circumstance where we don't want to rely on the Kotlin compiler's inference, we would have written (and included a semicolon too, just because long-time Java programmers have a nervous semicolon habit):

```kotlin
val immutableValue: Int = 1;
```

Notice that the type declaration follows the variable name. To support a type inference system, it makes sense that the variable data type doesn't need to appear before the variable name, as it does in Java.

What if we want to mutate a variable? That is, despite the benefits of immutability, we still want to be able to change a variable's value. We simply change ```val``` to ```var```. For example:

```kotlin
var mutableValue = 1
mutableValue = 2
```

Ok, ok, so we've only replaced a "final" keyword with a "val" keyword, removed the primitive keyword, and ditched a semicolon, or six keystrokes in total. But as we start to work through more examples, I think you'll start to appreciate how valuable Kotlin's conciseness is, and how rarely the code trades that concission for clarity.

I think you're going to like Kotlin.

Let's review what we learned: 
1. Kotlin supports inferred types, which contributes to the language's conciseness
2. Kotlin supports both mutable and immutable values, right out of the box

For questions, clarifications, or issues with this less please contact Michael Rice at [me@michaelrice.com](mailto:me@michaelrice.com)


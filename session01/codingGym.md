---
id: litvis

narrative-schemas:
  - ../../narrative-schemas/teaching.yml
---

@import "../../css/datavis.less"

<!-- Everything above this line should probably be left untouched. -->

# Coding Gym 1 : Functions

## Induction

These exercises are designed to help you build confidence programming with Elm. They assume no prior experience of coding in any language and comprise simple tasks that build your familiarity with the process of coding. In many cases they involve repetitions of limited coding tasks, but just like repeats in a gym, the more you do, the easier it gets.

The exercises will not focus on visualization (for that, see the main lecture notes), but instead concentrate on basic principles of coding in a functional language.

This document, and all the other Coding Gym documents, provides both the exercise instructions, and space for you to complete them by adding your own code.

Make sure you are viewing this page in _VSCode_ and have the litvis preview window open (`Ctrl/Cmd-K` followed by `V`). This should show a nicely formatted version of the page on the right hand side.

{(annotation|}

If you want to add your own notes to this page you can do so conveniently by placing your extra content inside these **annotation labels**, noting carefully the use of the different bracket markers `{`, `(`, `|`, `)` and `}`.

{|annotation)}

## 1.1. Simple functions

Our first coding exercises will create some functions to return values of some kind. You can give a function any name you like as long as it starts with a lowercase letter and has no spaces. The first line of a function definition is its _type annotation_ and reports the type of value it will generate. In the examples below, `myName` generates a `String` (some text), `myYearOfBirth` an integer (whole number) and `myFavouriteNumber` a floating point number (a number with a decimal point).

Below the type annotation you name the function again followed by `=` and then on a new line indented should be the code that does the work of generating a value to return.

```elm {l r}
myName : String
myName =
    "Ada Lovelace"


myYearOfBirth : Int
myYearOfBirth =
    1815


myFavouriteNumber : Float
myFavouriteNumber =
    2.71828
```

You can create your own function in a _code block_ in your document by using a pair of triple backticks as follows:

````markdown
```elm {l raw}

```
````

The `l` in the code block header means display the literate code in the preview window. `raw` (or just `r` if you prefer) means that the value of any functions you create in the block will be displayed in the preview.

{(task|}

Create separate functions, that display the following, each in their own `raw` code block. If created successfully, you should see the result of each function appear in the preview window. To start you off, I've created a few code blocks for the first few questions below the task window, but you will need to start adding your own after completing the first three functions.

- Your own first name.
- Your own last name.
- Your own year of birth.
- The number [π](https://www.piday.org/million/) rounded to six decimal places (you can just provide the number to 6 d.p. rather than relying on any _round_ function).
- A quote of your choice about data visualization.
- The number of legs of a titmouse.

{|task)}

```elm {l r}
myFirstName : String
myFirstName =
    "Ayliah"
```

```elm {l r}
mySurname : String
mySurname =
    "Fani"
```

```elm {l r}
myYear : Int
myYear =
    1995
```

```elm {l r}
pie : Float
pie =
    3.141592
```

```elm {l r}
quote : String
quote =
    "Data Vis is cool"
```

```elm {l r}
legs : Int
legs =
    2
```

## 1.2. Simple functions with operators

As well as assigning numbers or strings directly to a function, you can also get the code to perform calculations with _operators_. For example, to add two numbers together you might have a function:

```elm {l r}
daysWorking : Int
daysWorking =
    5 + 6
```

Other operators you might use include `-` (subtraction), `*` (multiplication), `//` (integer division), `/` (floating point division), `^` (exponentiation, such as `4^2` for four-squared) and `++` for concatenating (joining) strings. These operators can be applied directly to numbers (or strings) or to functions that generate numbers (or strings). If you need to control the order in which operators apply, you can use brackets. For example `2 * (3 + 4)` is 14, not 10.

As with other functions built into the Elm language, you can refer to the [Elm documentation](https://package.elm-lang.org/packages/elm/core/latest/Basics) for examples and details of how to use them.

{(task|}

Try these exercises by creating functions to calculate:

- The sum of the integers 1 to 5.
- 22 divided by 7 to at least 12 decimal places.
- The number of seconds in a leap-year.
- Your _James Bond name_ (i.e. in the form "Bond, James Bond").
- The mean (average) of the numbers 1 to 5.

{|task)}

```elm{l r}
sum : Int
sum =
    1 + 2 + 3 + 4 + 5
```

```elm{l r}
division : Float
division =
    22/7
```

```elm{l r}
seconds : Int
seconds = 366*86400
```

```elm {l r}
bondName : String
bondName =
    "Fani, Ayliah Fani"
```

```elm{l r}
average : Float
average =
    (1+2+3+4+5)/5
```

## Basic Introduction To R


![Teal, Yellow, & Red Creative Colorful Goal Setting Presentation.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1588773575369/cX7Y3eKBT.jpeg)

In this article we will cover the intro basics to [**R Programming Language**](https://www.r-project.org/about.html). This article is meant for people willing to start programming in R, beginners in R who are willing to expand their already gained knowledge in R, or people willing to start their Data Science journey using R programming language. If you are familiar with other programming languages, getting to understand R programming language will be as easy as drinking water.

%[https://twitter.com/VictorOmondi197/status/1257981772425502720]


![Basics To R Programming Language.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1588773782511/Pr1DkpqrU.jpeg)

# What is R?

Well! It is a programming language, often used in statistics and data science, but let's get a clear definition from  Wikipedia <https://en.wikipedia.org/wiki/R_(programming_language)>

  > **According to Wikipedia: ** R is a programming language and free software environment for statistical computing and graphics supported by the R Foundation for Statistical Computing. The R language is widely used among statisticians and data miners for developing statistical software and data analysis.

R language provides a wide variety of statistical (linear and nonlinear modelling, classical statistical tests, time-series analysis, classification, clustering, …) and graphical techniques, and is highly extensible. [READ MORE>>](https://www.r-project.org/about.html)

# How to Install and Getting Started With R

Since this article focuses on the basics of R programming language, for instruction on how to install R and R studio please Check this [Edx Article](https://courses.edx.org/courses/UTAustinX/UT.7.01x/3T2014/56c5437b88fa43cf828bff5371c6a924/)

Once you have R and Rstudio installed, let's proceed to the business of the Day.

# Table of Contents

* [What is R](#what-is-r-)
* [How to Install and Getting Started With R](#how-to-install-and-getting-started-with-r)
* [Intro To R Basics](#intro-to-r-basics)
    - [Comments](#comments)  
    - [R Arithmetic Operators](#r-arithmetic-operators)
    - [Basic Data Types in R](#basic-data-types-in-r)
* [More Resources](#more-resources)

# Intro To R Basics

## Hello, World!

It's now like a rule that the first code you write when beginning to learn a programming language is a code that will display `Hello, World!` on the screen.

In order to display on the screen, R provides the [`print()`](https://www.rdocumentation.org/packages/base/versions/3.6.2/topics/print) function.
  > `print` prints its argument and returns it *invisibly*

In order to print `Hello, World!` in R, you need to pass the string `"Hello, World!"` in the `print()` function. the strings can be in double quotes `""` or single quotes `''`.
``` python
print("Hello, World!")
```
the output will be as follows:
```python
[1] "Hello, World!"
```

## Creating and Naming Variables

Variables helps your program claim a piece of memory when it's running. In R, variables allow you to store a value or an object. In simple terms, a variable is a named storage space. The variables created can later on be used in your program to perform various operations. 
In R, `<-`, `=` or `->` are used as the Assignment Operator to assign values to a variable name. Before creating variables, you must adhere to the rules of creating a Variable in R.

### Rules for Naming Variables in R

* Variable names **MUST** start with a letter, it can contain a letter, number, underscore (`_`) and period (`.`).

    > unlike other languages, **Underscore(`_`)** at the beginning of the variable name are **NOT** allowed in R

* Keywords **CANNOT** be used to name variables
* Special Character like `#`, or `&` and whitespace eg tab or space **CANNOT** be used in variable names
* Variable names are **Case Sensitive**, therefore, `my_name` is different from `my_Name`.

%[https://twitter.com/VictorOmondi197/status/1256312066224332805]

Below are examples of correct variable names and assignment in R
```python
age <- 17
age
```
```python
[1] 17
```
```python
name.first = "Victor"
name.first
```
```python
[1] "Victor"
```
```python
17347.3847 -> weight_kgs
weight_kgs
```
``` python
[1] 17347.38
```

## R Arithmetic Operators

An **operator** is a symbol that tells the compiler to perform specific mathematical or logical manipulations. R Arithmetic Operators are symbols that tells the compiler which mathematical operation to perform. R language supports the following arithmetic operators:

|Arithmetic Operator|Function|Description|Example|Output|
|---|---|---|---|---|
|`+`|Addition|adds a number to another number|`3+2`|`[1] 5`|
|`-` |Subtraction|subtracts a number from another number|`3 - 2`|`[1] 1`|
|`*`|Multiplication|multiplies number with another number|`3 * 2`|`[1] 6`|
|`/` |Division|splits a number into equal parts|`3/2`|`[1] 1.5`|
|`^`|Exponentiation|raising a number to the power of another number|`3 ** 2`|`[1] 9`|
|`%%`|Modulo|The modulo returns the remainder of the division of the number to the left by the number on its right|`3 %% 2`|`[1] 1`|

Let us use R arithmetic operators to calculate my age. We will use the already gained knowledge of variables and arithmetic operations we've discussed above. 

```python
year_of_birth = 2001
current_year = 2020
age = current_year - year_of_birt
age
```
```bash
[1] 19
```

As you can see `age` is a variable that stores the computations done when **subtracting** `year_of_birth` from `current_year`.

## Comments
R makes use of the `#` sign to add comments. Comments are added to a source code so that you and others can understand what the R code is about. Comments are not run as R code, so they will not influence your programs computation computations. 

```python
# My year of Birth
year_of_birth = 2001

# The Current Year
current_year = 2020

# Calculating my age by subtracting year_of_birth from the current_year
age = current_year - year_of_birth
age
```
```python
[1] 19
```

## Basic Data Types in R

There are numerous data types in R programming language, we will cover the `4` basic types, that is, **numerics**, **integers**, **logical** and **characters**

> Data type is the classification/categorization of data item. Everything in python is an object therefore, data types are classes and variables are the instance (object) of the data type.
Use `class(variable_name)` in order to understand to which data type a variable belongs.

To get you started with R Basic Data types, note the following:

> * Decimal values are called **numerics**
> * Natural Numbers are called **Integers**, **Integers** are also **numerics**
> * Boolean values, eg( `FALSE` or `TRUE`) are called **logical**. R is case sensitive, logicals must be in **UPPERCASE**
> * String values/text values are called **characters**

In the following code, we will create variables then use `class()` to check to which data type they belong.
```python
my_age = 14
class(my_age)

my_weight = 90.6
class(my_weight)

my_name = "Victor" #Note how the quotation marks on the right indicate that "Victor" is a character
class(my_name)

is_teenager = TRUE
class(is_teanager)
```
```python
[1] "numeric"
[1] "numeric"
[1] "character"
[1] "logical"
```

# More Resources

* R Introduction | R Tutorial: [link](http://www.r-tutor.com/r-introduction)
* Introduction to R Online Course | DataCamp: [link](https://learn.datacamp.com/courses/free-introduction-to-r)
* Google

# Programs

* [Moringa School Data Science Full-Time Course](https://moringaschool.com/programs/data-science-course/)
* [Data Camp Data Science](https://www.datacamp.com/)
* [Data Quest](https://dataquest.io)

And that marks the end of this article, keep an eye for more R articles as I cover more of R programming language to get you started in Data Science with R. Have any question? Ask Me on Twitter:

%[https://twitter.com/VictorOmondi1997]


![Basics To R Programming Language (1).jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1588773966695/RSIRtxGuO.jpeg)

<!-- TOC --><a name="author"></a>
# Author

**Khoi, Hoang Bao Khoi Nguyen**

<!-- TOC --><a name="table-of-contents"></a>
# Table of contents

<!-- TOC start -->

- [Author](#author)
- [Table of contents](#table-of-contents)
   * [Algorithms](#algorithms)
   * [Programming languages](#programming-languages)
   * [Intepreter and compiler](#intepreter-and-compiler)
   * [Printing](#printing)
   * [Operators](#operators)
   * [Errors](#errors)
   * [However](#however)
      + [Syntax error](#syntax-error)
      + [Runtime error](#runtime-error)
      + [Logic error](#logic-error)
      + [Semantic error](#semantic-error)
   * [N.B.](#nb)
   * [Types](#types)
   * [Assign values to variables](#assign-values-to-variables)
   * [Names in Python](#names-in-python)
   * [Operations on string](#operations-on-string)
   * [Get user's input](#get-users-input)
   * [Formatting](#formatting)
      + [str.format()](#strformat)
      + [String Modulo (%)](#string-modulo-)
      + [Template Strings](#template-strings)
      + [f-strings](#f-strings)
         - [Dynamic Expressions inside f-strings (Cool tricks):](#dynamic-expressions-inside-f-strings-cool-tricks)
   * [Some builtin functions](#some-builtin-functions)
   * [Filter](#filter)
   * [Map](#map)
   * [Reduce](#reduce)
   * [Boolean expressions](#boolean-expressions)
   * [Logical operators](#logical-operators)
   * [Special logical operators](#special-logical-operators)
   * [Condition](#condition)
   * [Try - Except:](#try-except)
   * [Pass, Continue, Break](#pass-continue-break)
   * [Indexing and slicing](#indexing-and-slicing)
   * [Sequence data type](#sequence-data-type)
   * [Some definitions about looping](#some-definitions-about-looping)
   * [List](#list)
   * [Here are some cool tricks with list](#here-are-some-cool-tricks-with-list)
   * [String](#string)
   * [Here are some cool tricks with string](#here-are-some-cool-tricks-with-string)
   * [Tuple](#tuple)
   * [Set](#set)
   * [Dictionary](#dictionary)
   * [Here are some cool tricks with dictionary](#here-are-some-cool-tricks-with-dictionary)
   * [Zipping](#zipping)
   * [File reading](#file-reading)
      + [Some functions to work with file](#some-functions-to-work-with-file)
   * [OS](#os)
   * [While loop](#while-loop)
   * [For loop](#for-loop)
   * [Function](#function)
   * [Testing](#testing)
      + [Assert](#assert)
      + [Doctest](#doctest)
      + [Pytest](#pytest)
      + [IPytest](#ipytest)
      + [Doctest vs Pytest](#doctest-vs-pytest)
   * [JSON](#json)
   * [CSV](#csv)
      + [csv.reader()](#csvreader)
      + [csv.writer()](#csvwriter)
      + [csv.DictReader()](#csvdictreader)
   * [Comprehensions](#comprehensions)
      + [List Comprehensions](#list-comprehensions)
      + [Dictionary Comprehensions](#dictionary-comprehensions)
      + [Set Comprehensions](#set-comprehensions)
      + [Some cool tricks with comprehension](#some-cool-tricks-with-comprehension)
   * [Generator](#generator)
   * [Regular Expression (re)](#regular-expression-re)
      + [Special Characters](#special-characters)
      + [Character Classes](#character-classes)
      + [Sets](#sets)
   * [But what if you can't remember everything of these](#but-what-if-you-cant-remember-everything-of-these)
   * [Exploratory Data Analysis](#exploratory-data-analysis)
      + [Structured data](#structured-data)
      + [Rectangular data](#rectangular-data)
      + [Pandas](#pandas)
      + [Location measures](#location-measures)
         - [Another way to calculate those location measures in Python: statistics library](#another-way-to-calculate-those-location-measures-in-python-statistics-library)
      + [Variability measures](#variability-measures)
      + [Data distribution](#data-distribution)
   * [OOP](#oop)
   * [Class](#class)
      + [Attributes](#attributes)
      + [Methods](#methods)
      + [Properties](#properties)
   * [Inheritance](#inheritance)
   * [Decorator](#decorator)
   * [Recursion](#recursion)
   * [Recursive data types](#recursive-data-types)
      + [Binary tree](#binary-tree)
   * [Searching](#searching)
      + [Linear search](#linear-search)
      + [Binary Search](#binary-search)
      + [Jump Search](#jump-search)
      + [Interpolation Search](#interpolation-search)
      + [Exponential Search](#exponential-search)
      + [Fibonacci Search](#fibonacci-search)
      + [Breadth-First Search (BFS) and Depth-First Search (DFS)](#breadth-first-search-bfs-and-depth-first-search-dfs)
      + [A* Search Algorithm](#a-search-algorithm)
   * [Sorting](#sorting)
      + [Built-in sort() function](#built-in-sort-function)
      + [Built-in sorted() function](#built-in-sorted-function)
      + [Bubble Sort](#bubble-sort)
      + [Insertion Sort](#insertion-sort)
      + [Quick Sort](#quick-sort)
      + [Merge Sort](#merge-sort)
   * [Timing the function](#timing-the-function)
      + [Time module](#time-module)
      + [timeit module](#timeit-module)
      + [And you can do some magic with this:](#and-you-can-do-some-magic-with-this)
      + [Decorator](#decorator-1)
      + [Or if you use jupyter notebook, we can use the magic command `%%time`:](#or-if-you-use-jupyter-notebook-we-can-use-the-magic-command-time)

<!-- TOC end -->

<!-- TOC --><a name="algorithms"></a>
## Algorithms

An algorithm is a step-by-step procedure to solve a particular problem or to achieve a specific outcome. It’s like a recipe that describes the exact steps needed for a computer to solve a problem or reach a goal.

**Example of algorithm:** Bubble sort algorithm, this is a simple sorting algorithm that repeatedly steps through the list, compares adjacent elements and swaps them if they are in the wrong order. The pass through the list is repeated until the list is sorted.


```python
def bubble_sort(list):
    for i in range(len(list)):
        for j in range(len(list) - 1):
            if list[j] > list[j + 1]:
                # Swap
                list[j], list[j + 1] = list[j + 1], list[j]
    return list

numbers = [64, 34, 25, 12, 22, 11, 90]
print(bubble_sort(numbers))
```

    [11, 12, 22, 25, 34, 64, 90]


<!-- TOC --><a name="programming-languages"></a>
## Programming languages

Programming languages are tools that allow developers to write instructions for computers to execute. They provide a way for humans to communicate with machines in a format that both can understand.

In this course, we are using python:


```python
print("Hello world!")
```

    Hello world!


<!-- TOC --><a name="intepreter-and-compiler"></a>
## Intepreter and compiler

Programming languages are tools that allow developers to write instructions for computers to execute. They provide a way for humans to communicate with machines in a format that both can understand.

Differences:

- An interpreter translates and executes code line by line. If it encounters an error, it stops at that point without executing the rest of the program.

- A compiler translates the entire program into machine code before execution. If there are any errors, they are reported after the compilation process, not during runtime.

<!-- TOC --><a name="printing"></a>
## Printing

To print in python, we use the function print.

Syntax is 

> `print(value, sep=' ', end='\n')`

'\n' means new line


```python
print("Hello world!")
```

    Hello world!



```python
print("Hello world!", sep = "-")
```

    Hello world!



```python
print("Hello world!", end = "---")
print("abc")
```

    Hello world!---abc


<!-- TOC --><a name="operators"></a>
## Operators

| Notation | Meaning |
----|-----------------
| + | Plus           |
| - | Minus          |
| * | Multiplication |
|  /  | Division       |

**Some other notations:**


```python
print(2 ** 3) # 2 to the power of 3 in 2 ways
print(pow(2, 3))
```

    8
    8



```python
5 % 2 # Modulus, find the remainder when dividing
```




    1




```python
7 // 2 # Floor division, round down the value and return an integer
```




    3



<!-- TOC --><a name="errors"></a>
## Errors

There are a lot of types of errors, knowing the total amounts of error is nearly impossible. Here are some errors that are derived from 'Exception' and 'BaseException':


```python
print([err.__name__ for err in BaseException.__subclasses__()])
```

    ['Exception', 'GeneratorExit', 'SystemExit', 'KeyboardInterrupt', 'CancelledError', 'AbortThread', 'AbortThread']



```python
print([err.__name__ for err in BaseException.__subclasses__()])
```

    ['Exception', 'GeneratorExit', 'SystemExit', 'KeyboardInterrupt', 'CancelledError', 'AbortThread', 'AbortThread']



```python
print([err.__name__ for err in Exception.__subclasses__()])
```

    ['TypeError', 'StopAsyncIteration', 'StopIteration', 'ImportError', 'OSError', 'EOFError', 'RuntimeError', 'NameError', 'AttributeError', 'SyntaxError', 'LookupError', 'ValueError', 'AssertionError', 'ArithmeticError', 'SystemError', 'ReferenceError', 'MemoryError', 'BufferError', 'Warning', '_OptionError', '_Error', 'error', 'Verbose', 'Error', 'SubprocessError', 'TokenError', 'StopTokenizing', 'ClassFoundException', 'EndOfBlock', 'TraitError', 'Error', 'Error', '_GiveupOnSendfile', 'error', 'Incomplete', 'TimeoutError', 'InvalidStateError', 'LimitOverrunError', 'QueueEmpty', 'QueueFull', 'Empty', 'Full', 'ArgumentError', 'ZMQBaseError', 'PickleError', '_Stop', 'error', 'error', 'ReturnValueIgnoredError', 'ArgumentError', 'ArgumentTypeError', 'ConfigError', 'ConfigurableError', 'ApplicationError', 'KeyReuseError', 'UnknownKeyError', 'LeakedCallbackError', 'BadYieldError', 'ReturnValueIgnoredError', 'Return', 'InvalidPortNumber', 'error', 'LZMAError', 'RegistryError', '_GiveupOnFastCopy', 'NoIPAddresses', 'BadZipFile', 'LargeZipFile', 'Error', 'BadEntryPoint', 'NoSuchEntryPoint', 'DuplicateKernelError', 'ErrorDuringImport', 'NotOneValueFound', 'CannotEval', 'OptionError', 'BdbQuit', 'Restart', 'ExceptionPexpect', 'PtyProcessError', 'FindCmdError', 'HomeDirError', 'ProfileDirError', 'IPythonCoreError', 'InputRejected', 'GetoptError', 'ErrorToken', 'PrefilterError', 'AliasError', 'Error', 'Warning', 'SpaceInInput', 'DOMException', 'ValidationError', 'EditReadOnlyBuffer', '_Retry', 'InvalidLayoutError', 'HeightIsUnknownError', 'GuardRejection', 'ParserSyntaxError', 'InternalParseError', '_PositionUpdatingFinished', 'SimpleGetItemNotFound', 'UncaughtAttributeError', 'HasNoContext', 'ParamIssue', '_JediError', 'OnErrorLeaf', 'InvalidPythonEnvironment', 'MessageError', 'Error', 'HTTPException', 'InteractivelyDefined', 'KillEmbedded', 'Error', 'ZombieProcessError', 'QueueEmpty', 'QueueFull', 'DebuggerInitializationError', 'ExpatError', 'Error', 'ParserSyntaxError', 'ResolutionError', '_Error', 'UnableToResolveVariableException', 'InvalidTypeInArgsException', 'DistutilsError', 'CCompilerError', 'Error', 'ParserSyntaxError']


*If you want to know more about the errors that are not listed, visit this link: https://docs.python.org/2/library/exceptions.html#exception-hierarchy*

<!-- TOC --><a name="however"></a>
## However

During the lecture, we are taught that there are 4 types of main errors:

- Syntax errors
- Runtime errors
- Logic errors
- Semantic errors

<!-- TOC --><a name="syntax-error"></a>
### Syntax error

These are errors where the code is not valid (generally syntax or indentation errors). The Python interpreter can’t understand the code. For example, forgetting to close a parenthesis:


```python
print("Hello, World!" 
```


      Cell In[52], line 1
        print("Hello, World!"
                              ^
    SyntaxError: incomplete input



<!-- TOC --><a name="runtime-error"></a>
### Runtime error

A runtime error is an error that occurs during the execution of a program. These errors are typically detected after the syntax of the code has been checked and are usually caused by illegal operations such as division by zero or attempting to access out-of-bounds array elements. Runtime errors can also be caused by resources not being available, like trying to open a file that doesn’t exist.

For example, dividing by zero:

(However, `ZeroDivisionError` can also be seen as logic error in the case that the code is `a/b` and `b` happens to be `0` unintentionally.)


```python
print(5 / 0)
```


    ---------------------------------------------------------------------------

    ZeroDivisionError                         Traceback (most recent call last)

    Cell In[53], line 1
    ----> 1 print(5 / 0)


    ZeroDivisionError: division by zero


<!-- TOC --><a name="logic-error"></a>
### Logic error

A logic error occurs when a program doesn’t perform as intended due to a flaw in the program’s logic or algorithm. The syntax of the code is correct, but the result is not what you expected.

For example, if you wrote a program to calculate the sum of two numbers but instead it subtracts them, that would be a logic error:


```python
def add_two_numbers(a, b):
    return a - b 
print(add_two_numbers(2, 2)) # Gives 0 instead of 4
```

    0


<!-- TOC --><a name="semantic-error"></a>
### Semantic error

A semantic error is when a programmer misunderstands how the programming language works and writes code that doesn’t make sense in the context of the language’s rules. The code may be syntactically correct, but it violates the rules or “semantics” of the language.

For example, trying to add a string to an integer in Python would be a semantic error because it’s not allowed by the language’s rules. Those are some examples of semantic errors:


```python
a = 123 + 'abc'
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[55], line 1
    ----> 1 a = 123 + 'abc'


    TypeError: unsupported operand type(s) for +: 'int' and 'str'



```python
a = [1, 2, 3]
b = a
b[0] = 5
print(a)  # Outputs [5, 2, 3] instead of [1, 2, 3]
# This code prints [5, 2, 3] because b is a shallow copy of a, so it is pointing to the same address as a
```

    [5, 2, 3]



```python
num1 = input('Enter a number: ')
num2 = input('Enter another number: ')
sum = num1 + num2

print('The sum of', num1, 'and', num2, 'is', sum) # Outputs 12 instead of 3
```

    Enter a number: 1
    Enter another number: 2
    The sum of 1 and 2 is 12


<!-- TOC --><a name="nb"></a>
## N.B.

The code below generates `Memory error`. A `MemoryError` in Python is a type of runtime error. It occurs when an operation runs out of memory during the execution of the program.

In the context of the code below, we could also consider it a `logic error` if we’re expecting the program to handle such large data structures. The logic of creating a list with 10**19 elements is flawed because Python, or any language for that matter, can’t handle such large data structures due to memory limitations.

However, it’s not a `semantic error` because the syntax and usage of the language constructs (in this case, list comprehension) are correct and make sense in the context of Python’s rules. The issue arises from the impracticality of the operation due to hardware limitations, not from a misunderstanding of how Python works.


```python
[i for i in range(10**19)]
```

<!-- TOC --><a name="types"></a>
## Types

These are some builting data types:

- Numeric Types: `int`, `float`, `complex` (complex is not in the course)

- Sequence Types: `list`, `tuple`, `range`

- Text Sequence Type: `str`

- Mapping Type: `dict`

- Set Types: `set`, `frozenset` (immutable set, this is not in the course)

- Boolean Type: `True`, `False`

- None Type: `None`

**Below are some advanced types, which are not in the course**

- Binary Sequence Types: `bytes`, `bytearray`, `memoryview`

- Other Builtin Types: Modules, Classes and Class Instances, Functions, Methods, Code Objects, Type Objects, the Ellipsis Object, the NotImplemented Object, Internal Objects, Iterator Object.


```python
type(12)
```




    int




```python
type({1,2})
```




    set



<!-- TOC --><a name="assign-values-to-variables"></a>
## Assign values to variables

This code is assignning the integer `12` to a box called `a`. The `: int` is called type hint, this is not necessary but in this course, we must include that. (Type hints are to check if the value of that variable is as expected, usually checked by `mypy`)


```python
a: int = 12
```

<!-- TOC --><a name="names-in-python"></a>
## Names in Python

**Rules:**

- It should start with a letter or underscore.
- It cannot start with a number: Can't be `100variable`
- It must only contain letters in the alphabet, numbers and underscores: Can't have names like `my_var$`
- They cannot share the name of a Python keyword: thess includes keywords like `for`, `if`, `while`...
- Names are case-sensitive: `my_var` are different from `MY_VAR`

**Conventions:**

- Variable and function names should be lowercase: `my_var`, `my_func`
- Class names should be CapWords: `MyClass`
- Constant (also class attributes) should be written in capital: `MY_CONSTANT`

**Python keywords:**

`False` `class` `finally` `is` `return`  `None` `continue` `for` `lambda` `try` 

`True` `def` `from` `nonlocal` `while`  `and` `del` `global` `not` `with` 

`as` `elif` `if` `or` `yield`  `assert` `else` `import` `pass` `break`  `except` `in` `raise`

<!-- TOC --><a name="operations-on-string"></a>
## Operations on string

We can use `+` and `*`


```python
'Hello' + ' ' + 'World!'
```




    'Hello World!'




```python
'Hello ' * 2
```




    'Hello Hello '



<!-- TOC --><a name="get-users-input"></a>
## Get user's input


```python
a = input("Say something: ")
print(a + ' something.')
```

    Say something: hello
    hello something.


<!-- TOC --><a name="formatting"></a>
## Formatting

In Python, strings can be formatted using several techniques. However, the most powerful technique is `f-strings`.

<!-- TOC --><a name="strformat"></a>
### str.format()


```python
name = "Alice"
print("Hello, {}!".format(name))
```

    Hello, Alice!


<!-- TOC --><a name="string-modulo-"></a>
### String Modulo (%)


```python
name = "Alice"
print("Hello, %s!" % name)
```

    Hello, Alice!


<!-- TOC --><a name="template-strings"></a>
### Template Strings


```python
from string import Template
name = "Alice"
t = Template('Hello, $name!')
print(t.substitute(name=name))
```

    Hello, Alice!


<!-- TOC --><a name="f-strings"></a>
### f-strings

In Python, `f-strings`, also known as formatted string literals, are a way to embed expressions inside string literals, using curly braces `{}`. The expressions will be replaced with their values when the string is created. The leading f before the string indicates that it is a formatted string.

**Basic usage:**


```python
name = "Alice"
print(f"Hello, {name}!")
```

    Hello, Alice!


**Expressions inside f-strings:**


```python
a = 5
b = 10
print(f"Five plus ten is {a + b}, not {2 * (a + b)}.")
```

    Five plus ten is 15, not 30.


**Precision in f-strings:**


```python
from math import pi
print(f"The value of pi to two decimal places is {pi:.2f}")
```

    The value of pi to two decimal places is 3.14


<!-- TOC --><a name="dynamic-expressions-inside-f-strings-cool-tricks"></a>
#### Dynamic Expressions inside f-strings (Cool tricks):


```python
item = "apple"
count = 5
print(f"There {'is' if count == 1 else 'are'} {count} {item if count == 1 else item+'s'}.")
```

    There are 5 apples.


<!-- TOC --><a name="some-builtin-functions"></a>
## Some builtin functions

`min()`: Returns the smallest item in an iterable or the smallest of two or more arguments.

```python
print(min(1, 2, 3, 4))  # Output: 1
```

`max()`: Returns the largest item in an iterable or the largest of two or more arguments.
```python
print(max(1, 2, 3, 4))  # Output: 4
```

`abs()`: Returns the absolute value of a number.
```python
print(abs(-5))  # Output: 5
```

`len()`: Returns the number of items in a container.
```python
print(len("Hello"))  # Output: 5
```

`divmod(x,y)`: Takes two numbers and returns a pair of numbers (a tuple) consisting of their quotient and remainder.
```python
print(divmod(8, 3))  # Output: (2, 2)
```

`pow(x,y)`: Returns x to the power y.
```python
print(pow(2, 3))  # Output: 8
```

`pow(x,y,z)`: Returns x to the power y, modulo z.
```python
print(pow(2, 3, 3))  # Output: 2
```

`round(num, y)`: Rounds a number to a certain number of precision digits.
```python
print(round(3.14159, 2))  # Output: 3.14
```

`isinstance(x,y)`: Checks if the object (first argument) is an instance or subclass of classinfo class (second argument).
```python
print(isinstance(5, int))  # Output: True
```

`range()` and `xrange()`: These are functions to generate lists of numbers. 
- `range()` returns a list
- `xrange()` returns an xrange object, which is kind of like an iterator and generates the numbers on demand.
(Note: In Python 3.x, xrange() has been deprecated and range() now behaves like xrange() used to behave.)

<!-- TOC --><a name="filter"></a>
## Filter

The `filter()` function constructs an iterator from elements of an iterable for which a function returns true.
```python
def is_even(num):
    return num % 2 == 0

even_numbers = filter(is_even, range(10))
print(list(even_numbers))  # Output: [0, 2, 4, 6, 8]
```

<!-- TOC --><a name="map"></a>
## Map

The `map()` function applies a given function to each item of an iterable (such as list, tuple etc.) and returns a list of the results.
```python
def square(num):
    return num ** 2

squared = map(square, range(10))
print(list(squared))  # Output: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

<!-- TOC --><a name="reduce"></a>
## Reduce

The `reduce()` function is a part of `functools` module (in Python 3.x) and it applies a rolling computation to sequential pairs of values in a list. 
```python
from functools import reduce

def multiply(x,y):
    return x * y

product = reduce(multiply, [1, 2, 3, 4])
print(product)  # Output: 24
```

<!-- TOC --><a name="boolean-expressions"></a>
## Boolean expressions

| **Operator** | **Purpose** |
|:----------|:---------|
| `==` | x is  equal to y |
| `!=` | x is not equal to y |
| `x > y` | x is greater than y |
| `x < y` | x is less than y |
| `x >= y` | x is greater than or equal to y | 
| `x <= y` | x is less than or equal to y | 

<!-- TOC --><a name="logical-operators"></a>
## Logical operators

| Operator | Technical name | Math symbol | Python construct | 
|:--------:|:--------------:|:------:|:------:|
| And      | Conjunction    | $\land$| `and`  |
| Or       | Disjunction    | $\lor$ | `or`   |
| Not      | Negation       | $\lnot$| `not`  |

<!-- TOC --><a name="special-logical-operators"></a>
## Special logical operators

The `in` keyword in Python is used to check if a value exists in a sequence like a `list`, `tuple`, `string`, or `dictionary`. It’s also used to iterate through a sequence in a loop.

Here's an example of using `in` to check if a value if in a `list`:


```python
numbers = [1, 2, 3, 4, 5]
if 3 in numbers:
    print("3 is in the list")
```

    3 is in the list


You can also use `in` in `for` loop to iterate over a sequence:


```python
for number in numbers:
    print(number)
```

    1
    2
    3
    4
    5


The `in` keyword can also be used with dictionaries to check if a key is present:


```python
person = {"name": "Alice", "age": 25}
if "name" in person:
    print("Name is a key")
```

    Name is a key


<!-- TOC --><a name="condition"></a>
## Condition

**If Statement**


```python
a = 1
if a < 5:
    print(f"{a} < 5")
```

    1 < 5


**If - else statement**


```python
a = 10
if a < 5:
    print(f"{a} < 5")
else:
    print(f"{a} >= 5")
```

    10 >= 5


**If - elif - else statement**


```python
a = 10
if a < 5:
    print(f"{a} < 5")
elif a < 10:
    print(f"5 <= {a} < 10")
else:
    print(f"{a} >= 10")
```

    10 >= 10


**Nested if - else**


```python
a = 10
if a < 5:
    print(f"{a} < 5")
else:
    if a < 10:
        print(f"5 <= {a} < 10")
    else:
        print(f"{a} >= 10")
```

    10 >= 10


<!-- TOC --><a name="try-except"></a>
## Try - Except:

```python
try:
        # Some Code.... 

except:
        # optional block
        # Handling of exception (if required)

else:
       
        # execute if no exception

finally:
        # Some code .....(always executed)
```


```python
a = 'abc'
try: 
    a += 1
except:
    print("Errors")
else:
    print("Done")
finally:
    print("Always see this")
```

    Errors
    Always see this


<!-- TOC --><a name="pass-continue-break"></a>
## Pass, Continue, Break


```python
if 10 < 11:
    pass # Do nothing
```


```python
for i in range(3):
    if i == 1:
        continue # skip an iteration
    print(i)
```

    0
    2



```python
for i in range(5):
    if i == 2:
        break # break the loop
    print(i)
```

    0
    1


<!-- TOC --><a name="indexing-and-slicing"></a>
## Indexing and slicing

Can be used for string, list, tuple, set

Syntax:
> `some_list[start:end:step]`

Any of the three (start, end, step) can be missing


```python
a = 'abcdef'
a[0]
```




    'a'




```python
a[1:]
```




    'bcdef'




```python
a[:3]
```




    'abc'




```python
a[:-1]
```




    'abcde'




```python
a[::]
```




    'abcdef'




```python
a[:]
```




    'abcdef'



**Cool trick to revert a string/list/set/...**


```python
a[::-1]
```




    'fedcba'



<!-- TOC --><a name="sequence-data-type"></a>
## Sequence data type

A collection of data can be **stored** in a **tuple**, **list**, **set**, or **dictionary**. The difference between using one or the other will depend on the properties you need to represent your data. In the following table, we briefly present the properties of each of these collections.

| Collection | Mutable | Ordered | Allows duplicates | Indexed | Representation |
|------------|:-------:|:-------:|:----------------:|:-------:|:--------------:|
| `tuple` | ✖︎ | ✔︎ | ✔︎ | ✔︎ | `(...)` |
| `list`  | ✔︎ | ✔︎ | ✔︎ | ✔︎ | `[...]` |
| `set`   | ✔︎ | ✖︎ | ✖︎ | ✖︎ | `{...}` |
| `dict`  | ✔︎ | ✖︎ | ✖︎ | ✔︎ * | `{key: val, ...}` |

<sup>*</sup> You access key-value pairs via a key.

<!-- TOC --><a name="some-definitions-about-looping"></a>
## Some definitions about looping

- **Iterable** is an object which you can iterate over, with `__iter__()` method. `List`, `Set`, `File`... are iterables.

- **Iterator** is an object which is used to iterate through an iterable using `__next__()` method.

- **Iteration** is a general term of describing 1 loop

<!-- TOC --><a name="list"></a>
## List

> `len(lst)`

Return the length of the list

> `lst.append(value)`

Append a value to list

> `lst.clear()` 

Remove all items from list

> `lst.copy()` 

Create a shallow copy of the list

> `lst.count(value)` 

Count the number of occurences of value

> `lst.extend(iterable)` 

Extend the list with another iterable (another list, tuple, set...)

> `lst.index(value)` 

Return the first index of the value

> `lst.insert(value, index)` 

Append the value to the given index

> `lst.pop(index)`

Remove the value at the given index

> `lst.remove(value)`

Remove the first occurence of value

> `lst.sort(reverse = False)`

Sort the list, reverse = False means sorting in ascending order

<!-- TOC --><a name="here-are-some-cool-tricks-with-list"></a>
## Here are some cool tricks with list

**Getting the value with highest occurences in a list:**


```python
lst = [1,2,3,1,1,2,3,1,1,3] # 10 values
max(lst, key = lst.count)   # 10*10 iterations
```




    1



However, in the solution above, max() function loops through `10*10` iterations. Here is a more efficient approach (by transforming `lst` to a set, now `lst` will only have 3 values):


```python
lst = [1,2,3,1,1,2,3,1,1,3]    # 10 values
max(set(lst), key = lst.count) # max loops through 3*10 iterations
```




    1



**Print all duplicates values in a list as a set:**


```python
lst = [1,1,2,3,3,1,3]
sett = set()
dupes = {x for x in lst if x in sett or sett.add(x)}
dupes
```




    {1, 3}



<!-- TOC --><a name="string"></a>
## String

> `s.casefold()` or `s.lower()`

Make all characters lowercase, but casefold() also cover non - ASCII letters

> `s.upper()`

Make all characters uppercase

> `s.capitalize()`

Capitalize every first characters of each words

> `s.isdigit()`

Check if string `s` is digit

> `'-'.join(A_List)`

Turn every values in the list to a string. Ex: A_List = [1,2,3]. Then we will get '1-2-3'

> `s.strip(".")`

Remove every dots in the string

> `s.rstrip(".")` or `s.lstrip(".")`

Remove the first right/left dot occured going from right/left side

> `s.split(".")`

Split the given string into list of strings, with the `.` as separator.

Ex: `s = "a.b.c"` Then we will get `['a', 'b', 'c']`

> `len(s)`

Return the length of string `s`

<!-- TOC --><a name="here-are-some-cool-tricks-with-string"></a>
## Here are some cool tricks with string

**Transforming a string to a list of characters:**

Normally, to do this, we would create an empty list, then loop through the string and append each character into that list. However, here is a better approach (The asterisk `*` notation is an unpacking notation, it means that it unpack the string and then use the `[]` to make it a list):


```python
s = "abcdefghijk"
[*s]
```




    ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k']



**And you can do the same for dictionary, but you have to use double asterisks:**


```python
def f(a, b, c):
    print(a, b, c)
f(**{'a': 1, 'b': 2, 'c': 3})
```

    1 2 3


**You can even do some magic like this:**


```python
def f(a, *b, **c):
    print(a)
    print(b)
    print(c)
f(1, 'x', 'y', 'z', dev = 'None', abc = 'NaN')
```

    1
    ('x', 'y', 'z')
    {'dev': 'None', 'abc': 'NaN'}


**Or this, when someone wants you to calculate the mean value but they don't provide how many parameters must be given:**


```python
def f(*a):
    return sum(a) / len(a)
f(1,2)
```




    1.5



**And here's a different notation for integer:**


```python
a = 1_000_000
b = 2_000
c = a + b

print(c)
print(f'{c:,}')
```




    1002000
    1,002,000


**Attention:**


```python
letter = 'A'

if letter = 'B' or 'C' or 'D':
	print(1)
else:
	print(0)
```




    1


This is because the above piece of code is equivalent to this below code, and 'C' and 'D' is a character so it will return True.

```python
letter = 'A'

if (letter = 'B') or ('C') or ('D'):
	print(1)
else:
	print(0)
```

So to fix:

```python
letter = 'A'

if letter in ['B', 'C', 'D']:
	print(1)
else:
	print(0)
```




    0



<!-- TOC --><a name="tuple"></a>
## Tuple

You can use tuple for information that you don't want to modify, like a tuple of `(student_id, name, grade)`

> `tup.count(value)`

Count the number of occurences of that value in the tuple

> `tup.index(value)`

Return the first index of value

<!-- TOC --><a name="set"></a>
## Set

You can use set when you don't want duplicates or you want to sort a sequence

> `set.add(value)`

Add a value to set (for set, you need to use .add() instead of .append(), this is a design choice of python)

> `set.clear()`

Clear all values in set

> `set.copy()`

Make a shallow copy of the set

> `set.difference(another_set)`

Return the difference of two or more sets as a new set.

> `set.intersection(another_set)`

Return the intersection of two sets as a new set.

> `set.pop()`

Remove the first value of the set once at a time.
Ex: sett = {1,2,3,4}
	sett.pop()
    # {2,3,4}
    
> `set.remove(value)`

Remove `value` from the set

> `set.union(another_set)`

Return the union of sets as a new set.

<!-- TOC --><a name="dictionary"></a>
## Dictionary

> `dct.clear()`

Clear dictionary

> `dct.copy()`

Make a shallow copy of the dictionary

> `dct.get(key, value)`

Return the value for key if key in in dictionary, if key is not in dictionary, return value (By default, value is `None`)

> `dct.items()`

Return an iterator of tuples (key, value)

> `dct.keys()`

Return an iterator of keys

> `dct.values()`

Return an iterator of values

> `dct.fromkeys(iterable)`

Create a new dictionary with keys from iterable and values set to value.

<!-- TOC --><a name="here-are-some-cool-tricks-with-dictionary"></a>
## Here are some cool tricks with dictionary

**Remove duplicate values in a list without changing the order:**

Below, I am creating a new dictionary with values of the list `lst` as key, and since keys in dictionary are unique, it will remove duplicates, as well as preserved the order because dictionary is unordered. Then I transform it to a list again using `list()`


```python
lst = [1, 2, 5, 4, 3, 1, 1, 2, 3, 5, 4, 2, 1]

list(dict.fromkeys(lst))
```




    [1, 2, 5, 4, 3]



**Consider the index of keys - values in dictionary using `enumerate()`:**


```python
dct = {'a': 'first', 'b': 'second', 'c': 'third'}
print(list(enumerate(dct)))          # Considering the keys
print(list(enumerate(dct.values()))) # Considering the values
print(list(enumerate(dct.items())))  # Considering the keys - values pair
```

    [(0, 'a'), (1, 'b'), (2, 'c')]
    [(0, 'first'), (1, 'second'), (2, 'third')]
    [(0, ('a', 'first')), (1, ('b', 'second')), (2, ('c', 'third'))]


**Sorting the dictionary by values:**


```python
dct = {'a': 1, 'b': 3, 'c': 2, 'd': 8, 'e': 5}
{k:v for k,v in sorted(dct.items(), key = lambda item: item[1])}
```




    {'a': 1, 'c': 2, 'b': 3, 'e': 5, 'd': 8}




```python
{k:v for k,v in sorted(dct.items(), key = lambda item: item[1], reverse = True)} # For descending order
```




    {'d': 8, 'e': 5, 'b': 3, 'c': 2, 'a': 1}



**Counting the number of occurrences of a value in a list:**


```python
lst = [1,2,3,4,2,1,32,3,4,1,5,3,6,7,3,1]
dct = {}
for i in lst:
    dct[i] = dct.get(i, 0) + 1
dct # The number `1` occurred 4 times...
```




    {1: 4, 2: 2, 3: 4, 4: 2, 32: 1, 5: 1, 6: 1, 7: 1}



**Dictionary aggregation:**


```python
a = {'apple':1, 'banana':2}
b = {'apple':1, 'banana':3, 'lemon':2}

dct = {k: a.get(k, 0) + b.get(k, 0) for k in zip(a | b)}
dct
```




    {'apple':2, 'banana':5, 'lemon':2}



<!-- TOC --><a name="zipping"></a>
## Zipping

The zip() function in Python is a built-in function that allows you to combine corresponding elements from multiple iterable objects (like lists, tuples, etc.) into a single iterable. This resulting iterable contains tuples, where the i-th tuple contains the i-th element from each of the argument sequences or iterables.


```python
lst1 = (1, 2, 3)
lst2 = [4, 5, 6, 7]
list(zip(lst1, lst2))
```




    [(1, 4), (2, 5), (3, 6)]



<!-- TOC --><a name="file-reading"></a>
## File reading

**Syntax**

```python
file = open("Path_to_file", 'r')
```

**Note**

Always close the file after opening to save changes to the file and avoid file corruption.

```python
file.close()
```

**Modes when reading a file**

|Character | Meaning|
|--------- | ---------------------------------------------------------------|
|'r'       | open for reading (default)|
|'w'       | open for writing, truncating the file first|
|'x'       | create a new file and open it for writing|
|'a'       | open for writing, appending to the end of the file if it exists|
|'b'       | binary mode|
|'t'       | text mode (default)|
|'+'       | open a disk file for updating (reading and writing)|
|'U'       | universal newline mode (deprecated)|

**Another way**

```python
with open("Path_to_file", 'r') as file:
    # some codes
```

This syntax will auto close the file.

<!-- TOC --><a name="some-functions-to-work-with-file"></a>
### Some functions to work with file

**Read the whole files:**
```python
file.read()
```

**Find a line that start with a letter:**
```python
for line in file:
    line.startwith('letter')
```

**Find a letter:**
```python
for line in file:
    line.find('letter')
```

**Writes a string to a files:** (If you want to write on a new line, you need to include the newline character (\n).)
```python
file.write(str)
```

<!-- TOC --><a name="os"></a>
## OS

The `os` module in Python provides functions for interacting with the operating system. This module comes under Python’s standard utility modules, so when you install Python, the os module is automatically included.

To use the functions provided by the os module, you need to import it into your Python script.
```python
import os
```

**Here are a few examples of what you can do with the os module:**

> `os.name`

This function gives the name of the imported operating system dependent module.

> `os.getcwd()`

This function allows you to see what your current working directory is.

> `os.listdir()`

This function allows you to see all the files in the directory you specify.

> `os.mkdir()`

This function allows you to create a new directory.

> `os.rename()`

This function allows you to rename a file or a directory.

> `os.getcwd()`

This function returns the current working directory (cwd) as a string. This is the folder where your Python script is being executed.

> `os.path.abspath()`

This function returns the absolute path of a file or directory. An absolute path is the complete address of a file or directory, starting from the root directory.

> `os.path.exists()`

This function checks if a file or directory exists at the given path. It returns True if the file or directory exists and False otherwise.

> `os.path.isdir()`

This function checks if the path exists and is a directory. It returns True if the path is a directory and False otherwise.

> `os.walk()`

This function generates the file names in a directory tree by walking the tree either top-down or bottom-up. For each directory in the tree rooted at directory top (including top itself), it yields a 3-tuple (dirpath, dirnames, filenames).

<!-- TOC --><a name="while-loop"></a>
## While loop

The while loop in Python is used to repeatedly execute a block of statements as long as a given condition is true. The condition is checked before each iteration, and if it evaluates to False, the loop is terminated and control is passed to the next statement in the program.

**Syntax:**
```python
	while condition:
    	# some code
```
        
**Example:**


```python
count = 1
while count <= 5:
    print(count)
    count += 1
```

    1
    2
    3
    4
    5


You can also control the flow of a while loop using `break` and `continue` statements:

The `break` statement allows you to exit the loop prematurely when a certain condition is met.
The `continue` statement allows you to skip the rest of the current iteration and move directly to the next one.
Here’s an example that uses both:


```python
count = 0
while count < 10:
    count += 1
    if count == 3:
        continue  # Skip printing when count is 3
    if count == 8:
        break  # Stop the loop when count is 8
    print(count)
```

    1
    2
    4
    5
    6
    7


**Notes:**
    
The while loop go on as long as the condition in the while loop is True. Hence, we can do something like:


```python
while True:
    a = int(input("Please enter a number: "))
    print(a)
    if a == -1:
        break
```

    Please enter a number: 1
    1
    Please enter a number: -1
    -1


or let say you want to remove every value `-1` out of a list:


```python
lst = [1,2,3,-1,1,-1,-1,5]
while -1 in lst:
    lst.remove(-1)
lst
```




    [1, 2, 3, 1, 5]



<!-- TOC --><a name="for-loop"></a>
## For loop

The for loop in Python is used to iterate over a sequence (like a list, tuple, string, or dictionary) or other iterable objects. Iterating over a sequence is called traversal.

**Syntax:**
```python
    for value in sequence:
    	# Some code
```
**Example:** `For` loop printing every character of a string:


```python
for char in "Hello":
    print(char)
```

    H
    e
    l
    l
    o


You can also use the for loop to iterate over a `list` or `tuple`:


```python
numbers = [1, 2, 3, 4, 5]
for num in numbers:
    print(num)
```

    1
    2
    3
    4
    5


When iterating over dictionaries using a for loop, it traverses the keys of the dictionary by default. If you want to iterate over values or `key-value` pairs, you can use `.values()` and `.items()`, respectively:


```python
person = {"name": "Alice", "age": 25}
for key in person:
    print(key)
```

    name
    age



```python
for value in person.values():
    print(value)
```

    Alice
    25



```python
for key, value in person.items():
    print(key, value)
```

    name Alice
    age 25


<!-- TOC --><a name="function"></a>
## Function

In Python, a function is a block of reusable code that performs a specific task. Functions provide better modularity for your application and allow for code reusability.

**Syntax**:
```python
	def function_name(parameters):
        """docstring"""
        # some code
        return result
```

**If ommitted result, the function will return None**


```python
def add_numbers(a, b):
    """This function adds two numbers"""
    result = a + b
    return result

total = add_numbers(3, 4)
print(total)
```

    7


<!-- TOC --><a name="testing"></a>
## Testing

Testing is a crucial part of software development that involves executing a program or application with the intent of finding software bugs. It can also be used to ensure that the program or application behaves as expected.

<!-- TOC --><a name="assert"></a>
### Assert

**Syntax:**
	
    assert `statement`, `Error message`
    
The `assert` keyword is used in Python for debugging purposes. It tests if a condition is true. If the condition is true, the program continues to execute. If the condition is false, the program stops and throws an `AssertionError` exception. For example:


```python
def add(a, b):
    return a + b

assert add(2, 2) == 4, "Function is wrong"
```


```python
def add(a, b):
    return a - b

assert add(2, 2) == 4, "Function is wrong"
```


    ---------------------------------------------------------------------------

    AssertionError                            Traceback (most recent call last)

    Cell In[108], line 4
          1 def add(a, b):
          2     return a - b
    ----> 4 assert add(2, 2) == 4, "Function is wrong"


    AssertionError: Function is wrong


<!-- TOC --><a name="doctest"></a>
### Doctest

The `doctest` module in Python is used to write tests inside docstrings (In order to use, you must import `doctest`). These tests can be run to verify that the code works as expected. For example:


```python
import doctest
```


```python
def add(a, b):
    """
    This function adds two numbers.
    
    >>> add(2, 2)
    4
    """
    return a + b

doctest.testmod()
```




    TestResults(failed=0, attempted=1)



or you can do:


```python
doctest.run_docstring_examples(add, globals(), verbose = True, name = "add")
```

    Finding tests in add
    Trying:
        add(2, 2)
    Expecting:
        4
    ok


<!-- TOC --><a name="pytest"></a>
### Pytest

`Pytest` is a testing framework in Python that allows you to easily create small, simple tests, yet scales to support complex functional testing for applications and libraries. An example of a simple test:


```python
def add(a, b):
    return a + b

def test_add():
    assert add(2, 2) == 4
```


```python
import ipytest
ipytest.autoconfig() #Configure ipytest
ipytest.run()
```

    [32m.[0m[32m                                                                                            [100%][0m
    [32m[32m[1m1 passed[0m[32m in 0.01s[0m[0m





    <ExitCode.OK: 0>



In `Pytest`, we also have `Fixtures`. `Fixtures` are functions that create data or initialize the state of a program. Tests can use fixtures to avoid duplicating code! To use them, test functions need to explicitly refer to them, and pass the fixture function as an argument! The syntax is as follows:

```python
import pytest

@pytest.fixture
def <fixture_name>():
    # Body
    return <value>

def test_<test_name>(<fixture_name>):
    assert <fixture_name> == ...
```

<!-- TOC --><a name="ipytest"></a>
### IPytest

`IPytest` is a pytest plugin for IPython and Jupyter. It allows you to run pytest inside Jupyter notebooks and IPython interactive shells.

<!-- TOC --><a name="doctest-vs-pytest"></a>
### Doctest vs Pytest

`Doctest` allows you to write tests inside docstrings which can double as documentation. `Pytest` requires separate functions for tests but is more powerful and flexible than doctest. It’s often easier to start with doctest for simple scenarios and switch to pytest as your testing needs become more complex.

<!-- TOC --><a name="json"></a>
## JSON

This is a library which is used to turn json file into a list of dictionary

```python
import json

with open("Path_to_file.json", 'r') as file:
    jsonfile = json.load(file)
```

<!-- TOC --><a name="csv"></a>
## CSV

The `csv` module in Python is used to read from and write to CSV (Comma Separated Values) files. CSV files are a common file format for data manipulation and are supported by many applications, including spreadsheets like Excel, Google Sheets, and database management systems.

<!-- TOC --><a name="csvreader"></a>
### csv.reader()

This function returns a reader object which iterates over lines in the specified CSV file. Here’s an example (In this example, each row read from the CSV file is returned as a list of strings):

```python
import csv

with open('file.csv', 'r') as file:
    reader = csv.reader(file)
    for row in reader:
        print(row)
```

<!-- TOC --><a name="csvwriter"></a>
### csv.writer()

This function returns a writer object responsible for converting the user’s data into delimited strings on the given file-like object. Here’s an example (In this example, data is written to a CSV file using the `writerow()` method):

```python
import csv

with open('file.csv', 'w', newline='') as file:
    writer = csv.writer(file)
    writer.writerow(["SN", "Name", "Contribution"])
    writer.writerow([1, "Linus Torvalds", "Linux Kernel"])
    writer.writerow([2, "Tim Berners-Lee", "World Wide Web"])
```

<!-- TOC --><a name="csvdictreader"></a>
### csv.DictReader()

This function creates an object that operates like a regular reader but maps the information read into a dictionary. The keys for the dictionary can be passed in with the fieldnames parameter or inferred from the first row of the CSV file.

```python
import csv

with open('file.csv', 'r') as file:
    reader = csv.DictReader(file)
    for row in reader:
        print(row)
```

<!-- TOC --><a name="comprehensions"></a>
## Comprehensions

Comprehensions in Python provide a concise way to create lists, dictionaries, and sets based on existing iterables, while also allowing for conditionals and transformations. They’re a key feature of Python that can make your code more readable and efficient.

<!-- TOC --><a name="list-comprehensions"></a>
### List Comprehensions

They create a new list from an existing list (or other iterable) according to some expression. For example:


```python
numbers = [1, 2, 3, 4, 5]
[n**2 for n in numbers]
```




    [1, 4, 9, 16, 25]




```python
# The code above is the same as this code
lst = []
for n in numbers:
    lst.append(n**2)
lst
```




    [1, 4, 9, 16, 25]



<!-- TOC --><a name="dictionary-comprehensions"></a>
### Dictionary Comprehensions
They create a new dictionary from an existing iterable. For example:


```python
numbers = [1, 2, 3, 4, 5]
{n: n**2 for n in numbers}
```




    {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}



<!-- TOC --><a name="set-comprehensions"></a>
### Set Comprehensions

They create a new set from an existing iterable. For example:


```python
numbers = [1, 2, 2, 3, 4, 4, 5, 5]
{n**2 for n in numbers}
```




    {1, 4, 9, 16, 25}



<!-- TOC --><a name="some-cool-tricks-with-comprehension"></a>
### Some cool tricks with comprehension

**If condition in a comprehension:**


```python
numbers = [1, 2, 2, 3, 4, 4, 5, 5]
[i for i in numbers if i > 3]
```




    [4, 4, 5, 5]



**If - else condition in a comprehension:**


```python
numbers = [1, 2, 2, 3, 4, 4, 5, 5]
[i if i > 3 else 'None' for i in numbers]
```




    ['None', 'None', 'None', 'None', 4, 4, 5, 5]



**So what if if-else is at the back (We can't have this, this is design choice):**


```python
numbers = [1, 2, 2, 3, 4, 4, 5, 5]
[i for i in numbers if i > 3 else 'None']
```


      Cell In[120], line 2
        [i for i in numbers if i > 3 else 'None']
                                     ^
    SyntaxError: invalid syntax



**Finding values that are duplicate in a list:**


```python
numbers = [1, 2, 2, 3, 4, 4, 5, 5, 5]
newset = set()
[i for i in numbers if i in newset or newset.add(i)]
```




    [2, 4, 5, 5]



<!-- TOC --><a name="generator"></a>
## Generator

A generator in Python is a special type of function that returns an iterable sequence of results, but instead of computing all the values upfront and storing them in memory (like a list), it generates each value on-the-fly as you iterate over the sequence. This can be very memory-efficient for large sequences where you don’t need all the values at once.

Generators are defined using the `def` keyword, just like regular functions, but instead of returning values using `return`, they use the `yield` keyword (A keyword like return but it returns a generator). Once a generator function calls `yield`, it pauses its execution and outputs its argument. When the next value is requested (for example, in a for loop), it resumes execution immediately after the `yield` statement, with all local state (like variable values) preserved.

The two keywords of a generator are `lazy` and `demand-driven`

In this example, `count_up_to(5)` is a generator that yields the numbers from 1 to 5 one at a time. Each time through the for loop, it prints the current number and then pauses at the yield statement. The next time through the loop, it picks up where it left off at the yield, increments count, and then yields the next number.


```python
def count_up_to(n):
    count = 1
    while count <= n:
        yield count
        count += 1

for number in count_up_to(5):
    print(number)
```

    1
    2
    3
    4
    5


To explain it in detailed, the first time the `for` calls the generator object created from your function, it will run the code in your function from the beginning until it hits `yield`, then it'll return the first value of the loop. Then, each subsequent call will run another iteration of the loop you have written in the function and return the next value. This will continue until the generator is considered empty, which happens when the function runs without hitting `yield` (This can be because the loop has come to an end, or because you no longer satisfy an "if/else").

**Another way of writing a generator is:**


```python
(i for i in range(1, 6))
```




    <generator object <genexpr> at 0x1124b30d0>



**This returns a generator object (which is an iterator). To print its value, we can do:**


```python
for i in (i for i in range(1, 6)):
    print(i)
```

    1
    2
    3
    4
    5


**Another example of a generator using `yield` (This is a function finding the factorial of number `n`):**


```python
def factorial(n):
    if n == 0:
        yield 1
    else:
        yield n * next(factorial(n-1))
next(factorial(5))
```




    120



In this case, I used the method `next()` to get the value of the generator.

<!-- TOC --><a name="regular-expression-re"></a>
## Regular Expression (re)

*You can use the site https://regexr.com/ to test your `re`*

`Regular expressions`, often shortened as `regex`, are a sequence of characters used to check whether a pattern exists in a given text (string) or not. They are used for various tasks like validating the format of email addresses or passwords, parsing text data files to find, replace, or delete certain strings, etc.

In Python, regular expressions are supported by the `re` module. This module provides regular expression matching operations similar to those found in Perl (An intepreted programming language). Both patterns and strings to be searched can be Unicode strings (str) as well as 8-bit strings (bytes).

Here are some of the important functions provided by the re module:

> `re.match(pattern, string)`

This function attempts to match the `pattern` at the start of the `string`.

> `re.search(pattern, string)`

This function searches the `string` for a match to the `pattern`, returning a match object if there’s a match anywhere in the `string`.

> `re.findall(pattern, string)`

This function returns all non-overlapping matches of the `pattern` in the `string` as a list of strings.

> `re.sub(pattern, repl, string)`

This function returns the `string` obtained by replacing the leftmost non-overlapping occurrences of the `pattern` in the string by the replacement `repl`.

> `re.split(pattern, string)`

This function splits the `string` by the occurrences of the `pattern`.

Here’s an example of how you might use these functions:


```python
import re

pattern = r"Cookie"
sequence = "Cookie Monster"
```


```python
# Use re.match()
if re.match(pattern, sequence):
    print("Match!")
else:
    print("Not a match!")
```

    Match!



```python
# Use re.search()
if re.search(pattern, sequence):
    print("Found a match!")
else:
    print("No match found.")

```

    Found a match!



```python
# Use re.findall()
print(re.findall(pattern, sequence))
```

    ['Cookie']



```python
# Use re.sub()
print(re.sub(pattern, "Cake", sequence))
```

    Cake Monster



```python
# Use re.split()
print(re.split(pattern, sequence))
```

    ['', ' Monster']


<!-- TOC --><a name="special-characters"></a>
### Special Characters

| Character | Description |
|:---------:|:------------|
| `^` | Matches the start of a string |
| `$` | Matches the end of a string |
| `.` | Matches any character except new line characters (e.g. `\n`)|
| `\` | Escapes special characters |
| `A\|B` | Matches expression A or B |
| `+` | Greedy match of one-or-more characters |
| `*` | Greedy match of zero-or-more characters |
| `?` | Greedy match of zero-or-one character. If added after a qualifier (i.e. `+`, `*`, `?`) performs non-greedy (or lazy) matches |
| `{n}` | Matches an expression `n` times |
| `{n, m}` | Matches an expression from `n` to `m` times |

<!-- TOC --><a name="character-classes"></a>
### Character Classes

| Character | Description |
|:---------:|:------------|
| `\w` | Matches alphanumeric characters (i.e. a-z, A-Z, 0-9 and \_) |
| `\d` | Matches digits (i.e. 0-9) |
| `\D` | Matches non-digits | 
| `\s` | Matches whitespace characters (e.g. \t, \n, \r) |
| `\S` | Matches non-whitespace characters |
| `\b` | Matches the empty string, but only at the start or end of a word |
| `\B` | Matches the empty string, but not at the start or end of a word |

<!-- TOC --><a name="sets"></a>
### Sets

| Character | Description |
|:---------:|:------------|
| `[ ]` | Contains characters to match |
| `[ab]` | Matches character `a` or `b`, not `ab` |
| `[a-z]` | Matches a lower-case letter from `a` to `z` |
| `[A-Z]` | Matches a capital letter from `A` to `Z` |
| `[0-9]` | Matches a digit from `0` to `9` |
| `[a-zA-Z0-9]` | Matches alphanumeric characters |
| `[+*().]` | Matches special characters as literals |
| `[^ab]` | Matches any character except `a` and `b` |

<!-- TOC --><a name="but-what-if-you-cant-remember-everything-of-these"></a>
## But what if you can't remember everything of these

**Then you can only do the hard way:**

Providing we have to obtain this tuple:
```python
("BIANCA", "Okay -- you're gonna need to learn how to lie.")
```
from this string:
```python
"L872 +++$+++ u0 +++$+++ m0 +++$+++ BIANCA +++$+++ Okay -- you're gonna need to learn how to lie."
```


```python
s = "L872 +++$+++ u0 +++$+++ m0 +++$+++ BIANCA +++$+++ Okay -- you're gonna need to learn how to lie."

match = re.search(r".+\+\+\+\$\+\+\+.+\+\+\+\$\+\+\+.+\+\+\+\$\+\+\+.(.+).\+\+\+\$\+\+\+.(.+)",s)
result = (match.group(1), match.group(2))
result
```




    ('BIANCA', "Okay -- you're gonna need to learn how to lie.")



In the code above, the `.+` means getting every characters, then the `\+` means the plus sign. In regex, special characters must start with the `\` symbol. 

Then, once reached the word `BIANCA`, I used the `.(.+).`, the 2 dots on 2 sides represents the white space. The `()` means grouping, this means I am grouping every character between the 2 dots.

Finally, I reach the character using `match.group()`, and the function `.group()` starts counting from 1.

<!-- TOC --><a name="exploratory-data-analysis"></a>
## Exploratory Data Analysis

This part is self-study, it's not important for this course, but it is for other courses in the future.

Exploratory Data Analysis (EDA) is a method used to analyze and investigate data sets and summarize their main characteristics, often employing data visualization methods.

EDA is primarily used to see what data can reveal beyond the formal modeling or hypothesis testing task. It provides a better understanding of data set variables and the relationships between them. It can also help determine if the statistical techniques you are considering for data analysis are appropriate.

Another main purpose of EDA is to help look at data before making any assumptions. It can help identify obvious errors, as well as better understand patterns within the data, detect outliers or anomalous events, find interesting relations among the variables.

Once EDA is complete and insights are drawn, its features can then be used for more sophisticated data analysis or modeling, including machine learning. In summary, EDA is a crucial step in the data analysis process that allows data scientists to understand the data better, make necessary assumptions, and formulate suitable models for further analysis.

<!-- TOC --><a name="structured-data"></a>
### Structured data

(This part is from the lecture)

Structured data usually comes in two flavors:
* **Numeric:** Represented by numbers and further divided into:
    - **Discrete:** Numerical data that takes integer values (e.g., counts). In Python, these are `int` or `long` values.
    - **Continuous:** Data that can take any numerical value within an interval (e.g., ratios). In Python, these are `float` values.
* **Categorical:** Data that takes a fixed set of values or states, known as levels. It can be:
    - **Nominal:** Categorical data without any order among its levels (e.g., “Yellow”, “Blue”, “Red”).
    - **Binary:** A special case of nominal data with just two levels: true (1) or false (0).
    - **Ordinal:** Categorical data with a natural order (e.g., “Excellent”, “Good”, “Bad”).
    
| Data type   | Category    | Python types  |
|-------------|-------------|---------------|
| Discrete    | Numeric     | `int`, `long` |
| Continuous  | Numeric     | `float`       |
| Nominal     | Categorical | `str`, `int`  |
| Binary      | Categorical | `bool`        |
| Ordinal     | Categorical | `str`, `int`  |

<!-- TOC --><a name="rectangular-data"></a>
### Rectangular data

`Rectangular data`, also known as multivariate cross-sectional data, is a common type of structured data that is used in statistical and machine learning models. It’s often compared to a spreadsheet or a single table in a relational database.

In rectangular data, each column represents a variable (also known as a feature), and each row represents a case or record. This format makes it easy to apply statistical concepts and machine learning algorithms.

Here are some key terms related to rectangular data:

* **Data frame:** Rectangular data is the basic data structure for statistical and machine learning models.
* **Feature:** A column in the table is commonly referred to as a feature. Synonyms include attribute, input, predictor, variable.
* **Outcome:** The variable or result that the model is trying to predict or explain.

Rectangular data can be derived from various sources such as sensor measurements, events, text, images, and videos. For example, text data can be converted to rectangular data where each column represents a word, each row represents a document, and each cell entry represents the frequency or presence/absence of that word in the document.

<!-- TOC --><a name="pandas"></a>
### Pandas

We don't use pandas in this course, but it is a powerful tool.

<!-- TOC --><a name="location-measures"></a>
### Location measures

`Location measures`, also known as measures of central tendency, are statistical values that attempt to describe a set of data by identifying the central position within that set of data. These measures indicate where most values in a distribution fall and are also referred to as the central location of a distribution. The most common location measures are the mean, median, and mode.

* **Mean:** The mean, often called the average, is calculated by adding all data points in a data set and then dividing by the number of data points. For example, the mean of `4, 1, and 7` is `(4 + 1 + 7) / 3 = 12 / 3 = 42.`

* **Median:** The median is the middle number in a sorted list of numbers. If there is an even number of observations, the median will be the average of the two middle numbers. For example, the median of `4, 1, and 7` is `4` because when the numbers are put in order `(1, 4, 7)`, the number `4` is in the middle.

* **Mode:** The mode is the number that appears most frequently in a data set. A set of data may have one mode, more than one mode, or no mode at all. For example, the mode of `{4, 2, 4, 3, 2, 2}` is `2` because it occurs three times, which is more than any other number.

<!-- TOC --><a name="another-way-to-calculate-those-location-measures-in-python-statistics-library"></a>
#### Another way to calculate those location measures in Python: statistics library

```python
import statistics

mean = statistics.mean(your_list)
median = statistics.median(your_list)
mode = statistics.mode(your_list)
```

<!-- TOC --><a name="variability-measures"></a>
### Variability measures

`Variability measures`, also known as measures of dispersion, are statistical values that describe the spread or dispersion of a set of data. These measures indicate how spread out the values in a distribution are around the central value. The most common variability measures are variance, standard deviation, and range.

* **Variance:** 
	- Variance is a measure of how far each value in the data set is from the mean. It is calculated by taking the average of squared deviations from the mean. 
    - Variance tells you the degree of spread in your data set. The more spread the data, the larger the variance is in relation to the mean. 
    - Variance is always measured in squared units. For example, if we have to find the variance of the height of students in a class, and if the height is given in cm, then the variance is calculated in cm^2.

* **Standard Deviation:** 
	- Standard deviation is another measure of variability. It is simply the square root of the variance.
    - Unlike variance, standard deviation is measured in the same units as the data, which makes it easier to interpret.
    - It gives us an idea of how much variation or “dispersion” there is from the average (mean), or expected value.

* **Interquartile Range (IQR):**
	- The Interquartile Range (IQR) is a measure of statistical dispersion, which is equal to the difference between the upper and lower quartiles.
    - It is used to measure the spread of the middle 50% of values in a dataset.
    - Quartiles are the values that divide a list of numerical data into quarters. There are three quartiles: Q1 (the first quartile), Q2 (the second quartile or median), and Q3 (the third quartile).
    - The formula for interquartile range is: Interquartile range = Upper Quartile – Lower Quartile = Q3 – Q1 where Q1 is the first quartile and Q3 is the third quartile of the series.
    
<!-- TOC --><a name="data-distribution"></a>
### Data distribution

A data distribution is a function or a listing which shows all the possible values (or intervals) of the data and how often they occur. When a dataset is plotted, the resulting graph gives an overview of all the possible values in the dataset and how often they occur. There are two types of data distribution based on two different kinds of data: `Discrete` and `Continuous`.

* **Box Plot:** A box plot is a graphical representation of statistical data based on a five-number summary. The five-number summary includes the minimum, first quartile (Q1), median (Q2), third quartile (Q3), and maximum. It can also show if a dataset is symmetric (median lies in the center of the box), positively skewed (median is closer to the bottom of the box), or negatively skewed (median is closer to the top of the box). The Interquartile Range (IQR) is the range between Q1 and Q3, representing the middle 50% of scores.

* **Histogram:** A histogram is a graphical representation of a grouped frequency distribution with continuous classes. It is represented by a set of rectangles, adjacent to each other, where each bar represents a kind of data. The horizontal axis displays the number range. The vertical axis (frequency) represents the amount of data that is present in each range. The number ranges depend upon the data that is being used.

**Here are some examples:**

- **Box Plot:** Let’s say we have a dataset with these five values: 2, 4, 6, 8, 10. The interquartile range (IQR) for this dataset is calculated as: Q1: 3; Q3: 9; IQR = Q3 – Q1 = 6.

Suppose we have a dataset that shows the height of 17 different plants (in inches) in a lab: `61, 63, 64, 66, 68, 69, 71, 71.5, 72, 72.5, 73, 73.5, 74, 74.5`.

- **Histogram:** We can group the data as follows in a frequency distribution table by setting a range:

| Height Range (ft) | Number of Trees (Frequency) |
|-------------------|-----------------------------|
| 60 - 75 | 3 |
| 66 - 70 | 3 |
| 71 - 75 | 8 |

This data can be now shown using a histogram.

<!-- TOC --><a name="oop"></a>
## OOP

* **Four pillars of OOP:**
	* **Encapsulation**
    * **Abstraction**
    * **Polymorphism**
    * **Inheritance**. There are some types of inheritance:
    	* **Single inheritance**: Single inheritance is when a class inherits from a single superclass. This is the simplest form of inheritance.
        ```python
        class Parent:  # Parent class
            def func1(self):
                print("Parent class.")

        class Child(Parent):  # Child class inherits from Parent
            def func2(self):
                print("Child class.")

        object = Child()
        object.func1()  # outputs: Parent class.
        object.func2()  # outputs: Child class.
        ```
    
        * **Multiple inheritance**: When a child class inherits from multiple parent classes, it is called multiple inheritance. Unlike Java and like C++, Python supports multiple inheritance. We specify all parent classes as a comma-separated list in the bracket. 
        ```python
        class Mammal: 
            def mammal_info(self):
                print("Mammals.")

        class WingedAnimal: 
            def winged_animal_info(self):
                print("Winged.")

        class Bat(Mammal, WingedAnimal):  # Bat inherits from both Mammal and WingedAnimal
            pass

        b1 = Bat()
        b1.mammal_info()  # outputs: Mammals.
        b1.winged_animal_info()  # outputs: Winged.

        ```
        * **Multilevel inheritance:** Multilevel inheritance is when a class is derived from a class which is itself derived from another class. The class at the very top of the hierarchy is often called the base or parent class, and classes that inherit from it are called child or derived classes.
        ```python
        class Grandfather:
            def super_method(self):
                print("Grandfather")

        class Father(Grandfather):
            def method1(self):
                print("Father")

        class Son(Father):  # Derived from Father (which is derived from Grandfather)
            def method2(self):
                print("Son")

        d2 = Son()
        d2.super_method()  # outputs: Grandfather
        d2.method1()  # outputs: Father
        d2.method2()  # outputs: Son

        ```
        * **Hierarchical inheritance:** Hierarchical inheritance is when more than one derived classes are created from a single base or parent class.
        ```python
        class Animal:
            def animal(self):
                print("Animal")

        class Cat(Animal): 
            def cat(self):
                print("Cat")

        class Dog(Animal):
            def dog(self):
                print("Dog")

        cat = Cat()
        dog = Dog()

        cat.animal()  # outputs: Animal
        cat.cat()  # outputs: Cat

        dog.animal()  # outputs: Animal
        dog.dog()  # outputs: Dog

        ```

<!-- TOC --><a name="class"></a>
## Class

* A `class` is a blueprint for creating objects. 
* `Objects` are instances of a `class`, which can have `properties (attributes)` and `behaviors (methods)`.
* When comparing 2 objects, Python compares its address, not its attributes.
* When working with an object, it is suggested to copy the object first. By doing this, you are copying the address of the object, not only the attributes.

```python
class a:
    # some codes
```

<!-- TOC --><a name="attributes"></a>
### Attributes

We have 2 types of attributes:

* **Class attributes**
```python
class a:
    MY_ATTRIBUTE = 1 # This is class attributes
```
* **Instance attributes**
```python
class a:
    def __init__(self, bee):
        self.b = bee # b is an instance attribute, bee is a parameter
```

Here's an example of calling those 2 attributes:


```python
class a:
    CLS_ATTR = 100
    def __init__(self, *param):
        self.inst_attr = param
obj = a(1,2,3)
obj.inst_attr
```




    (1, 2, 3)




```python
obj.CLS_ATTR
```




    100




<!-- TOC --><a name="methods"></a>
### Methods

Methods are function that are inside a class. We have 3 general types of method:

* **Instance method:**
```python
def my_method(self, *params):
    # some codes
```
* **Static method:** Method without passing `self` into
```python
@staticmethod
def my_static(*params):
    # some codes
```
* **Class method:** Method passing a class: `cls` instead of `self`
```python
@classmethod
def my_class_method(cls, *params):
    # some codes
```

<!-- TOC --><a name="properties"></a>
### Properties

In Python, a property is a way to access attributes of a class. A property in Python provides an interface for instance variables, it encapsulates instance variables and provides indirect access to them. There are three parts to a property:

* `getter` method: Is used to get the value of the variable.
* `setter` method: Sets the value of the attribute.
* `deleter` method: Deletes the attribute.

Here’s an example of how these concepts can be used in Python:


```python
class Vehicle:
    def __init__(self, brand, model):
        self._brand = brand  # protected attribute (Encapsulation)
        self._model = model  # protected attribute (Encapsulation)

    @property
    def brand(self):  # getter 
        return self._brand

    @brand.setter
    def brand(self, brand):  # setter 
        self._brand = brand

    def move(self):  # define method (polymorphism)
        pass

class Car(Vehicle):  # Car class inherits from Vehicle (inheritance)
    def move(self):  # override method (polymorphism)
        return "Drive"

class Boat(Vehicle):  # Boat class inherits from Vehicle (inheritance)
    def move(self):  # override method (polymorphism)
        return "Sail"
```


```python
car = Car("Ford", "Mustang")

# accessing and modifying property
print(car.brand)
car.brand = "Chevrolet"
print(car.brand)
```

    Ford
    Chevrolet



```python
boat = Boat("Yamaha", "275SD")

# calling methods
print(car.move())
print(boat.move())  
```

    Drive
    Sail


<!-- TOC --><a name="inheritance"></a>
## Inheritance

To inherit all attributes (including instance attributes and class attributes) from a class, you can use:
```python
super().__init__(*params)
```
or 
```python
parent_class.__init(self, *params)
```


```python
class parent:
    AB = 1
    def __init__(self, a, b):
        self.a = a
        self.b = b
class child(parent):
    def __init__(self, c):
        self.c = c
        super().__init__(a = 'Letter a', b = 0)

x = child(1)
```


```python
x.AB
```




    1




```python
x.c
```




    1




```python
x.a
```




    'Letter a'




```python
x.b
```




    0



<!-- TOC --><a name="decorator"></a>
## Decorator

**The `@` symbol is used for class and function `decorators`. Some common python decorators:**
```python
@property
@classmethod
@staticmethod
```

**The code snippet for the `decorator` is:**
```python
def decorator(func):
   return func

@decorator
def some_func():
    pass
```

* **which is equivalent to:**
```python
def decorator(func):
    return func

def some_func():
    pass

some_func = decorator(some_func)
```

**And we can even do `STACK DECORATOR`:**
```python
@f1(arg)
@f2
def func(): pass
```

* **which is equivalent to:**
```python
def func(): pass
func = f1(arg)(f2(func))
```

**However, `@` in the middle of a line is a `matrix multiplication`:**
```python
A = matrix([[1,3],[7,5]])
B = matrix([[6,8],[4,2]])

print(A @ B) # outputs: [[18, 14], [62, 66]]
```

Here is a good example of decorator:


```python
class Pizza(object):
    def __init__(self):
        self.toppings = []

    def __call__(self, topping):
        # When using '@instance_of_pizza' before a function definition
        # the function gets passed onto 'topping'.
        self.toppings.append(topping())

    def __repr__(self):
        return str(self.toppings)

pizza = Pizza()

@pizza
def cheese():
    return 'cheese'
@pizza
def sauce():
    return 'sauce'

print(pizza)
```

    ['cheese', 'sauce']


<!-- TOC --><a name="recursion"></a>
## Recursion

`Recursion` is a common mathematical and programming concept where a function calls itself.

In Python, a function is said to be recursive if it can call itself.

```python
def func(n):
	return func(n-1)
```

Recursive functions can make the code look clean and elegant, and they can break down complex tasks into simpler sub-problems. However, they can also be hard to follow and debug, and they can be inefficient as they take up a lot of memory and time.

Every recursive function must have a base condition that stops the recursion, or else the function calls itself infinitely1. The Python interpreter limits the depths of recursion to help avoid infinite recursions, resulting in stack overflows1. By default, the maximum depth of recursion is 1000. If the limit is crossed, it results in a RecursionError.

```python
def func(n):
    if n == 1:
        return 1
    else:
        return func(n-1)
```

**Examples:**


```python
def countup(n):
    if n == 0:
        pass
    else:
        countup(n-1)
        print(n)
countup(5)
```

    1
    2
    3
    4
    5



```python
def factorial(n):
    if n == 1:
        return 1
    else:
        return n * factorial(n-1)
factorial(5)
```




    120




```python
def fibonacci(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fibonacci(n-1) + fibonacci(n-2)
fibonacci(5)
```




    5



<!-- TOC --><a name="recursive-data-types"></a>
## Recursive data types

A recursive data type is a data type for values that may contain other values of the same type. Data of recursive types are usually viewed as directed graphs.

<!-- TOC --><a name="binary-tree"></a>
### Binary tree

An example of a recursive data type is a binary tree. A binary tree is a tree-like data structure where each node has at most two children, referred to as the left child and the right child. For each node, the left child’s key must be less than the node’s key, and the right child’s key must be greater than the node’s key.

**Example:**


```python
class Node:
    def __init__(self, data):
        self.left = None
        self.right = None
        self.data = data

    def insert(self, data):
        if self.data:
            if data < self.data:
                if self.left is None:
                    self.left = Node(data)
                else:
                    self.left.insert(data)
            elif data > self.data:
                if self.right is None:
                    self.right = Node(data)
                else:
                    self.right.insert(data)
        else:
            self.data = data

    def print_tree(self):
        if self.left:
            self.left.print_tree()
        print(self.data),
        if self.right:
            self.right.print_tree()

root = Node(12)
root.insert(6)
root.insert(15)
root.insert(1)
root.insert(21)
root.insert(3)

root.print_tree()
```

    1
    3
    6
    12
    15
    21


**There are some types of binary tree:**
* **Full Binary Tree:** A full binary tree is a special type of binary tree in which every parent node/internal node has either two or no children. It is also known as a proper binary tree.
* **Degenerate Tree:** A degenerate or pathological tree is a tree having a single child either left or right. Such trees are performance-wise the same as linked lists.
* **Skewed Binary Tree:** A skewed binary tree is a pathological/degenerate tree in which the tree is either dominated by the left nodes or the right nodes. Thus, there are two types of skewed binary trees: left-skewed binary trees and right-skewed binary trees.
* **Complete Binary Tree:** A Binary Tree is a Complete Binary Tree if all the levels are completely filled except possibly the last level and the last level has all keys as left as possible. A complete binary tree is just like a full binary tree, but with two major differences: Every level except the last level must be completely filled. All the leaf elements must lean towards the left.
* **Perfect Binary Tree:** A Binary tree is a Perfect Binary Tree in which all the internal nodes have two children and all leaf nodes are at the same level. The number of leaf nodes is the number of internal nodes plus 1.
* **Balanced Binary Tree:** A balanced binary tree, also known as a height-balanced binary tree, is defined to be a binary tree in which the height of the left and right subtree of any node differ by not more than 1.

<!-- TOC --><a name="searching"></a>
## Searching

Searching in Python is a fundamental operation that involves finding a specific value or a set of values that match a condition from a collection of items such as a list, an array, or a set.

**Some common searching methods:**

<!-- TOC --><a name="linear-search"></a>
### Linear search

This is the simplest form of searching. It involves iterating over each element in the list one by one until the desired element is found.


```python
def linear_search(arr, x):
    for i in range(len(arr)):
        if arr[i] == x:
            return i
    return -1
```

<!-- TOC --><a name="binary-search"></a>
### Binary Search

This method is used on sorted lists. It works by repeatedly dividing the list in half until the desired element is found. Here’s an example:


```python
def binary_search(arr, low, high, x):
    if high >= low:
        mid = (high + low) // 2
        if arr[mid] == x:
            return mid
        elif arr[mid] > x:
            return binary_search(arr, low, mid - 1, x)
        else:
            return binary_search(arr, mid + 1, high, x)
    else:
        return -1
```

<!-- TOC --><a name="jump-search"></a>
### Jump Search

Like Binary Search, Jump Search is a searching algorithm for sorted arrays. The basic idea is to check fewer elements by jumping ahead fixed steps or skipping some elements instead of searching all elements.


```python
import math

def jump_search(arr, x):
    n = len(arr)
    step = math.sqrt(n)
    prev = 0
    while arr[int(min(step, n)-1)] < x:
        prev = step
        step += math.sqrt(n)
        if prev >= n:
            return -1
    while arr[int(prev)] < x:
        prev += 1
        if prev == min(step, n):
            return -1
    if arr[int(prev)] == x:
        return prev
    return -1
```

<!-- TOC --><a name="interpolation-search"></a>
### Interpolation Search

This method works better than Binary Search for lists where the values are uniformly distributed. It tries to follow the way humans search a list by starting from where we think the item may be.


```python
def interpolation_search(arr, x):
    lo = 0
    hi = len(arr) - 1
    while lo <= hi and x >= arr[lo] and x <= arr[hi]:
        pos  = lo + ((hi - lo) // (arr[hi] - arr[lo]) * (x - arr[lo]))
        if arr[pos] == x:
            return pos
        if arr[pos] < x:
            lo = pos + 1;
        else:
            hi = pos - 1;
    return -1
```

<!-- TOC --><a name="exponential-search"></a>
### Exponential Search

This method involves two steps: finding a range where the element might be present and then performing Binary Search within that range.


```python
def binary_search(arr, l, r, x):
    if r >= l:
        mid = l + (r - l) // 2
        if arr[mid] == x:
            return mid
        if arr[mid] > x:
            return binary_search(arr, l, mid-1, x)
        return binary_search(arr, mid + 1, r, x)
    return -1

def exponential_search(arr, n, x):
    if arr[0] == x:
        return 0
    i = 1
    while i < n and arr[i] <= x:
        i = i * 2
    return binary_search( arr, i // 2, min(i, n-1), x)
```

<!-- TOC --><a name="fibonacci-search"></a>
### Fibonacci Search

This method works by dividing the array into unequal parts based on Fibonacci numbers and uses these numbers to search for an element.


```python
def fibonacci_search(arr, x):
    fibMMm2 = 0 
    fibMMm1 = 1  
    fibM = fibMMm2 + fibMMm1 
    while (fibM < len(arr)):
        fibMMm2 = fibMMm1
        fibMMm1 = fibM
        fibM = fibMMm2 + fibMMm1
    offset = -1;
    while (fibM > 1):
        i = min(offset+fibMMm2, len(arr)-1)
        if (arr[i] < x):
            fibM  = fibMMm1
            fibMMm1 = fibMMm2
            fibMMm2 = fibM - fibMMm1
            offset = i
        elif (arr[i] > x):
            fibM  = fibMMm2
            fibMMm1 = fibMMm1 - fibMMm2
            fibMMm2 = fibM - fibMMm1
        else :
            return i
```

<!-- TOC --><a name="breadth-first-search-bfs-and-depth-first-search-dfs"></a>
### Breadth-First Search (BFS) and Depth-First Search (DFS)

These are techniques used for traversing or searching tree or graph data structures.


```python
def dfs(graph, start, visited=None):
    if visited is None:
        visited = set()
    visited.add(start)
    print(start, end=' ')
    for next in graph[start] - visited:
        dfs(graph, next, visited)
    return visited

graph = {'0': set(['1', '2']),
         '1': set(['0', '3', '4']),
         '2': set(['0']),
         '3': set(['1']),
         '4': set(['2', '3'])}
dfs(graph, '0')
```

    0 1 4 2 3 3 2 




    {'0', '1', '2', '3', '4'}



<!-- TOC --><a name="a-search-algorithm"></a>
### A* Search Algorithm

It’s one of the best and popular techniques used in path-finding and graph traversals.


```python
from queue import PriorityQueue

def a_star(graph, start_node, end_node):
    
    open_list = PriorityQueue()
    open_list.put((0, start_node))
    came_from = {}
    cost_so_far = {}
    came_from[start_node] = None
    cost_so_far[start_node] = 0

    while not open_list.empty():
        current = open_list.get()[1]

        if current == end_node:
            break

        for next in graph.neighbors(current):
            new_cost = cost_so_far[current] + graph.cost(current, next)
            if next not in cost_so_far or new_cost < cost_so_far[next]:
                cost_so_far[next] = new_cost
                priority = new_cost + graph.heuristic(next, end_node)
                open_list.put((priority, next))
                came_from[next] = current

    return came_from, cost_so_far
```

<!-- TOC --><a name="sorting"></a>
## Sorting

Sorting is the process of arranging data in a particular format. In Python, there are several methods to sort data, including built-in functions and manual implementations. 

**Some common sorting methods:**

<!-- TOC --><a name="built-in-sort-function"></a>
### Built-in sort() function

Python’s list objects have a built-in `sort()` function that can be used to sort the items in the list in ascending order.


```python
numbers = [1, 3, 4, 2]
numbers.sort()
print(numbers)
```

    [1, 2, 3, 4]


<!-- TOC --><a name="built-in-sorted-function"></a>
### Built-in sorted() function

Python also provides a built-in function `sorted()`, which returns a new sorted list from the items in any sequence instead of just sorting the list like `sort()` function.


```python
numbers = [1, 3, 4, 2]
sorted_numbers = sorted(numbers)
print(sorted_numbers)
```

    [1, 2, 3, 4]


<!-- TOC --><a name="bubble-sort"></a>
### Bubble Sort

It is a simple sorting algorithm that repeatedly steps through the list, compares adjacent elements and swaps them if they are in the wrong order. The pass through the list is repeated until the list is sorted.


```python
def bubble_sort(numbers):
    for i in range(len(numbers)):
        for j in range(len(numbers) - i - 1):
            if numbers[j] > numbers[j + 1]:
                numbers[j], numbers[j + 1] = numbers[j + 1], numbers[j]
    return numbers
bubble_sort([1, 3, 4, 2])
```




    [1, 2, 3, 4]



<!-- TOC --><a name="insertion-sort"></a>
### Insertion Sort

It is a simple sorting algorithm that builds the final sorted array one item at a time. It is much less efficient on large lists than more advanced algorithms such as quicksort or merge sort.


```python
def insertion_sort(numbers):
    for i in range(1, len(numbers)):
        key = numbers[i]
        j = i - 1
        while j >=0 and key < numbers[j] :
                numbers[j + 1] = numbers[j]
                j -= 1
        numbers[j + 1] = key
    return numbers
insertion_sort([1, 3, 4, 2])
```




    [1, 2, 3, 4]



<!-- TOC --><a name="quick-sort"></a>
### Quick Sort

It is an efficient sorting algorithm that uses divide-and-conquer principles to divide a list into two sub-lists. The steps are:
- Pick an element from the array as a pivot.
- Partitioning: reorder the array so that all elements with values less than the pivot come before the pivot, while all elements with values greater than the pivot come after it.
- Recursively apply the above steps to the sub-array of elements with smaller values and separately to the sub-array of elements with greater values.


```python
def partition(arr, low, high):
    i = (low-1)
    pivot = arr[high]
    for j in range(low , high):
        if arr[j] <= pivot:
            i = i+1
            arr[i],arr[j] = arr[j],arr[i]
    arr[i+1],arr[high] = arr[high],arr[i+1]
    return (i+1)

def quick_sort(arr, low, high):
    if low < high:
        pi = partition(arr, low, high)
        quick_sort(arr, low, pi-1)
        quick_sort(arr, pi+1, high)
    return arr
        
quick_sort([1, 3, 4, 2], 0, len([1,3,4,2]) - 1)
```




    [1, 2, 3, 4]



<!-- TOC --><a name="merge-sort"></a>
### Merge Sort

It is an efficient sorting algorithm that uses divide-and-conquer principles to divide the unsorted list into n sub-lists, each containing one element (a list of one element is considered sorted), and then repeatedly merge sub-lists to produce new sorted sub-lists until there is only one sub-list remaining.


```python
def merge_sort(arr):
    if len(arr) > 1:
        mid = len(arr)//2
        L = arr[:mid]
        R = arr[mid:]
        merge_sort(L)
        merge_sort(R)
        i = j = k = 0
        while i < len(L) and j < len(R):
            if L[i] < R[j]:
                arr[k] = L[i]
                i += 1
            else:
                arr[k] = R[j]
                j += 1
            k += 1
        while i < len(L):
            arr[k] = L[i]
            i += 1
            k += 1
        while j < len(R):
            arr[k] = R[j]
            j += 1
            k += 1
    return arr

merge_sort([1, 3, 4, 2])
```




    [1, 2, 3, 4]



<!-- TOC --><a name="timing-the-function"></a>
## Timing the function

Timing functions in Python can be important for performance testing and optimization. Python provides several ways to time your code.

**There are some ways of doing this:**

<!-- TOC --><a name="time-module"></a>
### Time module

The simplest way to time a function in Python is using the time module.


```python
import time

def bubble_sort(numbers):
    for i in range(len(numbers)):
        for j in range(len(numbers) - i - 1):
            if numbers[j] > numbers[j + 1]:
                numbers[j], numbers[j + 1] = numbers[j + 1], numbers[j]
    return numbers

start_time = time.time()
bubble_sort([1, 3, 4, 2])
end_time = time.time()

execution_time = end_time - start_time
print(f"The function took {execution_time} seconds to complete")
```

    The function took 0.000102996826171875 seconds to complete


<!-- TOC --><a name="timeit-module"></a>
### timeit module

For small bits of code, the timeit module is quite handy. It temporarily turns off garbage collection and runs multiple trials to eliminate the influence of other tasks on your machine.


```python
import timeit

start_time = timeit.default_timer()

numbers = [1,3,4,2]
for i in range(len(numbers)):
    for j in range(len(numbers) - i - 1):
        if numbers[j] > numbers[j + 1]:
            numbers[j], numbers[j + 1] = numbers[j + 1], numbers[j]
    
end_time = timeit.default_timer()

execution_time = end_time - start_time
print(f"The function took {execution_time} seconds to complete")
```

    The function took 0.0002940830308943987 seconds to complete


<!-- TOC --><a name="and-you-can-do-some-magic-with-this"></a>
### And you can do some magic with this:

<!-- TOC --><a name="decorator-1"></a>
### Decorator

We can create a decorator that will measure the elapsed time of the function that it modifies.


```python
import time

def timer_decorator(func):
    def wrapper(*args, **kwargs):
        start_time = time.time()
        result = func(*args, **kwargs)
        end_time = time.time()
        print(f"The function took {end_time - start_time} seconds to complete")
        return result
    return wrapper

@timer_decorator
def bubble_sort(numbers):
    for i in range(len(numbers)):
        for j in range(len(numbers) - i - 1):
            if numbers[j] > numbers[j + 1]:
                numbers[j], numbers[j + 1] = numbers[j + 1], numbers[j]
    return numbers
bubble_sort([1, 3, 4, 2])
```

    The function took 7.867813110351562e-06 seconds to complete





    [1, 2, 3, 4]



<!-- TOC --><a name="or-if-you-use-jupyter-notebook-we-can-use-the-magic-command-time"></a>
### Or if you use jupyter notebook, we can use the magic command `%%time`:


```python
%%time
def bubble_sort(numbers):
    for i in range(len(numbers)):
        for j in range(len(numbers) - i - 1):
            if numbers[j] > numbers[j + 1]:
                numbers[j], numbers[j + 1] = numbers[j + 1], numbers[j]
    return numbers
bubble_sort([1, 3, 4, 2])
```

    CPU times: user 59 µs, sys: 2 µs, total: 61 µs
    Wall time: 66 µs





    [1, 2, 3, 4]


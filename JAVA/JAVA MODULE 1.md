# JAVA MODULE 1 — COMPLETE STUDY NOTES


---

# MODULE 1 — JAVA

## MODULE CONTENT

The PPT covers three major parts:

### 1.1 Introduction to Java

* Java's lineage
* Java buzzwords/features
* Object-oriented concepts
* JDK
* JRE
* JVM
* Bytecode
* Java API
* Simple Java program
* `main()` method
* Compile and run a Java program

### 1.2 Data Types, Variables, Arrays and Operators

* Data types
* Primitive data types
* Non-primitive/reference data types
* Arrays
* 1-D arrays
* 2-D arrays
* Methods
* Operators
* Type conversion and casting
* Automatic type promotion

### 1.3 Control Statements

* `if`
* `if-else`
* `if-else-if`
* Nested `if`
* `switch`
* `while`
* `do-while`
* `for`
* Enhanced `for`
* `break`
* Labelled `break`
* `continue`
* Labelled `continue`
* `return` is listed in the module outline, but no separate detailed slide/program for it is provided. 

---

# PART A — INTRODUCTION TO JAVA

# 1. Java's Lineage

Java is related to **C++**, which is a direct descendant of **C**.

* Java derives its syntax from C.
* Many object-oriented features of Java were influenced by C++.
* Java is influenced by C++, but **Java is not an enhanced version of C++**. 

### Easy way to remember

**C → C++ → Java**

Java gets:

* Syntax → mainly from C
* OOP influence → mainly from C++

---

# 2. Java Buzzwords

The PPT lists the following Java characteristics:

1. Simple
2. Object Oriented
3. Distributed
4. Multithreaded
5. Dynamic
6. Architecture Neutral
7. Portable
8. High Performance
9. Robust
10. Secure 

These are very important for theory questions.

---

## 2.1 Simple

Java is designed to be simple and follows C/C++ syntax.

According to the PPT, Java is simpler than C++ because it does not have:

* Pointers and pointer mathematics
* `struct`
* `typedef`
* Operator overloading
* Templates
* Multiple inheritance
* It has automatic garbage collection. 

### Remember:

**Java = C-like syntax + simpler features**

---

# 2.2 Portable

Java programs can execute on different computers containing a JVM.

When Java source code is compiled, it produces an intermediate code called **bytecode**.

Bytecode helps Java achieve portability.

The same bytecode can be taken to another computer/OS having a JVM and executed there. 

### Important line for exam:

> **Write Once, Run Anywhere**

---

# 2.3 Object Oriented

Java follows an object-oriented model.

Java programs are developed using:

* Classes
* Objects

A class contains:

* **Data** → information/properties
* **Methods** → functionality/behavior

Example from the PPT:

A **dog** can be considered an object.

### Properties

* Name
* Height
* Colour
* Age

These are represented using variables.

### Behaviours

* Running
* Barking
* Eating
* Sleeping

These are represented using methods.

Java supports:

1. Encapsulation
2. Inheritance
3. Polymorphism
4. Abstraction 

### Easy memory trick:

**EIPA**

* **E** → Encapsulation
* **I** → Inheritance
* **P** → Polymorphism
* **A** → Abstraction

---

# 2.4 Robust

Robust means **strong**.

Java programs are designed to be strong and not crash easily.

Reasons given in the PPT:

* Strongly typed language
* No pointers
* Automatic garbage collection
* Robust memory management
* Extensive error checking
* Exception handling 

---

# 2.5 Architecture Neutral

Java bytecode can run on computers having different:

* Operating systems
* CPUs

Therefore Java is called **architecture neutral**. 

---

# 2.6 Interpreted

Java compilation does not directly produce machine instructions.

It produces **bytecode**.

The bytecode can be executed on a machine implementing JVM.

The JVM interprets the bytecode into machine instructions at runtime. 

### Flow:

```text
Java Source Code
       ↓
    Compiler
       ↓
   Bytecode
       ↓
      JVM
       ↓
Machine Instructions
```

---

# 2.7 Distributed

Java was designed for Internet/web-based applications.

The PPT mentions built-in support for:

* TCP/IP
* HTTP
* FTP
* RMI — Remote Method Invocation 

---

# 2.8 Secure

Java provides security through:

* Interpretation
* Bytecode checker/verifier
* JVM
* No pointers

The interpreter performs checks on compiled code.

The PPT mentions checking:

* Illegal code
* Illegal data conversions
* Object field access
* Opcode parameter types 

---

# 2.9 Multithreaded

Java has built-in support for:

* Threads
* Process synchronization

This is useful for interactive programs. 

---

# 3. JAVA ARCHITECTURE

The main components of Java architecture are:

```text
             JDK
              |
      ----------------
      |              |
    JRE        Development Tools
      |
   JVM + Libraries
```

The PPT specifically identifies:

* JDK
* JRE
* JVM

as components of Java architecture. It also explains that Java combines compilation and interpretation. 

---

# 4. JDK — Java Development Kit

## Definition

JDK is a software development environment used for developing Java software applications and applets.

It contains development tools and supporting libraries together with JRE. 

### Important tools

| Tool           | Purpose                                      |
| -------------- | -------------------------------------------- |
| `javac`        | Java compiler                                |
| `java`         | Java launcher                                |
| `javadoc`      | Documentation tool                           |
| `appletviewer` | Run/debug Java applets without a web browser |

### Most important point

> **JDK is required to compile Java programs.**

---

# 5. JRE — Java Runtime Environment

JRE provides the environment required to **execute Java applications**.

It includes:

* JVM
* Class libraries
* Runtime software

The PPT says JRE provides the environment in which Java programs can execute and initiates the JVM. 

### Main components listed:

1. Java API
2. Class Loader
3. Bytecode Verifier
4. JVM Interpreter 

---

# 6. JVM — Java Virtual Machine

The PPT explains JVM mainly as the environment that executes bytecode.

### Important relationship

```text
JDK
 └── JRE
      ├── JVM
      └── Libraries
```

### Easy difference

| JDK                        | JRE                            | JVM               |
| -------------------------- | ------------------------------ | ----------------- |
| Used for development       | Used for running Java programs | Executes bytecode |
| Contains development tools | Contains runtime environment   | Virtual machine   |
| Includes JRE               | Includes JVM                   | Part of JRE       |

---

# 7. Java API

**Java API = Application Programming Interface**

It is a large collection of ready-made software components.

It contains predefined:

* Classes
* Interfaces
* Methods

These are organized into Java packages. 

## Important Java API packages

| Package         | Purpose                   |
| --------------- | ------------------------- |
| `java.lang`     | Fundamental Java classes  |
| `java.io`       | Input/output              |
| `java.util`     | Utilities and collections |
| `java.math`     | Mathematical operations   |
| `java.security` | Security functions        |
| `java.awt`      | GUI, graphics and images  |
| `java.sql`      | Database/SQL access       |
| `java.net`      | Networking                |
| `java.imageIO`  | Image input/output        |

`java.lang` is automatically imported and does not need explicit importing. 

---

# 8. BYTECODE

When Java source code is compiled, it produces **bytecode**.

The compiled file has the `.class` extension.

Example:

```text
Intro.java
    ↓ javac
Intro.class
```

The `.class` file contains bytecode.

The JVM executes/interprets this bytecode. 

---

# 9. SIMPLE JAVA PROGRAM

The PPT gives the following basic structure:

```java
public class Intro {

    public static void main(String[] args) {
        System.out.println("Welcome to the JDK!");
    }

}
```



## Understand each part

### `public class Intro`

Creates a class named `Intro`.

### `public static void main(String[] args)`

This is the main entry point of the Java program.

### `System.out.println()`

Used to display output.

---

# 10. MAIN METHOD

Remember the syntax:

```java
public static void main(String[] args)
```

Break it into:

```text
public  → accessible
static  → belongs to class
void    → returns nothing
main    → main method
String[] args → command-line arguments
```

For exams, the most important thing is to remember the complete syntax exactly.

---

# 11. COMPILE AND RUN JAVA PROGRAM

The PPT shows three steps.

## Step 1 — Write program

Create:

```text
Intro.java
```

Example:

```java
public class Intro {

    public static void main(String[] args) {
        System.out.println("Welcome to the JDK!");
    }

}
```

## Step 2 — Compile

Use:

```text
javac Intro.java
```

This creates:

```text
Intro.class
```

The `.class` file contains bytecode. 

## Step 3 — Run

Use:

```text
java Intro
```

Do **not** write `.class` while running.

Output:

```text
Welcome to the JDK!
```



### Easy memory:

```text
.java → javac → .class → java → Output
```

---

# 12. ADDITION OF TWO NUMBERS

The PPT gives **three methods**.

---

## 12.1 Hardcoded Input

```java
public class AddTwoNumbersWithoutScanner {

    public static void main(String[] args) {

        double num1 = 5.5;
        double num2 = 10.5;

        double sum = num1 + num2;

        System.out.println("The sum of " + num1 +
                           " and " + num2 + " is: " + sum);
    }
}
```

### Idea

Numbers are directly assigned in the program.

---

# 12.2 Using Scanner Class

```java
import java.util.Scanner;

public class AddNumbers_Scanner {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the first number: ");
        double num1 = scanner.nextDouble();

        System.out.print("Enter the second number: ");
        double num2 = scanner.nextDouble();

        scanner.close();

        double sum = num1 + num2;

        System.out.println("The sum of " + num1 +
                           " and " + num2 + " is: " + sum);
    }
}
```

### Important syntax

```java
import java.util.Scanner;
```

Create Scanner:

```java
Scanner scanner = new Scanner(System.in);
```

Read a double:

```java
scanner.nextDouble();
```

Close Scanner:

```java
scanner.close();
```

---

# 12.3 Using Command Line Arguments

```java
public class AddNumbers {

    public static void main(String[] args) {

        if (args.length != 2) {
            System.out.println(
                "Usage: java AddNumbers <num1> <num2>"
            );
            return;
        }

        double num1 = Double.parseDouble(args[0]);
        double num2 = Double.parseDouble(args[1]);

        double sum = num1 + num2;

        System.out.println("Sum: " + sum);
    }
}
```

### Important points

Command-line arguments are stored in:

```java
String[] args
```

Convert a string to `double`:

```java
Double.parseDouble(args[0]);
```

The PPT checks:

```java
if (args.length != 2)
```

before processing the values. 

---

# PART B — DATA TYPES

# 13. DATA TYPES

Data types specify:

* What type of data is stored
* The amount/size of memory required

The PPT divides Java data types into:

### 1. Primitive

### 2. Non-Primitive / Reference



---

# 14. PRIMITIVE DATA TYPES

The PPT's table gives the following:

| Data Type | Default Value |                    Size | Range                                                   |
| --------- | ------------: | ----------------------: | ------------------------------------------------------- |
| `byte`    |             0 |         1 byte / 8 bits | -128 to 127                                             |
| `short`   |             0 |       2 bytes / 16 bits | -32,768 to 32,767                                       |
| `int`     |             0 |       4 bytes / 32 bits | -2,147,483,648 to 2,147,483,647                         |
| `long`    |             0 |       8 bytes / 64 bits | -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 |
| `float`   |        `0.0f` |       4 bytes / 32 bits | approximately `1.4e-045` to `3.4e+038`                  |
| `double`  |        `0.0d` |       8 bytes / 64 bits | approximately `4.9e-324` to `1.8e+308`                  |
| `char`    |    `'\u0000'` |       2 bytes / 16 bits | 0 to 65536                                              |
| `boolean` |       `FALSE` | PPT states 1 or 2 bytes | 0 or 1                                                  |



---

# 15. BOOLEAN

A `boolean` stores:

```text
true
false
```

It is useful in conditions and as a flag.

The PPT states its default value as `False`. 

Example:

```java
boolean flag = true;
```

---

# 16. CHAR

`char` stores one character.

Characters are written using **single quotes**:

```java
char ch = 'A';
```

Java `char` supports Unicode.

According to the PPT:

* Size = 16 bits / 2 bytes
* Range = 0 to 65536 

---

# 17. NON-PRIMITIVE DATA TYPES

Reference/non-primitive data types:

* Refer to objects/instances
* Store a reference/address rather than the direct value
* Can be user-defined
* Can be assigned `null` 

Arrays are one important example.

---

# PART C — ARRAYS

# 18. ARRAYS

An array is a collection of elements of the **same type**.

Important points:

* Java arrays are objects.
* Elements have the same data type.
* Array uses indexing.
* First element is at index `0`.
* Arrays have a fixed set of elements.
* Length can be obtained using `length`.
* Arrays are dynamically allocated using `new`.



### Example

```java
int month_days[] = new int[12];
```

This creates an array of 12 integers.

The elements are initially `0`.

---

# 19. ARRAY CREATION — THREE WAYS

## Method 1 — Separate declaration, allocation and initialization

```java
int myArray[];

myArray = new int[3];

myArray[0] = 3;
myArray[1] = 5;
myArray[2] = 7;
```

## Method 2 — Declaration and allocation together

```java
int myArray[] = new int[3];

myArray[0] = 3;
myArray[1] = 5;
myArray[2] = 7;
```

## Method 3 — Declaration, allocation and initialization together

```java
int myArray[] = new int[] {3, 5, 7};
```

or:

```java
int myArray[] = {3, 5, 7};
```

The PPT shows these initialization approaches and explains that obtaining an array involves declaring the array variable and allocating memory using `new`. 

---

# 20. ONE-DIMENSIONAL ARRAY

## Basic syntax

```java
dataType[] arrayName;
```

Example:

```java
int[] a;
```

Memory allocation:

```java
a = new int[5];
```

Access:

```java
a[0]
a[1]
a[2]
```

Length:

```java
a.length
```

---

# PROGRAM 1 — PRINT ARRAY ELEMENTS

From the PPT:

```java
class OneDimensionalStandard
{
    public static void main(String args[])
    {
        int a = new int[3];

        a[0] = 10;
        a[1] = 20;
        a[2] = 30;

        System.out.println("One dimensional array elements are");
        System.out.println(a[0]);
        System.out.println(a[1]);
        System.out.println(a[2]);
    }
}
```

The PPT also demonstrates printing an array using a `for` loop. 

### Better exam pattern:

```java
int[] a = {10, 20, 30, 40, 50};

for (int i = 0; i < a.length; i++) {
    System.out.println(a[i]);
}
```

---

# PROGRAM 2 — INPUT AND DISPLAY 1-D ARRAY

The PPT shows using `Scanner` to:

1. Read array length
2. Create array
3. Read elements
4. Display elements

Basic structure:

```java
import java.util.*;

class OneDimensionalScanner
{
    public static void main(String args[])
    {
        int len;
        Scanner sc = new Scanner(System.in);

        System.out.println("Enter Array length : ");
        len = sc.nextInt();

        int a[] = new int[len];

        System.out.println("Enter " + len +
                           " Element to Store in Array :");

        for(int i = 0; i < len; i++)
        {
            a[i] = sc.nextInt();
        }

        System.out.println("Elements in Array are :");

        for(int i = 0; i < len; i++)
        {
            System.out.print(a[i] + " ");
        }
    }
}
```

---

# PROGRAM 3 — MONTH DAYS ARRAY

The PPT gives an example where an array stores the number of days in each month.

```java
class Array {

    public static void main(String args[]) {

        int month_days[];

        month_days = new int[12];

        month_days[0] = 31;
        month_days[1] = 28;
        month_days[2] = 31;
        month_days[3] = 30;
        month_days[4] = 31;
        month_days[5] = 30;
        month_days[6] = 31;
        month_days[7] = 31;
        month_days[8] = 30;
        month_days[9] = 31;
        month_days[10] = 30;
        month_days[11] = 31;

        System.out.println(
            "April has " + month_days[3] + " days."
        );
    }
}
```

The PPT then gives the improved shorter version:

```java
class AutoArray {

    public static void main(String args[]) {

        int month_days[] = {
            31, 28, 31, 30, 31, 30,
            31, 31, 30, 31, 30, 31
        };

        System.out.println(
            "April has " + month_days[3] + " days."
        );
    }
}
```



---

# PROGRAM 4 — AVERAGE OF ARRAY

```java
class Average {

    public static void main(String args[]) {

        double nums[] = {
            10.1, 11.2, 12.3, 13.4, 14.5
        };

        double result = 0;
        int i;

        for(i = 0; i < 5; i++)
            result = result + nums[i];

        System.out.println("Average is " + result / 5);
    }
}
```

### Logic to remember:

```text
sum = 0
↓
add every element
↓
average = sum / number of elements
```



---

# PROGRAM 5 — SUM OF ARRAY ELEMENTS

```java
public class OneDimensionalArrayExample2 {

    public static void main(String[] args) {

        int[] numbers = {2, 4, 6, 8, 10};

        int sum = 0;

        for (int i = 0; i < numbers.length; i++) {
            sum += numbers[i];
        }

        System.out.println(
            "Sum of array elements: " + sum
        );
    }
}
```



---

# PROGRAM 6 — FIND MAXIMUM ELEMENT

```java
public class OneDimensionalArrayExample3 {

    public static void main(String[] args) {

        int[] numbers = {14, 7, 21, 35, 10};

        int max = numbers[0];

        for (int i = 1; i < numbers.length; i++) {

            if (numbers[i] > max) {
                max = numbers[i];
            }
        }

        System.out.println(
            "Maximum element in the array: " + max
        );
    }
}
```

### Logic:

```text
Assume first element is maximum
        ↓
Compare remaining elements
        ↓
If current > max
        ↓
Update max
```



---

# PROGRAM 7 — STRING ARRAY

```java
public class OneDimensionalArrayExample4 {

    public static void main(String[] args) {

        String[] fruits = {
            "Apple", "Banana", "Orange",
            "Mango", "Grapes"
        };

        System.out.println("Fruits in the array:");

        for (int i = 0; i < fruits.length; i++) {
            System.out.println(
                "Fruit at index " + i + ": " + fruits[i]
            );
        }
    }
}
```



---

# 21. TWO-DIMENSIONAL ARRAY

A 2-D array can be represented as:

```text
        Column
        0   1   2

Row 0   a   b   c
Row 1   d   e   f
Row 2   g   h   i
```

Access:

```java
array[row][column]
```

Example:

```java
arr[0][0]
arr[0][1]
arr[1][0]
```

The PPT represents a 2-D array using rows and columns. 

---

# PROGRAM 8 — PRINT 2-D ARRAY

```java
import java.io.*;

class GFG {

    public static void main(String[] args)
    {
        int[][] arr = {
            {1, 2},
            {3, 4}
        };

        for (int i = 0; i < 2; i++) {

            for (int j = 0; j < 2; j++) {
                System.out.print(arr[i][j] + " ");
            }

            System.out.println();
        }
    }
}
```

Output:

```text
1 2
3 4
```



---

# PROGRAM 9 — 2-D ARRAY WITH `new`

```java
int[][] arr = new int[10][20];

arr[0][0] = 1;

System.out.println("arr[0][0] = " + arr[0][0]);
```

The PPT also shows accessing every element:

```java
for (int i = 0; i < 2; i++) {

    for (int j = 0; j < 2; j++) {

        System.out.println(
            "arr[" + i + "][" + j + "] = "
            + arr[i][j]
        );
    }
}
```



---

# PROGRAM 10 — INITIALIZE AND DISPLAY 2-D ARRAY

```java
public class TwoDimensionalArrayExample1 {

    public static void main(String[] args) {

        int[][] matrix = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        System.out.println("Elements of the 2D array:");

        for (int i = 0; i < matrix.length; i++) {

            for (int j = 0;
                 j < matrix[i].length;
                 j++) {

                System.out.print(matrix[i][j] + " ");
            }

            System.out.println();
        }
    }
}
```



---

# PROGRAM 11 — SUM OF MATRIX ELEMENTS

```java
public class TwoDimensionalArrayExample2 {

    public static void main(String[] args) {

        int[][] matrix = {
            {2, 4, 6},
            {8, 10, 12},
            {14, 16, 18}
        };

        int sum = 0;

        for (int i = 0; i < matrix.length; i++) {

            for (int j = 0;
                 j < matrix[i].length;
                 j++) {

                sum += matrix[i][j];
            }
        }

        System.out.println(
            "Sum of matrix elements: " + sum
        );
    }
}
```



---

# PROGRAM 12 — MAXIMUM ELEMENT IN MATRIX

```java
public class TwoDimensionalArrayExample3 {

    public static void main(String[] args) {

        int[][] matrix = {
            {15, 7, 23},
            {10, 21, 35},
            {18, 12, 27}
        };

        int max = matrix[0][0];

        for (int i = 0; i < matrix.length; i++) {

            for (int j = 0;
                 j < matrix[i].length;
                 j++) {

                if (matrix[i][j] > max) {
                    max = matrix[i][j];
                }
            }
        }

        System.out.println(
            "Maximum element in the matrix: " + max
        );
    }
}
```



---

# PROGRAM 13 — STRING 2-D ARRAY

```java
public class TwoDimensionalArrayExample4 {

    public static void main(String[] args) {

        String[][] names = {
            {"John", "Alice", "Bob"},
            {"Mary", "David", "Eva"},
            {"Tom", "Olivia", "Charlie"}
        };

        System.out.println("Names in the 2D array:");

        for (int i = 0; i < names.length; i++) {

            for (int j = 0;
                 j < names[i].length;
                 j++) {

                System.out.print(names[i][j] + " ");
            }

            System.out.println();
        }
    }
}
```



---

# PROGRAM 14 — ADDITION OF TWO MATRICES

This is an **important exam program**.

The PPT uses two hardcoded matrices and creates a third matrix for the result. 

```java
public class MatrixAdditionHardcoded {

    public static void main(String[] args) {

        int[][] matrix1 = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        int[][] matrix2 = {
            {9, 8, 7},
            {6, 5, 4},
            {3, 2, 1}
        };

        int rows = matrix1.length;
        int columns = matrix1[0].length;

        int[][] resultMatrix =
            new int[rows][columns];

        for (int i = 0; i < rows; i++) {

            for (int j = 0; j < columns; j++) {

                resultMatrix[i][j] =
                    matrix1[i][j] + matrix2[i][j];
            }
        }

        System.out.println("Matrix 1:");
        displayMatrix(matrix1);

        System.out.println("Matrix 2:");
        displayMatrix(matrix2);

        System.out.println(
            "Resultant matrix (Sum of matrices):"
        );
        displayMatrix(resultMatrix);
    }

    private static void displayMatrix(int[][] matrix) {

        for (int i = 0; i < matrix.length; i++) {

            for (int j = 0;
                 j < matrix[i].length;
                 j++) {

                System.out.print(matrix[i][j] + " ");
            }

            System.out.println();
        }

        System.out.println();
    }
}
```

### Most important logic

```java
resultMatrix[i][j] =
    matrix1[i][j] + matrix2[i][j];
```

Remember:

> **Same position + Same position = Result position**

---

# PART D — METHODS

# 22. JAVA METHODS

A method is a collection of statements that performs a specific task.

A method:

* Performs a specific task
* May return a result
* May perform a task without returning anything
* Allows code reuse
* Avoids rewriting the same code

An important point from the PPT:

> In Java, every method must be part of a class. 

### Basic idea

```text
Class
 ├── Data
 └── Methods
```

---

# PART E — OPERATORS

The PPT lists these operator categories:

1. Arithmetic
2. Unary
3. Assignment
4. Relational
5. Logical
6. Ternary
7. Bitwise
8. Shift
9. `instanceof` 

---

# 23. ARITHMETIC OPERATORS

| Operator | Meaning        |
| -------- | -------------- |
| `+`      | Addition       |
| `-`      | Subtraction    |
| `*`      | Multiplication |
| `/`      | Division       |
| `%`      | Modulus        |
| `++`     | Increment      |
| `--`     | Decrement      |

Examples:

```java
a + b
a - b
a * b
a / b
a % b
```

The PPT example uses:

```java
int a = 12, b = 5;
```

and performs the arithmetic operations. 

---

# 24. ASSIGNMENT OPERATORS

| Operator | Example   | Same as      |      |        |    |
| -------- | --------- | ------------ | ---- | ------ | -- |
| `=`      | `x = 5`   | `x = 5`      |      |        |    |
| `+=`     | `x += 3`  | `x = x + 3`  |      |        |    |
| `-=`     | `x -= 3`  | `x = x - 3`  |      |        |    |
| `*=`     | `x *= 3`  | `x = x * 3`  |      |        |    |
| `/=`     | `x /= 3`  | `x = x / 3`  |      |        |    |
| `%=`     | `x %= 3`  | `x = x % 3`  |      |        |    |
| `&=`     | `x &= 3`  | `x = x & 3`  |      |        |    |
| `        | =`        | `x           | = 3` | `x = x | 3` |
| `^=`     | `x ^= 3`  | `x = x ^ 3`  |      |        |    |
| `>>=`    | `x >>= 3` | `x = x >> 3` |      |        |    |
| `<<=`    | `x <<= 3` | `x = x << 3` |      |        |    |



### Example

```java
int a = 4;
int var;

var = a;
var += a;
var *= a;
```

---

# 25. RELATIONAL OPERATORS

Used for comparison.

| Operator | Meaning               |
| -------- | --------------------- |
| `==`     | Equal to              |
| `!=`     | Not equal             |
| `>`      | Greater than          |
| `<`      | Less than             |
| `>=`     | Greater than or equal |
| `<=`     | Less than or equal    |

Example:

```java
a == b
a != b
a > b
a < b
a >= b
a <= b
```

Relational expressions produce a Boolean result. 

---

# 26. LOGICAL OPERATORS

| Operator | Name        |   |            |
| -------- | ----------- | - | ---------- |
| `&&`     | Logical AND |   |            |
| `        |             | ` | Logical OR |
| `!`      | Logical NOT |   |            |

### `&&`

True when both conditions are true.

```java
x < 5 && x < 10
```

### `||`

True when at least one condition is true.

```java
x < 5 || x < 4
```

### `!`

Reverses the result.

```java
!(x < 5)
```



---

# 27. UNARY OPERATORS

Unary operators work with one operand.

The PPT lists:

* Unary minus `-`
* NOT `!`
* Increment `++`
* Decrement `--`
* Bitwise complement `~`

Increment and decrement can be:

### Pre-increment

```java
++x
```

### Post-increment

```java
x++
```

### Pre-decrement

```java
--x
```

### Post-decrement

```java
x--
```



---

# 28. TERNARY OPERATOR

The ternary operator is a conditional operator that takes **three operands**.

It is a one-line replacement for an `if-else` statement. 

## Syntax

```java
variable = condition ? expression1 : expression2;
```

Meaning:

```text
if condition is true
    expression1
else
    expression2
```

### PPT example

```java
num1 = 10;
num2 = 20;

res = (num1 > num2) ?
      (num1 + num2) :
      (num1 - num2);
```

Since `num1 < num2`:

```text
res = num1 - num2
```

Therefore:

```text
res = -10
```



---

# 29. SHIFT OPERATORS

The PPT lists:

1. Left shift `<<`
2. Signed right shift `>>`
3. Unsigned right shift `>>>` 

---

## Left Shift `<<`

Left shifting by a number of positions is equivalent to multiplying by a power of 2.

General idea:

```text
x << n
```

means shifting `x` left by `n` positions. 

---

## Signed Right Shift `>>`

When bits are shifted right:

* Rightmost bit is discarded.
* Leftmost position is filled with the sign bit.
* Positive numbers get `0` on the left.
* Negative numbers retain the sign bit.

The PPT uses:

```text
8 → binary 1000
```

After right shifting:

```text
0100
```

which is:

```text
4
```



---

# PART F — CONTROL FLOW STATEMENTS

# 30. CONTROL FLOW

Control flow statements control the flow of execution of a program.

There are **three types**:

### 1. Decision Making / Selection

* `if`
* `if-else`
* `if-else-if`
* `switch`

### 2. Looping / Iterative

* `while`
* `do-while`
* `for`
* enhanced `for`

### 3. Branching / Jump

* `break`
* `continue`
* `return`



---

# 31. `if` STATEMENT

Used when a block should execute only when a condition is true.

## Syntax

```java
if (condition)
{
    // statements
}
```

Example:

```java
if (x > 10)
{
    System.out.println("x is greater than 10");
}
```



---

# 32. `if-else`

Used when there are two possible paths.

## Syntax

```java
if (condition)
{
    // statements if true
}
else
{
    // statements if false
}
```



### Remember:

```text
TRUE  → if
FALSE → else
```

---

# 33. `if-else-if` LADDER

Used when there are multiple conditions.

## Syntax

```java
if (condition1)
{
    // statements
}
else if (condition2)
{
    // statements
}
else
{
    // statements
}
```

The PPT explains that if a condition becomes true, its corresponding block executes. If all conditions are false, the `else` block executes. 

---

# 34. NESTED `if`

An `if` statement inside another `if` statement is called a nested `if`.

Example structure from the PPT:

```java
if (i == 10 || i < 15)
{
    if (i < 15)
        System.out.println("i is smaller than 15");

    if (i < 12)
        System.out.println("i is smaller than 12 too");
}
else
{
    System.out.println("i is greater than 15");
}
```



---

# 35. SWITCH STATEMENT

`switch` is a selection statement.

It compares an expression with different `case` values.

## Basic syntax

```java
switch (expression)
{
    case value1:
        // statements
        break;

    case value2:
        // statements
        break;

    default:
        // statements
        break;
}
```

The PPT specifically emphasizes the use of `break` to terminate the switch when a matching case is found. It also states that the switch expression can use `short`, `int`, `enum`, or string literals. 

---

# PROGRAM 15 — MONTH CONVERTER USING SWITCH

The PPT gives a program that converts a numerical month into its corresponding month name.

Basic structure:

```java
switch (monthNumber)
{
    case 1:
        monthString = "January";
        break;

    case 2:
        monthString = "February";
        break;

    case 3:
        monthString = "March";
        break;

    case 4:
        monthString = "April";
        break;

    case 5:
        monthString = "May";
        break;

    case 6:
        monthString = "June";
        break;

    case 7:
        monthString = "July";
        break;

    case 8:
        monthString = "August";
        break;

    case 9:
        monthString = "September";
        break;

    case 10:
        monthString = "October";
        break;

    case 11:
        monthString = "November";
        break;

    case 12:
        monthString = "December";
        break;

    default:
        monthString = "Invalid month number";
        break;
}
```



---

# 36. MULTIPLE CASES IN ONE BLOCK

The PPT gives a program to calculate the number of days in a month.

The important technique is:

```java
case 1:
case 3:
case 5:
case 7:
case 8:
case 10:
case 12:
    numDays = 31;
    break;
```

Several cases can execute the same block.

For 30-day months:

```java
case 4:
case 6:
case 9:
case 11:
    numDays = 30;
    break;
```

February is handled separately, including the year condition shown in the PPT. 

---

# 37. STRING IN SWITCH

The PPT also demonstrates using a String with `switch`.

Example:

```java
String username = "Iechikicara";

switch (username)
{
    case "Doe":
        System.out.println("Username is Doe");
        break;

    case "John":
        System.out.println("Username is John");
        break;

    case "Jane":
        System.out.println("Username is Jane");
        break;

    default:
        System.out.println("Username not found!");
}
```



---

# PART G — LOOPS

# 38. `while` LOOP

The `while` loop:

1. Checks the condition.
2. If true, executes the body.
3. Checks again.
4. Stops when the condition becomes false.

## Syntax

```java
while (condition)
{
    // statements
}
```



---

# PROGRAM 16 — WHILE LOOP

```java
class WhileDemo {

    public static void main(String[] args) {

        int count = 1;

        while (count < 11) {

            System.out.println(
                "Count is: " + count
            );

            count++;
        }
    }
}
```

Output:

```text
Count is: 1
Count is: 2
...
Count is: 10
```



### Remember:

```text
while → condition first
```

---

# 39. `do-while` LOOP

The main difference:

### `while`

Checks condition **before** executing.

### `do-while`

Executes the body first and checks the condition **afterwards**.

Therefore, a `do-while` body executes **at least once**. 

## Syntax

```java
do
{
    // statements
}
while (condition);
```

---

# PROGRAM 17 — DO-WHILE

```java
class DoWhileDemo {

    public static void main(String[] args) {

        int count = 1;

        do {

            System.out.println(
                "Count is: " + count
            );

            count++;

        } while (count < 11);
    }
}
```



### Memory trick:

```text
while     → Check → Execute
do-while  → Execute → Check
```

---

# 40. `for` LOOP

The `for` statement provides a compact way to repeat statements over a range of values.

## Syntax

```java
for (initialization; condition; increment)
{
    // statements
}
```

### Three parts

1. **Initialization** → executes once at the beginning.
2. **Termination/condition** → decides whether loop continues.
3. **Increment** → executes after each iteration.



---

# PROGRAM 18 — FOR LOOP

```java
class ForDemo {

    public static void main(String[] args) {

        for (int i = 1; i < 11; i++) {

            System.out.println(
                "Count is: " + i
            );
        }
    }
}
```

Output:

```text
Count is: 1
Count is: 2
...
Count is: 10
```



---

# 41. ENHANCED `for` / FOR-EACH

The enhanced `for` is useful for iterating through:

* Arrays
* Collections

It makes loops more compact and easier to read. 

## Syntax

```java
for (dataType variable : array)
{
    // statements
}
```

---

# PROGRAM 19 — ENHANCED FOR

```java
class EnhancedForDemo {

    public static void main(String[] args) {

        int[] numbers = {
            1, 2, 3, 4, 5,
            6, 7, 8, 9, 10
        };

        for (int item : numbers) {

            System.out.println(
                "Count is: " + item
            );
        }
    }
}
```



### Easy difference

Normal:

```java
for (int i = 0; i < a.length; i++)
```

Enhanced:

```java
for (int item : a)
```

---

# PART H — JUMP STATEMENTS

# 42. `break`

`break` is used to terminate a loop.

The PPT discusses two types:

1. Unlabelled `break`
2. Labelled `break` 

---

# 43. UNLABELLED BREAK

Unlabelled `break` terminates the **immediate/innermost loop**.

Example idea:

```java
for (...)
{
    if (condition)
    {
        break;
    }
}
```

When `break` executes, control moves outside that loop.

---

# PROGRAM 20 — SEARCH USING BREAK

The PPT searches for `12` in an array.

```java
class BreakDemo_UnLabelled {

    public static void main(String[] args) {

        int[] arrayOfInts =
            {32, 87, 3, 589, 12, 1076, 2000, 8, 622, 127};

        int searchfor = 12;

        int i;
        boolean foundIt = false;

        for (i = 0; i < arrayOfInts.length; i++) {

            if (arrayOfInts[i] == searchfor) {

                foundIt = true;
                break;
            }
        }

        if (foundIt) {
            System.out.println(
                "Found " + searchfor +
                " at index " + i
            );
        }
        else {
            System.out.println(
                searchfor + " not in the array"
            );
        }
    }
}
```



### Main idea

```text
Search
 ↓
Found?
 ↓ YES
break
 ↓
Exit loop
```

---

# 44. LABELLED BREAK

A labelled `break` can terminate an **outer loop**.

## Syntax

```java
label:
for (...)
{
    for (...)
    {
        if (condition)
        {
            break label;
        }
    }
}
```

The PPT uses the label:

```java
search:
```

and searches a two-dimensional array. When the value is found, `break search;` terminates the outer loop. 

---

# PROGRAM 21 — LABELLED BREAK

Important structure from the PPT:

```java
class BreakWithLabelDemo {

    public static void main(String[] args) {

        int[][] arrayOfInts = {
            {32, 87, 3, 589},
            {12, 1076, 2000, 8},
            {622, 127, 77, 955}
        };

        int searchfor = 12;

        int i;
        int j = 0;
        boolean foundIt = false;

        search:
        for (i = 0; i < arrayOfInts.length; i++) {

            for (j = 0;
                 j < arrayOfInts[i].length;
                 j++) {

                if (arrayOfInts[i][j] == searchfor) {

                    foundIt = true;
                    break search;
                }
            }
        }

        if (foundIt) {
            System.out.println(
                "Found " + searchfor +
                " at " + i + ", " + j
            );
        }
        else {
            System.out.println(
                searchfor + " not in the array"
            );
        }
    }
}
```



---

# 45. `continue`

`continue` skips the current iteration and moves to the next iteration of the loop.

The PPT discusses:

* Unlabelled `continue`
* Labelled `continue` 

---

# PROGRAM 22 — UNLABELLED CONTINUE

The PPT uses a String and counts the number of occurrences of `'p'`.

```java
class ContinueDemo_Unlabelled {

    public static void main(String[] args) {

        String searchMe =
            "peter piper picked a " +
            "peck of pickled peppers";

        int max = searchMe.length();
        int numPs = 0;

        for (int i = 0; i < max; i++) {

            if (searchMe.charAt(i) != 'p')
                continue;

            numPs++;
        }

        System.out.println(
            "Found " + numPs +
            " p's in the string."
        );
    }
}
```

Output shown in the PPT:

```text
Found 9 p's in the string.
```



### Main idea

```text
Current character is not p?
        ↓
continue
        ↓
Skip remaining statements
        ↓
Next iteration
```

---

# 46. LABELLED CONTINUE

A labelled `continue` skips the current iteration of an **outer loop** marked by a label.

Example structure:

```java
outer:
for (initialization; condition; iteration)
{
    for (initialization; condition; iteration)
    {
        if (condition)
            continue outer;

        statement;
    }
}
```

The PPT specifically explains that labelled `continue` transfers execution to the next iteration and condition checking of the labelled outer loop. 

---

# 47. `return`

`return` is listed in the PPT's **Jump/Branching Statements** section, but the module does not provide a separate detailed `return` slide or program. 

So for this PPT, remember:

```text
Jump statements:
break
continue
return
```

---

# VERY IMPORTANT DIFFERENCES

## `if` vs `switch`

| `if`                                   | `switch`                        |
| -------------------------------------- | ------------------------------- |
| Used for conditions                    | Used to select among cases      |
| Can use relational/logical expressions | Matches case values             |
| Good for ranges/complex conditions     | Good for multiple fixed choices |

---

## `while` vs `do-while`

| while                   | do-while                     |
| ----------------------- | ---------------------------- |
| Condition checked first | Condition checked after body |
| May execute zero times  | Executes at least once       |
| `while(condition)`      | `do { } while(condition);`   |



---

## `for` vs enhanced `for`

| Normal `for`                | Enhanced `for`              |
| --------------------------- | --------------------------- |
| Uses index                  | Directly gets elements      |
| More control over index     | Simpler and shorter         |
| `for(int i=0;...)`          | `for(int x : array)`        |
| Useful when index is needed | Useful for simple traversal |



---

## `break` vs `continue`

| `break`                           | `continue`                      |
| --------------------------------- | ------------------------------- |
| Terminates loop                   | Skips current iteration         |
| Control exits loop                | Control moves to next iteration |
| Used to stop searching/processing | Used to skip unwanted values    |

### Memory trick

**BREAK = Stop**

**CONTINUE = Skip and go next**

---

# IMPORTANT PROGRAM PATTERNS TO MEMORIZE

For the exam, don't try to memorize every line separately. Memorize these patterns.

## 1-D array traversal

```java
for (int i = 0; i < array.length; i++)
{
    System.out.println(array[i]);
}
```

## 2-D array traversal

```java
for (int i = 0; i < matrix.length; i++)
{
    for (int j = 0; j < matrix[i].length; j++)
    {
        System.out.print(matrix[i][j] + " ");
    }

    System.out.println();
}
```

## Array sum

```java
int sum = 0;

for (int i = 0; i < array.length; i++)
{
    sum += array[i];
}
```

## Array maximum

```java
int max = array[0];

for (int i = 1; i < array.length; i++)
{
    if (array[i] > max)
        max = array[i];
}
```

## Matrix sum

```java
int sum = 0;

for (int i = 0; i < matrix.length; i++)
{
    for (int j = 0; j < matrix[i].length; j++)
    {
        sum += matrix[i][j];
    }
}
```

## Matrix addition

```java
result[i][j] =
    matrix1[i][j] + matrix2[i][j];
```

---

# IMPORTANT SYNTAX SHEET

## Class

```java
class ClassName
{
}
```

## Main method

```java
public static void main(String[] args)
{
}
```

## Output

```java
System.out.println();
```

## Input using Scanner

```java
import java.util.Scanner;

Scanner sc = new Scanner(System.in);
```

## Variable

```java
dataType variableName = value;
```

Example:

```java
int x = 10;
```

## 1-D array

```java
int[] a = new int[5];
```

## Array initialization

```java
int[] a = {1, 2, 3, 4, 5};
```

## 2-D array

```java
int[][] matrix = new int[3][3];
```

## If

```java
if (condition)
{
}
```

## If-else

```java
if (condition)
{
}
else
{
}
```

## If-else-if

```java
if (condition1)
{
}
else if (condition2)
{
}
else
{
}
```

## Switch

```java
switch (expression)
{
    case value:
        statements;
        break;

    default:
        statements;
}
```

## While

```java
while (condition)
{
}
```

## Do-while

```java
do
{
}
while (condition);
```

## For

```java
for (initialization; condition; increment)
{
}
```

## Enhanced for

```java
for (dataType variable : array)
{
}
```

## Break

```java
break;
```

## Labelled break

```java
label:
for (...)
{
    ...
    break label;
}
```

## Continue

```java
continue;
```

## Labelled continue

```java
continue label;
```

---

# TYPE CONVERSION / CASTING / AUTOMATIC PROMOTION

The module outline explicitly includes:

* Type Conversion and Casting
* Automatic Type Promotion in Expressions. 

However, the provided PPT pages do **not contain detailed explanatory slides/examples for these topics** in the material available here. Since you asked for notes **strictly based on the document**, I have not inserted additional outside explanations or rules that are not presented in the PPT.

### Exam checklist

Make sure you know these headings because they are explicitly part of Module 1:

```text
Type Conversion
Casting
Automatic Type Promotion in Expressions
```

---

# MOST IMPORTANT 15-MARK QUESTIONS

Based on the coverage and depth of the PPT, these are the topics I would prioritize for your internal exam.

### ⭐⭐⭐⭐⭐ Very Important

1. **Explain Java features/buzzwords.**
2. **Explain JDK, JRE and JVM with their relationship.**
3. **Explain Java architecture and execution process.**
4. **Explain bytecode and why Java is portable/architecture neutral.**
5. **Explain Java data types with size and range.**
6. **Explain arrays and their initialization methods.**
7. **Explain one-dimensional arrays with programs.**
8. **Explain two-dimensional arrays with programs.**
9. **Write a Java program for addition of two matrices.**
10. **Explain operators in Java with examples.**
11. **Explain control-flow statements in Java.**
12. **Explain `if`, `if-else`, nested `if` and `if-else-if`.**
13. **Explain switch statement with examples.**
14. **Explain `while`, `do-while`, `for` and enhanced `for`.**
15. **Explain `break` and `continue`, including labelled versions.**

---

# PROGRAMS YOU SHOULD DEFINITELY PRACTICE

For the exam, prioritize these:

### ⭐⭐⭐⭐⭐

1. Addition of two numbers — hardcoded
2. Addition using Scanner
3. Addition using command-line arguments
4. 1-D array input and display
5. Average of array
6. Sum of array elements
7. Maximum element in an array
8. String array
9. Display 2-D array
10. Sum of matrix elements
11. Maximum element in matrix
12. String 2-D array
13. Addition of two matrices
14. Month converter using `switch`
15. Number of days in month using `switch`
16. `while` loop
17. `do-while` loop
18. `for` loop
19. Enhanced `for`
20. Search an array using `break`
21. Search 2-D array using labelled `break`
22. Count characters using `continue`

---

# LAST-MINUTE REVISION — 1 PAGE

## Java basics

```text
C → C++ → Java
```

Java features:

```text
Simple
Object Oriented
Distributed
Multithreaded
Dynamic
Architecture Neutral
Portable
High Performance
Robust
Secure
```

---

## Java architecture

```text
JDK
 ↓
JRE
 ↓
JVM
 ↓
Bytecode execution
```

### Remember:

```text
JDK → Develop
JRE → Run
JVM → Execute
```

---

## Java execution

```text
.java
 ↓
javac
 ↓
.class / Bytecode
 ↓
JVM
 ↓
Output
```

---

## Data types

### Primitive

```text
byte
short
int
long
float
double
char
boolean
```

### Non-primitive

```text
Reference/Object types
Arrays
```

---

## Array

```java
int[] a = {1, 2, 3};
```

First index:

```text
0
```

Length:

```java
a.length
```

---

## Operators

```text
Arithmetic
Assignment
Relational
Logical
Unary
Ternary
Bitwise
Shift
instanceof
```

---

## Control flow

```text
Selection
 ├── if
 ├── if-else
 ├── if-else-if
 ├── nested-if
 └── switch

Iteration
 ├── while
 ├── do-while
 ├── for
 └── enhanced for

Jump
 ├── break
 ├── continue
 └── return
```



---

# EASY MEMORY TRICKS

### Java architecture

**JDK → JRE → JVM**

> **Develop → Run → Execute**

### Loops

> **while = check first**

> **do-while = execute first**

> **for = initialization, condition, increment**

> **for-each = directly take each element**

### Jump statements

> **break = stop**

> **continue = skip**

> **return = return control/value**

### Arrays

> **1-D = one loop**

> **2-D = two loops**

### Matrix addition

> **Same position + Same position**

```java
result[i][j] =
    a[i][j] + b[i][j];
```

---

## FINAL EXAM STRATEGY

For a **15-mark theory/program question**, use this order whenever possible:

### 1. Definition

Write 2–3 simple lines.

### 2. Key points

Write 5–8 bullet points.

### 3. Syntax

Put the syntax in a separate code block.

### 4. Program

Write the relevant Java program.

### 5. Explanation

Explain the important lines/logic.

### 6. Output

If applicable, show the output.

This makes the answer easy to **remember, write and score marks**.

The notes above cover the complete topic flow of the uploaded Module 1, including the Java introduction, architecture, data types, arrays, operators, and control-flow material through the final labelled `continue` topic.    

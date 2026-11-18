# cheat-sheet
Prog exam
JAVA PROGRAMMING EXAM CHEAT SHEET
Exam preparation guide
JAVA MASTER REFERENCE
Applications Development & Information Sciences
LANGUAGE

Java

LEVEL

Beginner to intermediate

ENVIRONMENT

NetBeans

PURPOSE

Exam reference



Main topics
- Java fundamentals and syntax
- Variables, data types and operators
- Input and output
- Selection and repetition
- Methods and arrays
- Object-oriented programming
- Inheritance, interfaces and abstraction
- Exception handling and debugging
- Java utility classes and exam techniques

PART 1: JAVA PROGRAMMING FUNDAMENTALS
1.1 What is Java?
Java is a high-level, object-oriented programming language used to develop applications.

Important characteristics:
- Object-oriented: Uses classes and objects.
- Platform-independent: Java programs compile into bytecode that runs on the Java Virtual Machine (JVM).
- Secure: Provides features such as bytecode verification and controlled memory access.
- Strongly typed: Variables must have declared data types.
- Robust: Supports exception handling and automatic memory management.
How Java works:
1. Source code

MyProgram.java

2. Java compiler (javac)

Compiles the source code

3. Bytecode

MyProgram.class

4. JVM

Java Virtual Machine executes bytecode

Program executes

Remember:
- JDK = Java Development Kit (tools to develop Java programs).
- JRE = Java Runtime Environment (runtime libraries and components).
- JVM = Java Virtual Machine (executes Java bytecode).
1.2 Basic Java program structure
Every Java program needs a class. A typical executable application has a main() method.
public class MyProgram {

    public static void main(String[] args) {

        System.out.println("Hello World!");

    }
}


Explanation:
Code	Meaning
public	Accessible from other classes
class	Declares a class
MyProgram	Name of the class
static	Can be called without creating an object
void	Does not return a value
main	Starting point of the application
String[] args	Receives command-line arguments
System.out.println()	Displays output

Important exam rules:
1. Java is case-sensitive.
2. Every statement normally ends with a semicolon ;.
3. Opening curly braces { must have matching closing braces }.
4. The public class name must match the filename.
5. The main() method must have the correct signature for the standard Java application entry point.
1.3 Comments
Comments explain code and are ignored by the compiler.
// Single-line comment

/*
 Multi-line comment
 Used for longer explanations.
*/

/**
 * Documentation comment.
 * Used to document classes and methods.
 */


Use comments to explain why code is written, especially when the logic is complicated.
PART 2: VARIABLES AND DATA TYPES
2.1 What is a variable?
A variable is a named storage location that holds information while a program executes.

Example:
int age = 20;
String name = "John";
double salary = 15000.50;


Structure:
dataType variableName = value;


2.2 Java data types
Java has two main categories of data types: primitive and reference types.

Primitive data types
Data type	Description	Example
int	Whole numbers	int age = 20;
double	Decimal numbers	double price = 99.99;
float	Decimal numbers, less precision	float rate = 5.5f;
long	Large whole numbers	long population = 9000000L;
short	Smaller whole numbers	short number = 100;
byte	Very small whole numbers	byte level = 10;
char	Single character	char grade = 'A';
boolean	True or false	boolean passed = true;

Reference data types

These refer to objects rather than storing primitive values directly.

Examples:
String name = "Sayuren";

int[] numbers = {10, 20, 30};

Scanner input = new Scanner(System.in);


2.3 Declaring and initializing variables
Declaration:
int age;


Initialization:
age = 21;


Declaration and initialization together:
int age = 21;


Updating a variable:
age = 25;


2.4 Constants
A constant is a value that cannot be changed after initialization.

Use final.
final double VAT = 0.15;

final int MAX_USERS = 100;


Attempting to change a final variable results in a compilation error.
2.5 Naming conventions
Good variable names describe their purpose.
int studentAge;
double accountBalance;
String firstName;


Avoid:
int x;
double a;
String q;


Unless they are short-lived mathematical variables where the meaning is obvious.

Java naming conventions:
- Variables: studentName
- Methods: calculateTotal()
- Classes: StudentDetails
- Constants: MAXIMUM_SCORE
- Packages: com.mycompany.application
2.6 Type casting
Type casting converts a value from one data type to another.

Widening casting (automatic):
int number = 10;

double result = number;

System.out.println(result); // 10.0


An integer can automatically become a double.

Narrowing casting (manual):
double price = 99.99;

int result = (int) price;

System.out.println(result); // 99


The decimal portion is removed, not rounded.

Exam warning: Narrowing can cause data loss.
2.7 String operations
A String stores text.
String name = "John Smith";


Useful String methods:
Method	Purpose	Example
length()	Counts characters	name.length()
toUpperCase()	Converts to uppercase	name.toUpperCase()
toLowerCase()	Converts to lowercase	name.toLowerCase()
charAt(0)	Gets character at index	name.charAt(0)
substring(0, 4)	Extracts part of String	name.substring(0, 4)
equals()	Compares String contents	name.equals("John")
equalsIgnoreCase()	Compares ignoring case	name.equalsIgnoreCase("john")
contains()	Checks whether text exists	name.contains("Smith")
trim()	Removes leading/trailing whitespace	name.trim()
replace()	Replaces characters/text	name.replace("John", "Sam")

VERY IMPORTANT: Comparing Strings

Incorrect:
if (name == "John") {
    System.out.println("Match");
}


Correct:
if (name.equals("John")) {
    System.out.println("Match");
}


Why? == compares object references, whereas .equals() compares String contents.
PART 3: OPERATORS
Operators perform calculations and comparisons.
3.1 Arithmetic operators
Operator	Meaning	Example	Result
+	Addition	10 + 5	15
-	Subtraction	10 - 5	5
*	Multiplication	10 * 5	50
/	Division	10 / 5	2
%	Modulus (remainder)	10 % 3	1

Understanding modulus (%)
int number = 10;

System.out.println(number % 2);


Output: 0

Modulus is extremely useful for checking even and odd numbers.
if (number % 2 == 0) {
    System.out.println("Even");
} else {
    System.out.println("Odd");
}


3.2 Relational operators
Used to compare two values.
Operator	Meaning
==	Equal to
!=	Not equal to
>	Greater than
<	Less than
>=	Greater than or equal to
<=	Less than or equal to

Example:
int age = 20;

System.out.println(age >= 18);


Output: true
3.3 Logical operators
| Operator | Meaning | Example |
|---|---|---|
| && | AND | age >= 18 && age <= 60 |
| || | OR | age < 18 || age > 60 |
| ! | NOT | !isValid |

Truth table
A	B	A && B	A || B
true	true	true	true
true	false	false	true
false	true	false	true
false	false	false	false

3.4 Increment and decrement
int number = 5;

number++; // 6

number--; // 5


Other forms:
number += 5; // number = number + 5

number -= 2; // number = number - 2

number *= 3; // number = number * 3

number /= 2; // number = number / 2


Exam tip: Understand the difference between number++ and ++number when they are used inside larger expressions.
int x = 5;

System.out.println(x++); // Prints 5

System.out.println(x);   // Prints 6


int y = 5;

System.out.println(++y); // Prints 6


PART 4: INPUT AND OUTPUT
4.1 Displaying information
Java uses System.out to display information.
System.out.print("Hello");

System.out.println("World");

System.out.printf("Age: %d", 20);


Difference:
- print() displays text without automatically moving to a new line.
- println() displays text and moves to a new line.
- printf() formats output.
4.2 Using Scanner for input
The Scanner class allows users to enter information.

Import it:
import java.util.Scanner;


Example:
import java.util.Scanner;

public class UserInput {

    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);

        System.out.print("Enter your name: ");

        String name = input.nextLine();

        System.out.println("Welcome " + name);

        input.close();
    }
}


Important Scanner methods
Method	Input
nextInt()	Integer
nextDouble()	Double
nextFloat()	Float
nextBoolean()	Boolean
next()	One word
nextLine()	Entire line of text
nextLong()	Long integer

4.3 The Scanner nextLine() problem
One of the most common Java exam and practical programming mistakes.

Problem:
int age = input.nextInt();

String name = input.nextLine();


The nextLine() may consume the leftover newline after nextInt().

Solution:
int age = input.nextInt();

input.nextLine(); // Consume leftover newline

String name = input.nextLine();


Remember to use this after nextInt(), nextDouble() and similar token-reading methods when you subsequently need a full line.
4.4 Formatting output
double price = 125.5678;

System.out.printf("Price: R%.2f", price);


Output:
Price: R125.57


Useful formatting symbols:
Symbol	Meaning
%d	Integer
%f	Decimal
%.2f	Decimal to 2 places
%s	String
%c	Character
%n	New line

PART 5: CONDITIONAL STATEMENTS
Conditional statements allow a program to make decisions.
5.1 if statement
Used when a condition must be checked.
int age = 20;

if (age >= 18) {

    System.out.println("You are an adult");

}


5.2 if-else statement
int age = 16;

if (age >= 18) {

    System.out.println("Adult");

} else {

    System.out.println("Minor");

}


5.3 if-else-if statement
Used when multiple conditions need to be checked.
int mark = 75;

if (mark >= 80) {

    System.out.println("Distinction");

} else if (mark >= 70) {

    System.out.println("Good");

} else if (mark >= 50) {

    System.out.println("Pass");

} else {

    System.out.println("Fail");

}


Output: Good

Important: Conditions are checked from top to bottom. Once a condition is true, the remaining branches are skipped.
5.4 Nested if statements
An if statement inside another if statement.
int age = 20;
boolean hasID = true;

if (age >= 18) {

    if (hasID) {

        System.out.println("Entry allowed");

    }

}


5.5 Switch statements
Useful when comparing one variable against several specific values.
int choice = 2;

switch (choice) {

    case 1:
        System.out.println("Home");
        break;

    case 2:
        System.out.println("Settings");
        break;

    case 3:
        System.out.println("Exit");
        break;

    default:
        System.out.println("Invalid choice");
}


What does break do?

It stops execution from continuing into the next case in a traditional switch statement.

What does default do?

It executes when no case matches.
5.6 Ternary operator
A shorter way of writing a simple if-else statement.
int age = 20;

String result = (age >= 18) ? "Adult" : "Minor";

System.out.println(result);


Structure:
condition ? valueIfTrue : valueIfFalse;


PART 6: LOOPS AND REPETITION
Loops allow code to execute repeatedly.
6.1 for loop
Used when the number of repetitions is known or controlled by a counter.
for (int i = 1; i <= 5; i++) {

    System.out.println(i);

}


Output:
1
2
3
4
5


Breakdown:
for (initialization; condition; update)


- Initialization: Creates the counter.
- Condition: Determines whether the loop continues.
- Update: Changes the counter.
6.2 while loop
Used when repetition depends on a condition.
int i = 1;

while (i <= 5) {

    System.out.println(i);

    i++;

}


Important: Always ensure the condition can eventually become false, otherwise you may create an infinite loop.
6.3 do-while loop
Executes the code at least once before checking the condition.
int number = 1;

do {

    System.out.println(number);

    number++;

} while (number <= 5);


6.4 Difference between loops
Loop	When to use	Executes at least once?
for	Known repetitions	No
while	Condition-controlled repetition	No
do-while	Must execute once before checking	Yes

6.5 Break and continue
break: Completely exits the loop.
for (int i = 1; i <= 10; i++) {

    if (i == 5) {
        break;
    }

    System.out.println(i);
}


Output: 1, 2, 3, 4.

continue: Skips the current iteration and moves to the next.
for (int i = 1; i <= 5; i++) {

    if (i == 3) {
        continue;
    }

    System.out.println(i);
}


Output: 1, 2, 4, 5.
6.6 Nested loops
A loop inside another loop.
for (int i = 1; i <= 3; i++) {

    for (int j = 1; j <= 3; j++) {

        System.out.print("* ");

    }

    System.out.println();
}


Output:
* * *
* * *
* * *


Useful for multiplication tables, patterns and two-dimensional arrays.
PART 7: METHODS
7.1 What is a method?
A method is a block of code that performs a specific task. Methods help organise programs, reduce repetition and make code easier to maintain.

Example:
public static void greet() {

    System.out.println("Welcome to Java!");

}


Calling the method:
greet();


Output:
Welcome to Java!


7.2 Method structure
public static int calculateTotal(int a, int b) {

    int total = a + b;

    return total;
}


Component	Meaning
public	Access modifier
static	Belongs to the class
int	Return data type
calculateTotal	Method name
int a, int b	Parameters
return	Sends a value back

7.3 Void methods
A void method does not return a value.
public static void displayName(String name) {

    System.out.println(name);

}


Calling it:
displayName("John");


7.4 Methods that return values
public static int addNumbers(int a, int b) {

    return a + b;

}


Using the returned value:
int answer = addNumbers(10, 20);

System.out.println(answer);


Output: 30

Remember:
- void = returns nothing.
- int = returns an integer.
- double = returns a decimal number.
- String = returns text.
- boolean = returns true or false.
The returned value must be compatible with the declared return type.
7.5 Parameters vs arguments
These are frequently confused in exams.

Parameters: Variables declared in the method definition.
public static void greet(String name)


Here, name is a parameter.

Arguments: Actual values passed when calling the method.
greet("Sayuren");


Here, "Sayuren" is an argument.
7.6 Method overloading
Method overloading occurs when multiple methods have the same name but different parameter lists.
public static int add(int a, int b) {

    return a + b;

}

public static int add(int a, int b, int c) {

    return a + b + c;

}

public static double add(double a, double b) {

    return a + b;

}


Calling the methods:
System.out.println(add(5, 10));

System.out.println(add(5, 10, 15));

System.out.println(add(2.5, 3.5));


Important exam rule: You cannot overload a method simply by changing its return type. The parameter list must differ.
7.7 Method overriding
Method overriding occurs when a subclass provides its own implementation of a method inherited from its superclass.
class Animal {

    public void makeSound() {

        System.out.println("Animal sound");

    }
}

class Dog extends Animal {

    @Override
    public void makeSound() {

        System.out.println("Bark!");

    }
}


Calling:
Dog dog = new Dog();

dog.makeSound();


Output: Bark!

Difference between overloading and overriding
Overloading	Overriding
Same method name	Same inherited method signature
Different parameter lists	Same parameter list
Usually within the same class	Between superclass and subclass
Compile-time polymorphism	Runtime polymorphism

7.8 Variable scope
Scope determines where a variable can be accessed.

Local variable

Declared inside a method.
public void calculate() {

    int total = 100;

}


Only accessible within its scope.

Instance variable

Declared inside a class but outside methods.
class Student {

    String name;
    int age;

}


Each object gets its own instance variables.

Static variable

Belongs to the class and is shared by its instances.
class Student {

    static String schoolName = "IIE";

}


Access:
System.out.println(Student.schoolName);


PART 8: ARRAYS
8.1 What is an array?
An array stores multiple values of the same data type in one variable.

Instead of creating:
int mark1 = 70;
int mark2 = 80;
int mark3 = 90;


You can create:
int[] marks = {70, 80, 90};


8.2 Declaring arrays
int[] numbers;

numbers = new int[5];


Or:
int[] numbers = new int[5];


This creates an array with five integer positions.
8.3 Array indexing
Java arrays start counting from index 0.
Example array
10

Index 0

20

Index 1

30

Index 2

40

Index 3

50

Index 4


First element = index 0. Last element = index 4.

Accessing an element:
int[] numbers = {10, 20, 30, 40, 50};

System.out.println(numbers[0]); // 10

System.out.println(numbers[2]); // 30


Changing an element:
numbers[1] = 99;


8.4 Array length
Use .length to determine the number of elements.
int[] numbers = {10, 20, 30};

System.out.println(numbers.length);


Output: 3

Important distinction:
- Arrays use .length.
- Strings use .length().
- ArrayLists use .size().
8.5 Looping through arrays
Using a for loop:
int[] marks = {70, 80, 90, 65};

for (int i = 0; i < marks.length; i++) {

    System.out.println(marks[i]);

}


Using an enhanced for loop:
for (int mark : marks) {

    System.out.println(mark);

}


Difference:
- Standard for loop gives access to the index.
- Enhanced for loop directly gives you each element.
8.6 Calculating the sum and average
This is a very common exam question.
int[] marks = {70, 80, 90, 60};

int total = 0;

for (int i = 0; i < marks.length; i++) {

    total += marks[i];

}

double average = (double) total / marks.length;

System.out.println("Total: " + total);

System.out.println("Average: " + average);


Output:
Total: 300
Average: 75.0


Why use (double)?

It ensures decimal division rather than integer division.
8.7 Finding the highest and lowest value
int[] numbers = {20, 45, 10, 80, 30};

int highest = numbers[0];

int lowest = numbers[0];

for (int i = 1; i < numbers.length; i++) {

    if (numbers[i] > highest) {

        highest = numbers[i];

    }

    if (numbers[i] < lowest) {

        lowest = numbers[i];

    }
}

System.out.println("Highest: " + highest);

System.out.println("Lowest: " + lowest);


Exam insight: Initialise the highest and lowest variables using the first array element rather than zero. This works correctly with arrays containing only negative numbers.
8.8 Searching an array
Linear search checks each element until a match is found.
int[] numbers = {10, 20, 30, 40, 50};

int search = 30;

boolean found = false;

for (int i = 0; i < numbers.length; i++) {

    if (numbers[i] == search) {

        found = true;

        System.out.println("Found at index: " + i);

        break;
    }
}

if (!found) {

    System.out.println("Number not found");

}


8.9 Sorting an array
Java provides the Arrays utility class.
import java.util.Arrays;

int[] numbers = {50, 20, 40, 10, 30};

Arrays.sort(numbers);

System.out.println(Arrays.toString(numbers));


Output:
[10, 20, 30, 40, 50]


Other useful methods:
Arrays.toString(numbers);

Arrays.equals(array1, array2);

Arrays.fill(numbers, 0);

Arrays.copyOf(numbers, numbers.length);


8.10 Two-dimensional arrays
A two-dimensional array stores information in rows and columns.
int[][] numbers = {

    {1, 2, 3},

    {4, 5, 6},

    {7, 8, 9}

};


Accessing values:
System.out.println(numbers[0][0]); // 1

System.out.println(numbers[1][2]); // 6


Nested loops:
for (int i = 0; i < numbers.length; i++) {

    for (int j = 0; j < numbers[i].length; j++) {

        System.out.print(numbers[i][j] + " ");

    }

    System.out.println();
}


Output:
1 2 3
4 5 6
7 8 9


8.11 Arrays of objects
An array can store references to objects rather than primitive values.
Student[] students = new Student[3];

students[0] = new Student("John", 20);

students[1] = new Student("Mary", 21);

students[2] = new Student("Peter", 19);


You can loop through them:
for (int i = 0; i < students.length; i++) {

    System.out.println(students[i].getName());

}


This is particularly important in object-oriented programming.
PART 9: OBJECT-ORIENTED PROGRAMMING (OOP)
High-priority exam topic
Object-oriented programming is a programming approach based on classes and objects.

It helps developers create reusable, organised and maintainable applications.

The four main OOP principles are:
1. Encapsulation
2. Inheritance
3. Polymorphism
4. Abstraction
9.1 Classes
A class is a blueprint or template used to create objects.

Example:
public class Student {

    String name;

    int age;

}


The class describes what a student object will contain.
9.2 Objects
An object is an instance of a class.
Student student1 = new Student();

student1.name = "John";

student1.age = 20;


Creating another object:
Student student2 = new Student();

student2.name = "Mary";

student2.age = 21;


Each object has its own instance data.

Remember:
- Class = blueprint.
- Object = instance of a class.
- Attribute = data belonging to a class or object.
- Method = behaviour or action of a class or object.
9.3 Attributes
Attributes are variables declared within a class.
public class Car {

    String colour;

    String model;

    int year;

}


Here, colour, model and year are attributes.
9.4 Constructors
A constructor is a special method used to initialise an object.

It has the same name as the class and does not have a return type.
public class Student {

    String name;

    int age;

    public Student(String studentName, int studentAge) {

        name = studentName;

        age = studentAge;

    }
}


Creating an object:
Student student1 = new Student("John", 20);


The constructor automatically runs when the object is created.

Default constructor:
public Student() {

    name = "Unknown";

    age = 0;

}


Parameterized constructor:
public Student(String name, int age) {

    this.name = name;

    this.age = age;

}


The this keyword

Refers to the current object.

It is commonly used to distinguish instance variables from parameters with the same names.
this.name = name;


Left side: object's instance variable.

Right side: parameter.
9.5 Encapsulation
Encapsulation means protecting an object's data by restricting direct access to its internal attributes.

Usually achieved through:
- Private attributes.
- Public getter methods.
- Public setter methods.
Example:
public class Student {

    private String name;

    private int age;

    public String getName() {

        return name;

    }

    public void setName(String name) {

        this.name = name;

    }

    public int getAge() {

        return age;

    }

    public void setAge(int age) {

        if (age >= 0) {

            this.age = age;

        }

    }
}


Using the class:
Student student = new Student();

student.setName("John");

student.setAge(20);

System.out.println(student.getName());

System.out.println(student.getAge());


Access modifiers
Modifier	Accessibility
public	Accessible from anywhere, subject to module/package accessibility
private	Only within the declaring class
protected	Same package and subclasses, subject to inheritance rules
Default (no modifier)	Same package

Exam definition: Encapsulation combines data and methods in a class while controlling access to the internal data.
9.6 Inheritance
Inheritance allows a subclass to acquire accessible attributes and methods from a superclass.

It promotes code reuse.

Example:
public class Animal {

    public void eat() {

        System.out.println("Animal is eating");

    }
}


Subclass:
public class Dog extends Animal {

    public void bark() {

        System.out.println("Dog is barking");

    }
}


Using inheritance:
Dog dog = new Dog();

dog.eat();

dog.bark();


Output:
Animal is eating
Dog is barking


Important terminology
Term	Meaning
Superclass	Parent class
Subclass	Child class
extends	Inherits from a class
super	Refers to superclass members or constructor
Inherited method	Method available from the superclass

The super keyword
Used to access superclass constructors, methods and fields.
class Animal {

    String name = "Animal";

}

class Dog extends Animal {

    String name = "Dog";

    public void display() {

        System.out.println(super.name);

        System.out.println(this.name);

    }
}


Output:
Animal
Dog


Calling a superclass constructor:
class Animal {

    public Animal(String name) {

        System.out.println(name);

    }
}

class Dog extends Animal {

    public Dog() {

        super("Animal");

    }
}


Important: A superclass constructor call using super() must be the first statement in a constructor.

Java supports single class inheritance: a class can extend only one direct superclass. However, a class can implement multiple interfaces.
9.7 Polymorphism
Polymorphism means one interface or parent type can represent different object types, allowing different behaviours.

There are two commonly taught forms:
- Compile-time polymorphism: method overloading.
- Runtime polymorphism: method overriding and dynamic method dispatch.
Example:
class Animal {

    public void makeSound() {

        System.out.println("Animal sound");

    }
}

class Dog extends Animal {

    @Override
    public void makeSound() {

        System.out.println("Bark");

    }
}

class Cat extends Animal {

    @Override
    public void makeSound() {

        System.out.println("Meow");

    }
}


Using polymorphism:
Animal animal1 = new Dog();

Animal animal2 = new Cat();

animal1.makeSound();

animal2.makeSound();


Output:
Bark
Meow


Why is this important?

The variable type is Animal, but the actual objects are Dog and Cat.

Java executes the overridden method belonging to the actual object's class.

This is called dynamic method binding or dynamic method dispatch.
9.8 Abstraction
Abstraction hides implementation details and exposes essential functionality.

In Java, abstraction is commonly achieved using:
1. Abstract classes.
2. Interfaces.
Abstract classes
An abstract class cannot be instantiated directly.
abstract class Animal {

    public abstract void makeSound();

    public void sleep() {

        System.out.println("Sleeping");

    }
}


Subclass:
class Dog extends Animal {

    @Override
    public void makeSound() {

        System.out.println("Bark");

    }
}


Using it:
Dog dog = new Dog();

dog.makeSound();

dog.sleep();


Important rules:
- An abstract class uses the abstract keyword.
- An abstract class cannot be instantiated.
- It can contain abstract and concrete methods.
- A concrete subclass must implement inherited abstract methods unless it is also abstract.
- Abstract classes can have constructors and instance variables.
Interfaces
An interface defines a contract that implementing classes agree to follow.
interface Printable {

    void print();

}


Implementing the interface:
class Report implements Printable {

    @Override
    public void print() {

        System.out.println("Printing report");

    }
}


Using it:
Report report = new Report();

report.print();


Important interface rules:
- A class uses implements to implement an interface.
- A class can implement multiple interfaces.
- Interface methods without a body are implicitly public and abstract.
- Interface fields are implicitly public static final.
- Interfaces can also contain default, static and private methods in modern Java.
9.9 Abstract classes vs interfaces
Abstract class	Interface
Uses abstract class	Uses interface
Extended using extends	Implemented using implements
A class extends one direct class	A class can implement multiple interfaces
Can have constructors	Cannot have constructors
Can have instance variables	Fields are constants
Can contain abstract and concrete methods	Can define abstract and implemented methods
Useful for shared base functionality and state	Useful for defining contracts and capabilities

Exam tip: If a question asks you to explain when to use an interface, mention that interfaces are useful when different classes need to follow the same contract without sharing a common superclass implementation.
PART 10: ADVANCED JAVA CLASS FEATURES
10.1 The Object class
Every Java class directly or indirectly inherits from java.lang.Object, unless it is Object itself.

Three important methods:
- toString()
- equals()
- getClass()
toString()
Returns a String representation of an object.

Default example:
Student student = new Student();

System.out.println(student.toString());


You can override it to provide meaningful information.
public class Student {

    private String name;

    private int age;

    public Student(String name, int age) {

        this.name = name;

        this.age = age;

    }

    @Override
    public String toString() {

        return "Name: " + name + ", Age: " + age;

    }
}


Using it:
Student s1 = new Student("John", 20);

System.out.println(s1);


Output:
Name: John, Age: 20


Notice that Java automatically calls toString() when an object is printed as a String.
equals()
Compares objects for equality.

By default, Object.equals() compares object identity, but classes can override it to compare their contents.
public class Student {

    private String name;

    public Student(String name) {

        this.name = name;

    }

    @Override
    public boolean equals(Object obj) {

        if (this == obj) {
            return true;
        }

        if (obj == null || getClass() != obj.getClass()) {
            return false;
        }

        Student other = (Student) obj;

        return name.equals(other.name);

    }
}


Using it:
Student s1 = new Student("John");

Student s2 = new Student("John");

System.out.println(s1.equals(s2));


Output: true

Remember: Overriding equals() should normally be accompanied by overriding hashCode() consistently.
getClass()
Returns the runtime class of an object.
Student student = new Student("John");

System.out.println(student.getClass());


Example output:
class Student


Useful when determining an object's actual class at runtime.
10.2 Packages
A package groups related Java classes and interfaces.

It helps organise code, avoid naming conflicts and control package-level access.

Example package structure:
src
 └── com.mycompany.application
      ├── Main.java
      ├── Student.java
      └── Teacher.java


Declaring a package:
package com.mycompany.application;

public class Student {

}


Importing a class:
import com.mycompany.application.Student;


Importing all accessible types in a package:
import com.mycompany.application.*;


Important: The package declaration must appear before imports and the class declaration.
10.3 The static keyword
static means a member belongs to the class rather than to each individual object.

Example:
class Counter {

    static int count = 0;

    public Counter() {

        count++;

    }
}


Using it:
Counter c1 = new Counter();

Counter c2 = new Counter();

Counter c3 = new Counter();

System.out.println(Counter.count);


Output: 3

Remember:
- Static variable = shared by all instances.
- Instance variable = separate for every object.
- Static method = called using the class name without needing an instance.
- Static methods cannot directly access instance members without an object reference.
10.4 The final keyword
Can be applied to variables, methods and classes.
final int MAX = 100;


Prevents reassignment of the variable.
final class Security {

}


Prevents the class from being subclassed.
class Animal {

    public final void breathe() {

        System.out.println("Breathing");

    }
}


Prevents subclasses from overriding that method.

Important: A final reference to an object cannot be reassigned, but the object's mutable contents may still be changed.
PART 11: EXCEPTION HANDLING
11.1 What is an exception?
An exception is an event that disrupts the normal flow of a program during execution.

Examples:
- Dividing by zero using integer division.
- Accessing an invalid array index.
- Converting invalid text into a number.
- Attempting to use a null reference.
11.2 try-catch
Used to handle exceptions without immediately terminating the program.
try {

    int number = 10 / 0;

} catch (ArithmeticException e) {

    System.out.println("Cannot divide by zero");

}


11.3 finally
The finally block normally executes whether an exception occurs or not.
try {

    int result = 10 / 2;

    System.out.println(result);

} catch (Exception e) {

    System.out.println("An error occurred");

} finally {

    System.out.println("Program completed");

}


Useful for cleanup operations.
11.4 Multiple catch blocks
try {

    int[] numbers = {10, 20, 30};

    System.out.println(numbers[5]);

} catch (ArithmeticException e) {

    System.out.println("Arithmetic error");

} catch (ArrayIndexOutOfBoundsException e) {

    System.out.println("Invalid array index");

} catch (Exception e) {

    System.out.println("Other error");

}


Important: Catch more specific exceptions before general exceptions.
11.5 Common Java exceptions
Exception	Meaning
ArithmeticException	Invalid arithmetic operation
NullPointerException	Using a null reference incorrectly
ArrayIndexOutOfBoundsException	Accessing an invalid array index
NumberFormatException	Invalid String-to-number conversion
InputMismatchException	Incorrect Scanner input type
IOException	Input/output operation problem
ClassCastException	Invalid object type casting

11.6 throw and throws
throw: Explicitly throws an exception.
if (age < 18) {

    throw new IllegalArgumentException("Must be 18 or older");

}


throws: Declares that a method may pass an exception to its caller.
public void readFile() throws IOException {

    // File reading code

}


Difference:
throw	throws
Used inside a method	Used in method declaration
Throws an exception object	Declares possible exceptions
Followed by an exception instance	Followed by exception class names

11.7 Checked vs unchecked exceptions
Checked	Unchecked
Checked by compiler	Not required to be handled at compile time
Must be caught or declared	Handling is not compulsory
Example: IOException	Example: NullPointerException

PART 12: JAVA COLLECTIONS AND UTILITY CLASSES
These are useful when working with groups of data.
12.1 ArrayList
An ArrayList is a resizable collection that stores objects.

Import:
import java.util.ArrayList;


Creating:
ArrayList<String> names = new ArrayList<>();


Adding values:
names.add("John");

names.add("Mary");

names.add("Peter");


Accessing values:
System.out.println(names.get(0));


Updating:
names.set(0, "David");


Removing:
names.remove("Mary");


Checking size:
names.size();


Checking if an item exists:
names.contains("Peter");


Looping:
for (String name : names) {

    System.out.println(name);

}


Clearing:
names.clear();


Array vs ArrayList
Array	ArrayList
Fixed length after creation	Resizable
Can store primitives and references	Stores objects (use wrapper classes for primitives)
Uses .length	Uses .size()
Direct indexing	Uses .get(index)
Less collection functionality built in	Many useful methods

12.2 Wrapper classes
Wrapper classes represent primitive values as objects.
Primitive	Wrapper
int	Integer
double	Double
char	Character
boolean	Boolean
long	Long
float	Float

Example:
Integer number = 10;

Double price = 99.99;


Java automatically converts between primitives and their wrapper types in many situations. This is called autoboxing and unboxing.
12.3 Math class
Useful mathematical methods:
Math.max(10, 20);      // 20

Math.min(10, 20);      // 10

Math.sqrt(25);         // 5.0

Math.pow(2, 3);        // 8.0

Math.abs(-10);         // 10

Math.round(5.7);       // 6

Math.ceil(5.2);        // 6.0

Math.floor(5.8);       // 5.0


Generating a random number:
int number = (int)(Math.random() * 10) + 1;


This generates an integer from 1 to 10 inclusive.
12.4 Random class
import java.util.Random;

Random random = new Random();

int number = random.nextInt(10) + 1;


Produces a random integer from 1 to 10 inclusive.
12.5 ArrayList vs arrays vs HashMap
Structure	Purpose
Array	Fixed-size collection of indexed elements
ArrayList	Resizable indexed collection
HashMap	Stores key-value pairs

HashMap example:
import java.util.HashMap;

HashMap<Integer, String> students = new HashMap<>();

students.put(1, "John");

students.put(2, "Mary");

System.out.println(students.get(1));


Output: John

PART 13: FILE HANDLING
File handling allows programs to read information from and write information to external files.
13.1 Writing to a file
Using FileWriter:
import java.io.FileWriter;
import java.io.IOException;

public class WriteFile {

    public static void main(String[] args) {

        try {

            FileWriter writer = new FileWriter("data.txt");

            writer.write("Welcome to Java!");

            writer.close();

            System.out.println("File written successfully");

        } catch (IOException e) {

            System.out.println("File error");

        }
    }
}


13.2 Reading from a file
Using Scanner:
import java.io.File;
import java.io.FileNotFoundException;
import java.util.Scanner;

public class ReadFile {

    public static void main(String[] args) {

        try {

            File file = new File("data.txt");

            Scanner reader = new Scanner(file);

            while (reader.hasNextLine()) {

                String line = reader.nextLine();

                System.out.println(line);

            }

            reader.close();

        } catch (FileNotFoundException e) {

            System.out.println("File not found");

        }
    }
}


13.3 Append to a file
FileWriter writer = new FileWriter("data.txt", true);


The true argument enables appending rather than replacing the existing file contents.

Remember: File handling commonly requires exception handling because file operations can fail.
PART 14: DEBUGGING AND COMMON PROGRAMMING ERRORS
Knowing how to identify errors is just as important as knowing how to write code.
14.1 Three main types of errors
Error type	Explanation	Example
Syntax error	Breaks Java grammar	Missing semicolon
Runtime error	Occurs during execution	Division by zero
Logical error	Program runs but produces incorrect output	Incorrect formula

Syntax error
Incorrect:
int age = 20


Correct:
int age = 20;


Runtime error
int number = 10 / 0;


This causes an ArithmeticException.
Logical error
int length = 10;

int width = 5;

int area = length + width;


The code compiles, but the formula is incorrect.

Correct:
int area = length * width;


14.2 Common NetBeans errors
Error	Possible solution
Cannot find symbol	Check variable, method or class name
Missing return statement	Add the required return value
Incompatible types	Check data types
Non-static variable cannot be referenced from static context	Create an object or make the member static where appropriate
Class not found	Check class name, package and project configuration
ArrayIndexOutOfBoundsException	Check array indexes
NullPointerException	Ensure the object has been initialised
Method does not override	Check method signature and inheritance

14.3 Debugging tips
1. Read the error message carefully.
2. Identify the line where the error occurs.
3. Check the variable names and data types.
4. Check brackets and semicolons.
5. Trace the values through the program.
6. Test with small inputs.
7. Use NetBeans breakpoints and step-through debugging.
Important: The line where the compiler reports an error is not always the original source of the problem. Sometimes the mistake is on an earlier line.
PART 15: IMPORTANT JAVA COMPARISONS
These comparisons are especially useful for theory questions.
15.1 Key differences to memorise
Concept 1	Concept 2	Main difference
Class	Object	Blueprint vs instance
Constructor	Method	Initialises objects vs performs tasks
==	.equals()	Compares primitive values/references vs object equality
print()	println()	No automatic new line vs new line
while	do-while	Checks first vs executes first
Overloading	Overriding	Different parameters vs redefining inherited method
extends	implements	Inherits a class vs implements an interface
Abstract class	Concrete class	Cannot be instantiated vs can be instantiated
Static	Instance	Belongs to class vs belongs to an object
break	continue	Exits loop vs skips current iteration
Array	ArrayList	Fixed size vs resizable
throw	throws	Actually throws vs declares possible exceptions

15.2 Access modifier comparison
Access modifier	Same class	Same package	Subclass outside package	Other packages
private	Yes	No	No	No
Default	Yes	Yes	No	No
protected	Yes	Yes	Yes, through inheritance access rules	No general access
public	Yes	Yes	Yes	Yes, subject to module accessibility

PART 16: IMPORTANT PROGRAMMING FORMULAS AND ALGORITHMS
These are common calculations that can appear in programming exams.
16.1 Calculate a percentage
Formula:
\[
\text{Percentage}=\frac{\text{Obtained value}}{\text{Total value}}\times100
\]

Java:
double percentage = (obtained / total) * 100;


Make sure to use decimal arithmetic:
double percentage = ((double) obtained / total) * 100;


16.2 Calculate a discount
Formula:
\[
\text{Discount}=\text{Price}\times\text{Discount rate}
\]

double price = 1000;

double discountRate = 0.10;

double discount = price * discountRate;

double finalPrice = price - discount;


Final price: R900.
16.3 Calculate VAT
Assuming a VAT rate of 15%:
double price = 100;

double vat = price * 0.15;

double total = price + vat;


Output:
VAT: 15.0
Total: 115.0


16.4 Check whether a number is even or odd
if (number % 2 == 0) {

    System.out.println("Even");

} else {

    System.out.println("Odd");

}


16.5 Calculate factorial
Factorial means multiplying a positive integer by all positive integers below it.

Example:
\[
5!=5\times4\times3\times2\times1=120
\]

Java:
int number = 5;

int factorial = 1;

for (int i = 1; i <= number; i++) {

    factorial *= i;

}

System.out.println(factorial);


Output: 120

For this simple loop implementation, use non-negative input and an integer type large enough for the result.
16.6 Generate a multiplication table
int number = 5;

for (int i = 1; i <= 12; i++) {

    System.out.println(number + " x " + i
            + " = " + (number * i));

}


16.7 Find whether a number is positive, negative or zero
if (number > 0) {

    System.out.println("Positive");

} else if (number < 0) {

    System.out.println("Negative");

} else {

    System.out.println("Zero");

}


16.8 Calculate an average from user input
Scanner input = new Scanner(System.in);

int total = 0;

for (int i = 1; i <= 5; i++) {

    System.out.print("Enter mark: ");

    int mark = input.nextInt();

    total += mark;

}

double average = total / 5.0;

System.out.println("Average: " + average);


16.9 Fibonacci sequence
The Fibonacci sequence starts with 0 and 1. Each subsequent number is the sum of the previous two.

Example:

0, 1, 1, 2, 3, 5, 8, 13

Java:
int first = 0;

int second = 1;

for (int i = 1; i <= 8; i++) {

    System.out.print(first + " ");

    int next = first + second;

    first = second;

    second = next;

}


16.10 Reverse a String
String word = "JAVA";

String reversed = "";

for (int i = word.length() - 1; i >= 0; i--) {

    reversed += word.charAt(i);

}

System.out.println(reversed);


Output: AVAJ

An alternative:
String reversed = new StringBuilder(word).reverse().toString();


16.11 Check whether a String is a palindrome
A palindrome reads the same forwards and backwards.

Examples: level, madam, racecar.
String word = "level";

String reversed = new StringBuilder(word).reverse().toString();

if (word.equalsIgnoreCase(reversed)) {

    System.out.println("Palindrome");

} else {

    System.out.println("Not a palindrome");

}


PART 17: COMPLETE JAVA PROGRAMMING EXAMPLES
This section combines several concepts. These are particularly useful because exam questions often ask you to write an entire working program rather than isolated code snippets.
Example 1: Student marks and grading system
Question: Write a Java program that accepts a student's name and three marks, calculates the average and determines whether the student has passed.
import java.util.Scanner;

public class StudentGrading {

    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);

        // Get student name
        System.out.print("Enter student name: ");

        String name = input.nextLine();

        // Get marks
        System.out.print("Enter first mark: ");

        double mark1 = input.nextDouble();

        System.out.print("Enter second mark: ");

        double mark2 = input.nextDouble();

        System.out.print("Enter third mark: ");

        double mark3 = input.nextDouble();

        // Calculate average
        double average = (mark1 + mark2 + mark3) / 3;

        // Display results
        System.out.println("Student: " + name);

        System.out.println("Average: " + average);

        // Determine result
        if (average >= 50) {

            System.out.println("Result: PASS");

        } else {

            System.out.println("Result: FAIL");

        }

        input.close();

    }
}


Concepts tested:
- Scanner input.
- Variables.
- Data types.
- Arithmetic operators.
- Conditional statements.
- Output.
Example 2: Menu-driven application
Question: Create a simple calculator using a switch statement.
import java.util.Scanner;

public class Calculator {

    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);

        System.out.println("1. Addition");

        System.out.println("2. Subtraction");

        System.out.println("3. Multiplication");

        System.out.println("4. Division");

        System.out.print("Choose an option: ");

        int choice = input.nextInt();

        System.out.print("Enter first number: ");

        double num1 = input.nextDouble();

        System.out.print("Enter second number: ");

        double num2 = input.nextDouble();

        switch (choice) {

            case 1:
                System.out.println(num1 + num2);
                break;

            case 2:
                System.out.println(num1 - num2);
                break;

            case 3:
                System.out.println(num1 * num2);
                break;

            case 4:

                if (num2 != 0) {

                    System.out.println(num1 / num2);

                } else {

                    System.out.println("Cannot divide by zero");

                }

                break;

            default:
                System.out.println("Invalid choice");

        }

        input.close();

    }
}


Example 3: Complete OOP student application
This example demonstrates classes, objects, encapsulation, constructors, getters, setters and methods.

Student.java
public class Student {

    private String name;

    private int age;

    private double mark;

    public Student(String name, int age, double mark) {

        this.name = name;

        this.age = age;

        this.mark = mark;

    }

    public String getName() {

        return name;

    }

    public void setName(String name) {

        this.name = name;

    }

    public int getAge() {

        return age;

    }

    public void setAge(int age) {

        if (age >= 0) {

            this.age = age;

        }

    }

    public double getMark() {

        return mark;

    }

    public void setMark(double mark) {

        if (mark >= 0 && mark <= 100) {

            this.mark = mark;

        }

    }

    public boolean hasPassed() {

        return mark >= 50;

    }

    @Override
    public String toString() {

        return "Student: " + name
                + ", Age: " + age
                + ", Mark: " + mark;

    }
}


Main.java
public class Main {

    public static void main(String[] args) {

        Student student1 = new Student("John", 20, 75);

        System.out.println(student1);

        if (student1.hasPassed()) {

            System.out.println("Student passed");

        } else {

            System.out.println("Student failed");

        }

    }
}


What this program demonstrates:
Concept	Where it appears
Class	Student
Object	student1
Attributes	name, age, mark
Encapsulation	private variables
Constructor	Student()
Getter	getName()
Setter	setName()
Method	hasPassed()
this keyword	this.name = name
Method overriding	toString()

Example 4: Inheritance and polymorphism
class Employee {

    protected String name;

    public Employee(String name) {

        this.name = name;

    }

    public void displayDetails() {

        System.out.println("Employee: " + name);

    }
}

class Manager extends Employee {

    private double salary;

    public Manager(String name, double salary) {

        super(name);

        this.salary = salary;

    }

    @Override
    public void displayDetails() {

        System.out.println("Manager: " + name);

        System.out.println("Salary: R" + salary);

    }
}

public class Main {

    public static void main(String[] args) {

        Employee employee = new Manager("John", 25000);

        employee.displayDetails();

    }
}


Output:
Manager: John
Salary: R25000.0


Why?
- Manager inherits from Employee.
- super(name) calls the superclass constructor.
- Manager overrides displayDetails().
- Employee employee is a superclass reference.
- The actual object is a Manager.
- Runtime polymorphism executes the Manager's method.
PART 18: JUNIT TESTING
Testing is an important part of application development. JUnit is a framework used to write and execute automated Java tests.
18.1 What is unit testing?
Unit testing involves testing individual parts of a program, such as methods, to verify that they work correctly.

Example method:
public int addNumbers(int a, int b) {

    return a + b;

}


JUnit test:
import org.junit.jupiter.api.Test;

import static org.junit.jupiter.api.Assertions.assertEquals;

public class CalculatorTest {

    @Test
    public void testAddNumbers() {

        Calculator calculator = new Calculator();

        assertEquals(15, calculator.addNumbers(10, 5));

    }
}


18.2 Important JUnit annotations
Annotation	Purpose
@Test	Marks a test method
@BeforeEach	Runs before every test
@AfterEach	Runs after every test
@BeforeAll	Runs once before all tests
@AfterAll	Runs once after all tests
@Disabled	Disables a test

18.3 Important assertion methods
Assertion	Purpose
assertEquals()	Checks whether two values are equal
assertNotEquals()	Checks whether two values differ
assertTrue()	Checks whether a condition is true
assertFalse()	Checks whether a condition is false
assertNull()	Checks whether a value is null
assertNotNull()	Checks whether a value is not null
assertThrows()	Checks whether an exception is thrown

Example:
@Test
public void testPositiveNumber() {

    int number = 10;

    assertTrue(number > 0);

}


18.4 Arrange, Act, Assert
A useful pattern for writing tests:
1. Arrange: Set up the test data.
2. Act: Execute the method being tested.
3. Assert: Check the expected result.
@Test
public void testAddition() {

    // Arrange
    Calculator calculator = new Calculator();

    // Act
    int result = calculator.addNumbers(5, 10);

    // Assert
    assertEquals(15, result);

}


Exam insight: A passing test does not prove that a program has no bugs. It shows that the tested behaviour met the expected result for the tested conditions.
PART 19: HOW TO APPROACH PROGRAMMING EXAM QUESTIONS
This is one of the most important sections in the cheat sheet.

When you see a programming question, do not immediately start typing code. Break the question down.
19.1 The five-step method
1. Step 1: Understand the question
   
   Identify what the program must do. Look for keywords such as calculate, display, compare, repeat, store, search and validate.
2. Step 2: Identify inputs
   
   Determine what information the user or program must provide.
   
   Example: Name, age, marks or price.
3. Step 3: Identify processing
   
   Determine the calculations, conditions, loops or methods required.
4. Step 4: Identify outputs
   
   Determine what the program must display or return.
5. Step 5: Test the program
   
   Check normal values, boundary values and invalid inputs.
19.2 IPO: Input, Process, Output
A very useful technique for understanding programming problems.

Example question:

A program must calculate the total price of five products.
Input	Process	Output
Five product prices	Add all prices	Total price

Example code:
double total = 0;

for (int i = 1; i <= 5; i++) {

    total += input.nextDouble();

}

System.out.println("Total: " + total);


19.3 Recognising question keywords
If the question says...	Think about...
Repeat	Loops
Until	while or do-while
Exactly five times	for loop
If / otherwise	if-else
Several fixed options	switch
Store multiple values	Array or ArrayList
Calculate total	Accumulator
Count the number of	Counter
Find highest	Maximum comparison
Find lowest	Minimum comparison
Search for	Linear search
Sort	Arrays.sort()
Create an object	Class and constructor
Reuse another class	Inheritance
Protect data	Encapsulation
Same method, different behaviour	Polymorphism
Hide implementation	Abstraction
Implement a contract	Interface
Handle an error	Exception handling
Test a method	JUnit

19.4 Accumulators vs counters
A counter counts how many times something happens.
int count = 0;

count++;


An accumulator adds values together.
int total = 0;

total += 10;


Example:
int count = 0;

int total = 0;

for (int i = 1; i <= 5; i++) {

    int number = i * 10;

    total += number;

    count++;

}

System.out.println("Count: " + count);

System.out.println("Total: " + total);


Output:
Count: 5
Total: 150


19.5 Boundary testing
Always test values at the limits of your conditions.

For example, if a student passes with 50%:
Test mark	Expected result
49	Fail
50	Pass
51	Pass
0	Fail
100	Pass

This helps identify mistakes such as:
if (mark > 50)


Instead of:
if (mark >= 50)


19.6 Understanding tracing and dry runs
A dry run means manually following the program and recording how variables change.

Example:
int total = 0;

for (int i = 1; i <= 3; i++) {

    total += i;

}


Trace table:
Iteration	i	total
Start	-	0
1	1	1
2	2	3
3	3	6

Final answer: 6.

Exam tip: If you are asked to determine the output of a program, create a trace table before writing your answer.
PART 20: JAVA QUICK-REFERENCE SYNTAX SHEET
Keep this section easy to find during your exam
This is the section to use when you know what you want to do but cannot remember the exact Java syntax.
20.1 Essential syntax
Task	Java syntax
Create integer	int x = 10;
Create decimal	double x = 10.5;
Create String	String name = "John";
Create boolean	boolean valid = true;
Display output	System.out.println(x);
Get user input	input.nextInt();
If statement	if (condition) { }
Else statement	else { }
For loop	for (int i=0; i<5; i++) { }
While loop	while (condition) { }
Do-while	do { } while (condition);
Create method	public void methodName() { }
Return value	return value;
Create array	int[] numbers = new int[5];
Create object	Student s = new Student();
Inherit class	class Dog extends Animal { }
Implement interface	class Dog implements Animal { }
Handle exception	try { } catch (Exception e) { }
Override method	@Override
Private attribute	private String name;
Constant	final int MAX = 100;

20.2 Essential imports
import java.util.Scanner;

import java.util.Arrays;

import java.util.ArrayList;

import java.util.Random;

import java.util.HashMap;

import java.io.File;

import java.io.FileWriter;

import java.io.IOException;


20.3 Commonly forgotten syntax
// String comparison
name.equals("John");

// Array length
numbers.length;

// String length
name.length();

// ArrayList size
names.size();

// Convert String to integer
int number = Integer.parseInt("123");

// Convert String to double
double price = Double.parseDouble("99.99");

// Convert integer to String
String text = String.valueOf(123);

// Generate random number 1-100
int randomNumber = (int)(Math.random() * 100) + 1;

# --Main Topics--

### [**1. Syntax**](#syntax)
### [**2. Statements**](#statements)
### [**3. Comments**](#comments)
### [**4. Data Types**](#datatype)
### [**5. Output**](#output)
### [**6. Input**](#input)
### [**7. Variables**](#variables)
### [**8. Operators**](#operators)
### **5. If/Else & Loops**
### **6. Functions and Scopes**
##

<a name = "syntax"><\a>
# Syntax
## Let's break up simple code given below
```cpp
#include <iostream>
using namespace std;

int main() {
  cout << "Hello World!";
  return 0;
}
```
1.  **#include <iostream>** ->  is a header file library that lets us work with input and output objects, such as cout (used in line 5). Header files add functionality to C++ programs.
<iostream> pronounced  "input-output stream = i o stream".
2.  **using namespace std;**->  Means that we can use names for objects and variables from the standard library.
#include and namespaces we will discuss much later in level 5, so don't worry if you don't understand them. Just remember that they always should be in your code.
3.  **int main() {}** ->  Another thing that always appear in a C++ program is int main(). This is called a function. Any code inside its curly brackets {} will be execute.
4.  **cout** ->  (pronounced "see-out") is an object used together with the insertion operator (<<) to output/print text. In our example, it will output "Hello World!".
5.  **return 0;** ->  ends the main function without errors
##                 
**Note**:  A blank line. C++ ignores white spaces. But we use it to make the code more readable.

**Note**:  After each code line type ; . Semi-column signalises to cpp that "this line is finished,now move to next step".

**Interesting feature**: The body of int main() could also been written as:**int main () { cout << "Hello World! "; return 0; }**

**Interesting feature**: You may seen codes without namespace. It can be replaced with ::, like:
```cpp
#include <iostream>
using namespace std;

int main(){
cout << "Hi";
return 0;
}
```
Can be replaces by ***hemorrhoid*** std::cout
```cpp
#include <iostream>

int main(){
std::cout << "Hi";
return 0;
}
```
<a name = "statements"><\a>
# Statements
As was mentioned above code line must end with semi-column(;), they are called ***Statements***.
Here are few statements for example:
```cpp
cout << "Happy Day";
cout << "Please Die😢";
return 0;
```
<a name = "comments"><\a>
# Comments
Comments are used in C++ in two ways: one-line-comment and text-comment
```cpp
# Comment covering only one line, out of it causes syntax error

/* ---Text-Comment
Covers text from backslash-asterikses (/*)
*/

```
## 
<a name = "datatype"><\a>
## Data Types:
```txt
Data Type-    -Size-      -Description-

--Basic--
boolean       1 byte       Stores true or false values
char          1 byte       Stores a single character/letter/number, or ASCII values
int        2 or 4 bytes    Stores whole numbers, without decimals
float         4 bytes      Stores fractional numbers, containing one or more decimals. Sufficient for storing 6-7 decimal digits
double        8 bytes      Stores fractional numbers, containing one or more decimals. Sufficient for storing 15 decimal digits
void                       The void data type represents the absence of value. We cannot create a variable of void type. It is used for pointer and functions

--Derived--
array                      List of variables that size and data type we declare 
pointer        1 byte      Pointing to register where data stores. Ex: if int x = 1, there should be smth showing location of x.
reference      1 byte      Is also some sort of pointing to location of variable
function                   result of part of code

--User Defined--
class                      * Spoilers *
structure                  * Spoilers *
union                      * Spoilers *
using                      * Spoilers *
typedef                    * Spoilers *

auto          XXXXXX       System automatically chooses correct data type for data value
```

```cpp
int myNum = 5;               // Integer (whole number)
float myFloatNum = 5.99;     // Floating point number
double myDoubleNum = 9.98;   // Floating point number
char myLetter = 'D';         // Character
bool myBoolean = true;       // Boolean
string myText = "Hello";     // String
auto Any_Thing = 53;         // After compilation declared as integer

cout << sizeof(myNum); #Show size of variable
```
<a name = "output"><\a>
# Output
As you undersand output is showing results of code to us, and to see it we use ***cout <<*** see-out
```cpp
cout << "Hello World"; #output: Hello World

# But there is one problem, when you use two "cout" they still go in one line

cout << "Hello World";
cout << "Bye World"; #output: Hello WorldBye World

# To solve it use endl(end line) or "\n" directly in text
cout << "Hello World"<< endl << "Bye World";
cout << "Hello World\nBye World";

#  Final output:
#->Hello World
#  Bye World

```
## '\n' Is called ***escape sequance***

Here are other escape sequances:
```txt
\n  - New line 
\t  - Horizontal tab
\v  - Vertical tab
\\  - Enter backslash
\b  - Backspace the text ( to remove previous letter from text )
\r  - Move the cursor to the start of the current line
\a  - Generates alert bell sound in C++
\'  - Enters single brace to text
\"  - Enters double brace to text
```
There is also one problem in C++ , in ' ' braces we can enter **only one letter**, so 'Hello' will cause an error, so use for it " " braces

## Math in C++
**cout** also works as calculator for numbers and has some arithmetical methods
```cpp
#include <cmath>

cout << 5+4-2; #output: 7
cout << max(10,4);   #output maximum value
cout << min(10,4);   #output minimum value
cout << sqrt(64);    #square root of 64
cout << round(2.6);  #round up to nearest numbe
cout << log(2);      #Logarithm with base of 2
```
## 
<a name = "input"><\a>
# Input
Input is entering data to code, and in C++ we use ***cin>>*** see-in. After entering data in cin program automaticaly creates new line, so no nedd for '\n' or endl
```cpp
cout << "Enter 1st: ";
cin >> first;
cout << "Enter 2nd;
cin >> second;
/*
Enter 1st: Ismail
Enter 2nd: Alina
*/
```
But before that we have to declare space for variables.
<a name = "variables"><\a>
## Variables
Variables are containers for storing data values.

In C++, there are different types of variables (defined with different keywords), for example:

•int - stores integers (whole numbers), without decimals, such as 123 or -123
•double - stores floating point numbers, with decimals, such as 19.99 or -19.99
•char - stores single characters, such as 'a' or 'B'. Char values are surrounded by single quotes
•string - stores text, such as "Hello World". String values are surrounded by double quotes
•bool - stores values with two states: true or false

Syntax
```txt
type variableName = value;
int Number = 1;
int Velocity = 30;
int x;
x = 50;

You also can declare variables in one line:
int Number = 1, Velocity = 30;

int x, y, z;
x=y=z=50;


The general rules for naming variables are:

• Names can contain letters, digits and underscores
• Names must begin with a letter or an underscore (_)
• Names are case-sensitive (myVar and myvar are different variables)
• Names cannot contain whitespaces or special characters like !, #, %, etc.
• Reserved words (like C++ keywords, such as int) cannot be used as names
```
You also can leave variable empty to further fill it with "cin"
```cpp
int Number;
cin >> Number; # User will enter data for Number integer type
```
If you want to make your variable unchangeable you should use ***const***
```cpp

const int abc = 4;
cin >> abc ; # Error occurs

const int Num;
Num = 2; # Error occurs
```

<a name = "operators"><\a>
# Operators
Operators are used to perform operations on variables and values
```txt

| Operator | Name           | Description                                | Example |
|    +     |Addition        | Adds together two values                   |  x + y  |
|    -     |Subtraction     | Subtracts one value from another           |  x - y  |
|    *     |Multiplication  | Multiplies two values                      |  x * y  |
|    /     |Division        | Divides one value by another               |  x / y  |
|    %     |Modulus         | Returns the division remainder             |  x % y  |
|    ++    |Increment       | Increases the value of a variable by 1     |   ++x   |
|    --    |Decrement       | Decreases the value of a variable by 1     |   --x   |
------------------------------Assignment Operators----------------------------------
|    ++    |Increment       | Increases the value of a variable by n     |   x+=5  |
|    --    |Decrement       | Decreases the value of a variable by n     |   x-=5  |
|    %=    |Modulus         | Means x = x % n, reminder of x/n           |   x%=2  |
|    *=    |Multiplication  | Means x = x / n, multiply same number to n |   x*=5  |
|    /=    |Division        | Means x = x / n, divide same number to n   |   x/=5  |
------------------Comparison(Condition) Operators-----------------------------------
|    ==    |Equality        | check if x is equal to some number         |   x==5  |
|    <=    |Less of equal   | x is less or equal                         |   x<=5  |
|    >=    |Greater or equal| x is greater or equal                      |   x>=5  |
|    !=    |Not equal       | Not equal to number                        |   x!=5  |
|    <     |Less than       | x is less or equal                         |   x< 5  |
|    >     |Greater than    | x is greater or equal                      |   x> 5  |
---------------------------------Logical Operators----------------------------------
|    &&    | Logical And    | If both conditions true, returns true               | (x>4)&&(x<10)|
|    ||    | Logical Or     | If at least one conditions true, returns true       | (x>4)||(x<10)|
|    !     | Logical Not    | REverses result, from true to false and vice verca  |    !(x> 4)   |
```
Examples
```cpp
int x = 10;
int y = 3;

cout << (x + y) << "\n"; // 13
cout << (x - y) << "\n"; // 7
cout << (x * y) << "\n"; // 30
cout << (x / y) << "\n"; // 3 (integer division removes reminders)
cout << (x % y) << "\n"; // 1

int z = 5;
++z;
cout << z << "\n"; // 6
--z;
```
cout << z << "\n"; // 5
```

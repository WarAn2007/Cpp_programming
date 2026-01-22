# Comments
Comments are used in C++ in two ways: one-line-comment and text-comment
```cpp
# Comment covering only one line, out of it causes syntax error

/* ---Text-Comment
Covers text from backslash-asterikses (/*)
*/

```
## 
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
/*
Both give same output:
Hello World
Bye World
*/
```
'\n' Is called ***escape sequance***

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
# Input
Input is entering data to code, and in C++ we use ***cin>>*** see-in. After entering data in cin program automaticaly creates new line, so no nedd for '\n' or endl
```cpp
cout << "Enter 1st: ";
cin >> fisrt;
cout << "Enter 2nd;
cin >> second;
/*
Enter 1st: Ismail
Enter 2nd: Alina
*/
```
But before that we have to declare space for variables.
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


If you declare one data type space but enter another, error will occur:
int Num = "twenty-one" # ERROR
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
## Data Types:
```txt
Data Type-    -Size-      -Description-
boolean       1 byte       Stores true or false values
char          1 byte       Stores a single character/letter/number, or ASCII values
int        2 or 4 bytes    Stores whole numbers, without decimals
float         4 bytes      Stores fractional numbers, containing one or more decimals. Sufficient for storing 6-7 decimal digits
double        8 bytes      Stores fractional numbers, containing one or more decimals. Sufficient for storing 15 decimal digits
auto          XXXXXX       System automatically chooses correct data type for data value
```

```cpp
int myNum = 5;               // Integer (whole number)
float myFloatNum = 5.99;     // Floating point number
double myDoubleNum = 9.98;   // Floating point number
char myLetter = 'D';         // Character
bool myBoolean = true;       // Boolean
string myText = "Hello";     // String

cout << sizeof(myNum); #Show size of variable
```

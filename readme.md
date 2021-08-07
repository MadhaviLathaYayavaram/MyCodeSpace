# Variables, Scopes, and Variable Shadowing in JavaScript #


## Variables ## 

Variables are used for storing different types of data which are also called ‘Values’ and input. Data can be in the form of Strings, Numbers, and /or special characters. Every data item is given a variable name according to the rules specified in JS.

Variables in Javascript can be declared in three ways using the keywords let, var, and const. Variable names are unique identifiers that are used as short names to recognize the data.


## Scope ##

The scope is a section that includes a set of instructions which we can say a compound statement grouped in curly braces { }. This region is differentiated as a block of code in JS.

The scope determines their accessibility at a particular level for variables, objects, and functions. We can assume that there are 3 types of scopes for variables in Javascript code.

*  Block Scope
*  Function Scope
*  Global Scope


## ECMAScript 6 (2015)##

The updated ECMAScript 6 version has introduced variable shadowing and block scoping through let and const declaration. Only ‘Global Scope’ and ‘Function Scope’ were existing before this version.


## Variable Shadowing in JS ##

A variable name can be declared and used inside and outside of a block. In such cases, the data assigned at the inner level is stored in the memory at the block level and can be accessed inside the block. The data assigned in the outside code of the block is stored in the memory and used outside which is called shadowing.

The variable shadowing is allowed for a variable that is declared using ‘var’ at outside of a block and can be declared as ‘let’ inside the block. But a ‘let’ variable that is created outside of a block cannot be redeclared inside the block using var, and is called “Illegal Shadowing”. But, it can be duplicated by using the ‘let’ assignment inside the block.

##nTemporal Dead Zone ##

Accessing variables before they are declared using let and const is not possible due to the TDZ and gives ‘Reference Error’.

Accessing a variable declared with ‘var’ gives a result of “Undefined”.
Accessing a variable before its declaration with ‘let’ and ‘const’ throws “reference error”.
The ‘let’ and ‘const’ variables can be hoisted/accessed before their declaration, but only in a valid scope, otherwise, it goes for a dead zone.
The temporal dead zone is also applied to function arguments.


## JavaScript Execution Context ##

Javascript engine runs two times through the code:
Creation / Compilation
Execution / Context

The creation phase allocates memory for the variables, checks for hoisting too. The Execution phase carries the “Undefined” values which were already checked by the initializer.


## Variable Scopes ##

A variable declared outside a function works as Global. And all the scripts, functions, and the whole webpage can access it. A variable that is declared inside a block cannot be used outside the block, because it has only block scope.

A variable declared within a javascript function contains ‘Local Scope’ and works only inside of the function.

Local variables/block level variables can be declared and accessed through a function. They are automatically get deleted when the function is completed.

If a value is directly assigned to a variable anywhere in the script, it automatically works as a global variable and is accessible from every part after the code execution.


## JavaScript Hoisting ##
All the variable declarations in JS are done at the top of the current scope which is called ‘Hoisting’. A variable can be declared first and can be used later. Variables can be defined with let and const and hoisted at the top of the block. The block is aware of the variable but it cannot be used until it is declared. A variable is in the “Temporal Dead Zone” from the start of the block until it is declared. Javascript hoists only variable declarations, not their initializations. Javascript interprets the variables and then executes them in the second phase.


## Strict Mode ##
The “use strict” directive was introduced in ES 5, which does not allow undeclared variables. Using and deleting a variable, a function, or an object is not possible without declaring them, in strict mode.

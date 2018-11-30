# Axolotl: The New Programming Language
Can an expressive computer language, like Lisp, be changed to be as readable as Python? I looked at what it takes for a language to become more readable and expressive. I took a readable language (Python) 
and an expressive language (Lisp) and created a language in the middle of the two, named Axolotl. Axolotl was first made as a LISP implementation,
so it would start with the power of a lisp, but alter it to be more readable, (more similar to what you would see in math class). 

Axolotl mimics the syntax of Lisp of using many parenthesis and condensing the program into a few lines. Although it did keep some syntax of Python like using an = 
sign to declare variables and was influenced by Python’s simple wording. Many of the syntax keywords (like function, 
var, etc) were modeled after the language used in math class and in calculators.

Axolotl sits firmly between Python and LISP. It has the initial readability of Python since users can easily recognize 
certain words like function, var, and mult and understand what they do. Once user’s work more with the language they will
be able to understand it easier.

My language is based off of research from Peter Norvig’s Lispy language (1) and Joel Martin’s Mal language (2), both LISP implementations. 

### The 6 program files of Axolotl:  
`Reader`: Tokenizes the AST input and evaluates them.   
`Ax_Types`: Shows how to parse values and checks what type  (list, function, symbol, etc.) the input AST is.  
`Core`: Creates Axolotl specific syntax and functions.  
`Env`: Creates the environment which holds all axolotl functions (like sum) as well as variables and functions the user will create.   
`Printer`: Prints the tokens in different ways, according to their type.   
`Script`: The main script that creates the REPL (space for the user input on the command line) and calls the other programs as input.   

### Basic Axolotl functions:  
**var**: Defines a variable, for example to set x equal to 3: `(var x 3)`  
**function**: Creates a function with parameters (or assigned variables), for example to create an addition function that adds x to y (which is equal to 4): 
`(function addition [x, y 4] (sum x y))`  
**output**: Executes multiple expressions but only returns the last one, for example in the code: `(output (var a 6) 7 (sum a 8))`, while we define var a (which would return 6) or show the number 7, it will only return a + 8 (14).   
**if**: If the parameter is true it will run the code below it, for example if we have a variable that is true, with the code: `(if true 7 8)` it will return the first output `(7)` but if it was false it would return the second output `(8)`. These outputs could also be other functions or programs.  
**func**: Creates an unnamed function (called lambda in math), for example in the code:
 `(func [a b] (sum a b)) 2 3)`, we create a function that takes an a and b and adds them together. a and b are 2 and 3, so the function will return 5. This is good for little functions that the user doesn’t want to bother naming because it will only be used once. 
 
 ### Why you should make your own Lisp implementation
 “To truly understand something, you need to teach it to somebody else. A corollary is that to truly understand Lisp, 
 you need to teach a computer how to do it.” (Martin, J. (2014). The Make-A-Lisp Process). This is a valuable tool to learn any programming language better. By 
 writing your own interpreter you understand what the computer is doing with the code you type. You can truly understand
 the language because you wrote it yourself, so you can more easily learn other concepts faster. It’s also a chance for 
 programmers to learn why languages chose the syntax they did and the impact of it on what users can do with the language. 
 It’s also an excuse to get better at whatever language you write your interpreter in. 

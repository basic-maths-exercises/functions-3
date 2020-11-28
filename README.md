# Local variables and scope

There is one final thing we need to understand about the Python functions we write; namely, the opposite of a global variable - a local variable.  

To understand this concept of local variables and the scope of a variable consider the program shown in `main.py`.  Based on what you have learned thus far you might suppose that this program would output the number 27 as it first sets `c=a+b=4+5=9`.  `d` is then set equal to `3*c`, which is `3*9=27`.  When you run the program, however, it returns the following error:

````
Traceback (most recent call last):   
  File "python", line 5, in <module> 
NameError: name 'c' is not defined  
````

This error is returned because the variable `c` is a local variable.  Python code outside of function thus cannot access the value of `c`.  We can only access the value of `c` when we are in function.

The existence of these local variables might seem irritating at first.  They are actually enormously useful, however.  The fact that variables do not exist outside of functions means we can use the same names for variables in different functions.  We are thus not required to think of lots of different names for variables.  More critically, however, as variables defined in the function cannot be accessed outside the function, the code that calls the function can essentially think of the function as a black box.  From the point of view of the calling code the only variables that matter are those that are passed to the function and those that the function returns. 

To complete this exercise, you must fix the code in `main.py`.  To do this you will need to look at the functions that you have written for the previous exercises to work out how you can ensure that the value of `c` is __returned__ to the calling code.  As discussed above, unless you return the value of `c` from the function it will be deleted from memory once the function finishes executing. 

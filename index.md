JavaScript Best Practices

1: Declarations on Top
It is a good coding practice to put all declarations at the top of each script or function.

This will:

Give cleaner code
Provide a single place to look for local variables
Make it easier to avoid unwanted (implied) global variables
Reduce the possibility of unwanted re-declarations

2: Use === Comparison
The == comparison operator always converts (to matching types) before comparison.

The === operator forces comparison of values and type:

3: Avoid global variables, avoid new, avoid ==, avoid eval()

Avoid Global Variables
Minimize the use of global variables.

This includes all data types, objects, and functions.

Global variables and functions can be overwritten by other scripts.

Use local variables instead, and learn how to use closures.

4: Always Declare Local Variables
All variables used in a function should be declared as local variables.

Local variables must be declared with the var keyword or the let keyword, otherwise they will become global variables.

5: Needed but Not More
“Good code explains itself” is an arrogant myth.

Comment what you consider needed - but don’t tell others your life story.

Avoid using the line comment //. /* */ is much safer to use because it doesn’t cause errors when the line break is removed.

If you debug using comments, there is a nice little trick: 

Comments should never go out to the end user in plain HTML or JavaScript. See Development code is not live code

6:Use Shortcut Notations
Shortcut notations keep your code snappy and easier to read once you get used to it.

7: Modularize
Keep your code modularized and specialized.

It is tempting and easy to write one function that does everything. However, as you extend the functionality you will find that you do the same things in several functions.

To prevent that, make sure to write smaller, generic helper functions that fulfill one specific task rather than catch-all methods.

At a later stage you can also expose these functions when using the revealing module pattern to create an API to extend the main functionality.

Good code should be easy to build upon without rewriting the core.

8: Enhance Progressively
Avoid creating a lot of JavaScript dependent code.

DOM generation is slow and expensive.

Elements that are dependent on JavaScript but are available when JavaScript is turned off are a broken promise to our users.

9: Recognize and remove duplicate code
Similar to our last example, you should look out for instances in your code where you have identical lines of duplicate code.

In cases like these, you should move the duplicated code into a function and call the function in all the instances that it was used before. This reduces visual clutter and aids in debugging later as the team can look at the one function rather than its multiple usage sections.

10: Use Strict Mode to catch silent errors
JavaScript is a very forgiving language compared to other hardcoded languages like C++ and Java. While helpful for getting code to run without throwing errors, this leniency can lead to silent errors that pass without correction. This can also lead to inconsistent behavior if JavaScript can resolve the silent error in multiple ways.

To bypass this, opt into Strict Mode. This setting makes two major changes:

Silent errors that would previously make it past the compiler now throw errors, allowing you to fine-tune your code before it reaches your team members.
Fixes mistakes that prevent JavaScript from optimizing your code
JavaScript Strict Code programs often run faster than their “sloppy” counterparts
To opt into strict mode, add the line'use strict'; either at the top of your script section (if you want the whole section to be strict) or before the desired function (if only certain sections should be strict).



Sources:
https://www.w3schools.com/js/js_best_practices.asp
https://www.thinkful.com/learn/javascript-best-practices-1/
https://www.educative.io/blog/javascript-tips-simplify-code
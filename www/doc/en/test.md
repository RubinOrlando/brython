Testing and debugging
---------------------

### Interactive test

The Brythons site, or its mirror available for download, include a console where you can test Python code

Please note that the namespace is not refreshed when you click on "run", you must reload the page for that

For debugging and testing Brython, a number of test scripts are grouped in the directory `tests` ; you can access them by clicking the link  "Test pages" in the console, then select the different tests and run them

### Debugging scripts

Whatever the debugging level, syntax errors are reported in the browser console (or at the place defined by `sys.stderr`)

For instance, the code

>    x = $a

generates the message

>    SyntaxError: unknown token [$]
>    module '__main__' line 1
>    x = $a
>        ^

By setting the debugging level to 1 in the call to function <code>brython(_debug\_mode_)</code>, the exceptions raised at runtime and not caught by an `except` also produce an error message, as close as possible to the one generated by Python3

This code :

>    x = [1,2]
>    x[3]

generates :

>    IndexError: list index out of range
>    module '__main__' line 2
>    x[3]
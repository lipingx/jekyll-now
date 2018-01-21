Python modules and packages

[Python modules and packages](https://docs.python.org/3/tutorial/modules.html)

# module: (*.py) A module is a file containing Python definitions and statements. 
The file name is the module name with the suffix .py appended.

As your program gets longer, you may want to split it into several files for easier maintenance. You may also want to use a handy function that you’ve written in several programs without copying its definition into each program.
Definitions from a module can be imported into other modules or into the main module.
```python
# This does not enter the names of the functions defined in module1 directly in the current symbol table; it only enters the module name module1 there
import module1
module1.func1(1000)
```

```python
# imports names from a module directly into the importing module’s symbol table.
from module1 import func1, class1
a = func1(1000)
```

```
# import all names that a module defines:
from module1 import * 
```

# package: 

In on module, use classes in different module


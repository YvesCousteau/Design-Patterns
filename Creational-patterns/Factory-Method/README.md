# Factory Method 
---
**Factory method** is a creational design pattern which solves the problem of creating product objects without specifying their concrete classes.
---
## Example 1

This example illustrates how to organize a GUI framework into independent modules using dynamic dispatch:

1. The gui module defines interfaces for all the components. It has no external dependencies.
2. The html_gui module provides HTML implementation of the base GUI. Depends on gui.
3. The windows_gui module provides Windows implementation of the base GUI. Depends on gui.

The app is a client application that can use several implementations of the GUI framework, depending on the current environment or configuration. However, most of the app code doesn’t depend on specific types of GUI elements. All client code works with GUI elements through abstract interfaces defined by the gui module.

The Abstract Factory example demonstrates an even greater separation of a factory interface and its implementations.

**Output**
```
<button>Test Button</button>
Click! Button says - 'Hello World!'
Dialog - Refresh
```

---
## Example 2

This example illustrates how to implement the Factory Method pattern using static dispatch (generics).

Inspired by the Factory Method example from the GoF book.

**Output**
```
Loading resources...
Starting the game...
Magic Room: Infinite Room
Magic Room: Red Room
Loading resources...
Starting the game...
Ordinary Room: #2
Ordinary Room: #1
```
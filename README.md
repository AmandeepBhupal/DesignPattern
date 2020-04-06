# DesignPattern

## Principles
 - S - Single Responsibility Principle
 - O - Open Close Principle + Specification
 - L - Liskov Substitution Principle
 - I - Interface Segregation Interface
 - D - Dependency Inversion Principle 


## Single Responsibility Principle

A class should focus on doing a single task rather than multiple tasks. For example, a journal class should just have functions to add, remove, and the Overridden toString() function.
If you want to implement writing to file, do it in a separate class so that if there is an error with that, the user can understand , otherwise fault isolation can be tough, as the journal would fail, and user can't figure out whether that happened in read, write to file , or while adding to arraylist of contents of file.

Basically, segregate the functions of Journal object read, add, delete and separate the responsibility of writing to file in separate class.

## Open Close Principle + Specification

Open for extension, close for modification. For example, if you have a filter and specification(as enums).
You should have an interface of spefification and then the filter should use that specifiocation, so that no matter how many specifications a user adds to the overall functionalities, he or she could use the filter code as it is.


## Liskov Substitution Principle

Fucntions that use pointers or references to base class must be able to use object of derived class without knowing it. For example, a class rectange, with a sub class square. A user should not be knowing whether to initiate a square, or a rectangle, he or she should just be invoking a standard rectangle class and there should be fucntions to detect if it is a square and do the work accordingly.

So we have a RectangleFactory class which invokes a Rectangle class object or a Square class object based on output of the isSquare method, which outputs true if width and height are the same.

## Interface Segregation Interface

The interfaces should be segregated such that an old machine and new machine use the same interfaces (those required), to implement fucntionality and the user knows depending on the machine which functions it can execute (based on implemneted interfaces).

For example, in a machine interfcae there should be implementation of printer interface, fax interface and scanner interface separately, depending on what that machine can do.

## Dependency Inversion Principle 

High level modules should not depend on low level modules. Implement this using abstraction, such that, business logic (high level) does not depend on storage implementation (low level). 
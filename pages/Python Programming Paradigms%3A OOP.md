- What is a class in Python? #card
	- A class is a blueprint for creating objects. It defines attributes and methods that its objects will have.
- What is an object in Python? #card
	- An object is an instance of a class. It has its own values for the attributes defined in the class.
- What is an attribute? #card
	- An attribute is a variable that belongs to a class or an object, describing its properties.
- What is a method? #card
	- A method is a function defined inside a class that describes the behaviors of the objects.
- How do you define a class in Python? #card
	- `class MyClass:`
- How do you create an object from a class? #card
	- `obj = MyClass()`
- What is the `__init__` method? #card
	- It is the constructor method called automatically when a new object is created, used to initialize attributes.
- How do you define the `__init__` method? #card
	- `def __init__(self, ...):`
- What does `self` mean in a class method? #card
	- `self` refers to the current instance of the class.
- How do you define a method inside a class? #card
	- `def my_method(self, ...):`
- How do you access an attribute inside a class? #card
	- `self.attribute_name`
- How do you access an attribute from outside the class? #card
	- `object.attribute_name`
- How do you create a class called `Vector` with attributes x, y, z? #card
	- ```python
	  class Vector:
	      def __init__(self, x, y, z=0):
	          self.x = x
	          self.y = y
	          self.z = z
	  ```
- How do you add two vectors using a method? #card
	- ```python
	  def sumar(self, other):
	      return Vector(self.x + other.x, self.y + other.y, self.z + other.z)
	  ```
- What is a special (dunder) method in Python? #card
	- A method that starts and ends with double underscores, like `__init__`, `__str__`, `__add__`.
- What does the `__str__` method do? #card
	- It returns a string representation of the object, used by `print()`.
- How do you overload the `+` operator in a class? #card
	- ```python
	  def __add__(self, other):
	      return Vector(self.x + other.x, self.y + other.y, self.z + other.z)
	  ```
- What is encapsulation? #card
	- Encapsulation is restricting direct access to some of an object's attributes and methods, usually to protect data.
- How do you make an attribute private in Python? #card
	- By prefixing it with double underscores, e.g., `self.__balance`.
- How do you make an attribute protected in Python? #card
	- By prefixing it with a single underscore, e.g., `self._name`.
- What is inheritance? #card
	- Inheritance allows a class (child) to inherit attributes and methods from another class (parent).
- How do you define a subclass in Python? #card
	- `class ChildClass(ParentClass):`
- How do you call the parent class constructor in a subclass? #card
	- `super().__init__(...)`
- What is polymorphism? #card
	- Polymorphism allows objects of different classes to be treated as objects of a common superclass, usually by sharing method names.
- What is abstraction? #card
	- Abstraction means hiding complex implementation details and showing only the necessary features.
- How do you define an abstract class in Python? #card
	- ```python
	  from abc import ABC, abstractmethod
	  class MyAbstractClass(ABC):
	      @abstractmethod
	      def my_method(self):
	          pass
	  ```
- What is a getter and setter? #card
	- Methods used to get and set the value of a private or protected attribute.
- How do you create a module in Python? #card
	- By saving Python code in a `.py` file and importing it with `import filename`.
- How do you create a package in Python? #card
	- By creating a folder with an `__init__.py` file and other module files inside.
- What is the principle of "composition over inheritance"? #card
	- Prefer combining simple objects (composition) rather than relying only on inheritance for code reuse.
- What is the Singleton design pattern? #card
	- Ensures a class has only one instance and provides a global point of access to it.
- What is the Factory Method pattern? #card
	- Defines an interface for creating objects, letting subclasses decide which class to instantiate.
- What is the Strategy pattern? #card
	- Defines a family of algorithms, encapsulates each one, and makes them interchangeable.
- What is the Observer pattern? #card
	- Defines a one-to-many dependency so that when one object changes state, all its dependents are notified.
- What is operator overloading in Python? #card
	- Operator overloading lets you define how standard operators (like `+`, `-`, `*`, etc.) behave when used with instances of your class.
- How do you implement operator overloading in Python? #card
	- By defining special methods (also called magic methods or dunder methods) in your class, which start and end with double underscores, like `__add__` or `__sub__`.
- What is the special method for the `+` operator? #card
	- `__add__`
- What happens when you use `+` between two instances of a class with `__add__` defined? #card
	- Python automatically calls the `__add__` method of that class.
- What is the special method for the `-` operator? #card
	- `__sub__`
- What are magic methods or dunder methods in Python? #card
	- They are special methods with names that start and end with double underscores (e.g., `__init__`, `__str__`, `__add__`), used to define specific behaviors for objects.
- What does the `dir()` function do in Python? #card
	- `dir()` returns a list of the attributes and methods of an object, class, or module. It is useful for exploring what you can do with an object.
- What does the `__len__` method do in a Python class? #card
	- It defines the behavior of the `len()` function for instances of the class.
- What does the `__getitem__` method do in a Python class? #card
	- It allows you to access elements using square brackets, like `obj[index]`.
- What does the `__setitem__` method do in a Python class? #card
	- It allows you to set the value of an element using square brackets, like `obj[index] = value`.
- What does the `__delitem__` method do in a Python class? #card
	- It allows you to delete an element using `del obj[index]`.
- What does the `__str__` method do in a Python class? #card
	- It defines the string representation of the object, used by `print()`.
- What does the `__repr__` method do in a Python class? #card
	- It defines the official string representation of the object, used by `repr()` and in the interactive shell.
- How do you make a custom list-like class in Python that supports indexing, assignment, deletion, and printing? #card
	- By implementing the methods: `__getitem__`, `__setitem__`, `__delitem__`, `__len__`, `__str__`, and `__repr__`.
- What is abstraction in object-oriented programming? #card
	- Abstraction is the ability to focus on the essential aspects of an object, ignoring irrelevant details. It allows you to represent complex concepts in a simplified way, providing a clear and concise interface to interact with objects.
- What are the benefits of abstraction in OOP? #card
	- 1. Simplicity: Reduces complexity by hiding implementation details and exposing only essential functionalities.
	- 2. Reusability: Makes code reusable by defining generic interfaces that can be implemented by different classes.
	- 3. Maintainability: Improves maintainability by separating interface from implementation, allowing changes in implementation without affecting users.
	- 4. Security: Protects internal data by providing controlled methods for interaction.
- Why is it important to organize code into modules and packages in Python? #card
	- Because it keeps the code clean, structured, and easy to maintain, and also facilitates code reuse and collaboration in large projects.
- What is a module in Python? #card
	- A module is a Python file (.py) that contains definitions of functions, classes, and variables that can be reused in other programs.
- How do you define a function in a Python module? #card
	- Using the `def` keyword, for example:  
	  `def greet(name): return f"Hello, {name}!"`
- How do you define a class in a Python module? #card
	- Using the `class` keyword, for example:  
	  `class Person: ...`
- How do you import a module in Python? #card
	- Using the `import` statement, for example:  
	  `import mymodule`
- How do you create an instance of a class defined in an imported module? #card
	- Using the syntax `module.Class()`, for example:  
	  `person = mymodule.Person("isadoji", 30)`
- What does the `__str__` method do in the `Person` class in the example? #card
	- It returns a string representation of the object, for example:  
	  `"Name: isadoji, Age: 30"`
- What is a package in Python? #card
	- A package is a collection of modules organized in a directory with a special __init__.py file. Packages allow you to organize related modules in a hierarchical structure.
- How do you structure a simple Python package? #card
	- Example structure:
	  mi_package/
	    __init__.py
	    module1.py
	    module2.py
- How do you make functions from modules available at the package level? #card
	- By importing them in the __init__.py file, e.g.:
	  from .module1 import function_module1
	  from .module2 import function_module2
- How do you import all public objects from a package in Python? #card
	- Using: from package_name import *
- How do you call a function defined in a module inside a package after importing with *? #card
	- You can call it directly by its name, e.g. function_module1()
- What does the following code do? 
  `from mi_paquete import *
  print(funcion_modulo1()) print(funcion_modulo2())` #card
	- It imports all public objects from the package mi_paquete and prints the result of calling funcion_modulo1() and funcion_modulo2().
- What is the Single Responsibility Principle (SRP) in OOP? #card
	- Each class should have only one responsibility or purpose. This means a class should have only one reason to change, making maintenance and understanding easier.
- What is the Open/Closed Principle (OCP) in OOP? #card
	- Classes should be open for extension but closed for modification. You should be able to add new functionality without modifying existing code, often achieved through inheritance and composition.
- What is the Liskov Substitution Principle (LSP) in OOP? #card
	- Subclasses should be substitutable for their base classes without altering the correctness of the program. Any instance of a subclass should be able to replace an instance of the base class without problems.
- What is the Interface Segregation Principle (ISP) in OOP? #card
	- Interfaces should be specific and focused on a limited set of functionalities. It's better to have several small, specific interfaces than a large, general one, so classes only implement what they need.
- What is the Dependency Inversion Principle (DIP) in OOP? #card
	- Classes should depend on abstractions, not on concrete implementations. Use interfaces or abstract classes to define dependencies instead of relying directly on concrete classes.
- What is encapsulation in OOP? #card
	- Encapsulation hides the internal details of classes and provides public methods to interact with them, protecting internal data from unauthorized modifications and making maintenance easier.
- What does "composition over inheritance" mean in OOP? #card
	- Composition allows you to create complex classes by combining objects from other classes, providing greater flexibility and avoiding problems associated with multiple inheritance.
- Why is it important to use design patterns in OOP? #card
	- Design patterns provide recognized solutions to common software design problems. Examples include Singleton, Factory, Observer, Strategy, and Decorator.
- Why is documentation and commenting important in OOP? #card
	- Documenting your code and providing clear comments makes it easier for others to understand and maintain the code over time.
- Why should you write unit tests for your classes and methods? #card
	- Unit tests help detect errors early and ensure that the code works correctly as
-
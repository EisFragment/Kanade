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
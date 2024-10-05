# Basic Inheritance:
Inheritance is a way to create a new class based on an existing class. The new class (child) inherits attributes and methods from the existing class (parent).

Example:
```bash
class Animal:
    def speak(self):
        print("Animal makes a sound")

class Dog(Animal):
    pass

dog = Dog()
dog.speak()  # Output: Animal makes a sound
```
## Adding New Methods:
Child classes can add their own methods in addition to inherited ones.
```bash
class Animal:
    def speak(self):
        print("Animal makes a sound")

class Dog(Animal):
    def wag_tail(self):
        print("Dog wags its tail")

dog = Dog()
dog.speak()    # Output: Animal makes a sound
dog.wag_tail() # Output: Dog wags its tail
```
## Method Overriding:
Child classes can provide their own implementation of methods inherited from the parent class.

```bash
class Animal:
    def speak(self):
        print("Animal makes a sound")

class Dog(Animal):
    def speak(self):
        print("Dog barks")

dog = Dog()
dog.speak()  # Output: Dog barks
```
## Using super():
The super() function allows you to call methods from the parent class within the child class.
```bash
class Animal:
    def __init__(self, name):
        self.name = name

class Dog(Animal):
    def __init__(self, name, breed):
        super().__init__(name)
        self.breed = breed

dog = Dog("Buddy", "Golden Retriever")
print(dog.name, dog.breed)  # Output: Buddy Golden Retriever
```
## Multiple Inheritance:
Python allows a class to inherit from multiple parent classes.

```bash
class Swimmer:
    def swim(self):
        print("Swimming")

class Flyer:
    def fly(self):
        print("Flying")

class Duck(Swimmer, Flyer):
    pass

duck = Duck()
duck.swim()  # Output: Swimming
duck.fly()   # Output: Flying
```

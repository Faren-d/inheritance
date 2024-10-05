# Basic Inheritance:
Inheritance is a way to create a new class based on an existing class. The new class (child) inherits attributes and methods from the existing class (parent).
## child, subclass, or derived class can add new attributes and methods or modify existing ones inherited from the parent, super class, or base class.
Example:
```bash
class Car(Vehicle): # Car is the derived class that inherits from Vehicle
    pass
my_car = Car("BMW", "X4", 2024) # Creating an instance of Car
my_car.display_info()
```
## Adding New Methods:
Child classes can add their own methods in addition to inherited ones.

## Method Adding and Overriding:
Child classes can provide their own implementation of methods inherited from the parent class.

```bash
class Car(Vehicle):
    def __init__(self, make, model, year, trunk_capacity):
        super().__init__(make, model, year) # Calls the __init__ of Vehicle
        self.trunk_capacity = trunk_capacity # New attribute specific to Car

    def display_car_info(self):
        print(f"{self.year} {self.make} {self.model} with trunk capacity:{self.trunk_capacity}")
    
    # Overriding an inherited method
    def diplay_info(self):
        print(f"This is a {self.year} {self.make} {self.model}.")

# Creating an instance of Car and using its methods
my_car = Car("BMW", "X6", 2025, 500)

my_car.display_car_info()
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

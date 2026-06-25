# Python Object-Oriented Programming (OOP) Fundamentals

This demonstrates the core concepts of **Classes and Objects** in Python. It provides a clear, side-by-side understanding of how to manage instance variables both with and without using the standard constructor method (`__init__`).

---

## 📖 Table of Contents
* [Overview](#overview)
* [1. Classes and Objects Without a Constructor](#1-classes-and-objects-without-a-constructor)
    * [Code Example](#code-example)
    * [How it Works](#how-it-works)
* [2. Classes and Objects With a Constructor](#2-classes-and-objects-with-a-constructor)
* [Execution and Output](#execution-and-output)

---

## 🔍 Overview

In Python, a **Class** serves as a blueprint for creating **Objects** (instances). While attributes are conventionally initialized automatically using a constructor, Python allows you to dynamically set instance variables using normal methods post-instantiation. 

This project explores these design patterns using a practical `Student` tracking example, as documented in `image_4030a5.png`.

---

## 1. Classes and Objects Without a Constructor

When a class is defined without an explicit `__init__` constructor, Python instantiates an empty object. Attributes must then be bound manually via a custom initialization method.

### Code Example

```python
class Student:
    # Custom method acting as a manual initializer
    def get_details(self, system_id, name, course, marks):
        self.system_id = system_id
        self.name = name
        self.course = course
        self.marks = marks
        
    # Method to display the initialized data
    def show_details(self):
        print(f"{self.system_id},{self.name},{self.course},{self.marks}")

# --- Object Instantiation ---

# 1. Create an empty instance of the Student class
s1 = Student()

# 2. Explicitly invoke the method to pass and bind data
s1.get_details(1, "Pavni", "BTECH", 40)

# 3. Print the results
s1.show_details()

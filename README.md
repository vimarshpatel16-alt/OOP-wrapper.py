# 👨‍💼 Employee Management System
### Python OOP Project – Inheritance Based Management System

---

## 📌 Project Overview

The **Employee Management System** is a menu-driven Python application developed using **Object-Oriented Programming (OOP)** concepts.

The project demonstrates how different classes can be connected using **inheritance**. It manages information about:

- 👤 Person
- 👨‍💼 Employee
- 👨‍💼 Manager

The program allows the user to create records and display their details through a simple interactive menu.

---

## 🎯 Objectives

The main objectives of this project are:

1. To understand the fundamentals of **Object-Oriented Programming** in Python.
2. To implement **Single Inheritance** and **Multilevel Inheritance**.
3. To understand **class and object creation**.
4. To implement **constructors** using `__init__()`.
5. To demonstrate **method overriding**.
6. To use **inheritance for code reusability**.
7. To create a simple **menu-driven application**.
8. To practice taking and processing user input.

---

## 🧠 OOP Concepts Used

This project demonstrates several important Python OOP concepts.

### 1. Class

A class is a blueprint for creating objects.

The project contains three classes:

```python
class Person:
````

```python
class Employee(Person):
```

```python
class Manager(Employee):
```

---

### 2. Object

Objects are created from classes.

Example:

```python
person = Person(name, age)
```

```python
employee = Employee(name, age, emp_id, salary)
```

```python
manager = Manager(name, age, emp_id, salary, dept)
```

---

### 3. Constructor

The `__init__()` method is used as a constructor to initialize object data.

Example:

```python
def __init__(self, name, age):
    self.name = name
    self.age = age
```

---

### 4. Inheritance

Inheritance allows one class to use the properties and methods of another class.

The inheritance structure used in this project is:

```text
             Person
                |
            Employee
                |
             Manager
```

`Employee` inherits from `Person`.

`Manager` inherits from `Employee`.

Therefore, `Manager` indirectly gets the properties and methods of `Person`.

---

### 5. Multilevel Inheritance

This project demonstrates **multilevel inheritance**:

```text
Person → Employee → Manager
```

For example:

* `Person` contains `name` and `age`.
* `Employee` adds `emp_id` and `salary`.
* `Manager` adds `department`.

---

### 6. Method Overriding

The `display()` method is defined in all three classes.

For example:

```python
def display(self):
```

Each child class provides its own version of the method and also calls the parent's `display()` method.

Example:

```python
Employee.display(self)
```

and:

```python
Person.display(self)
```

This demonstrates **method overriding**.

---

### 7. Encapsulation

The data of each object is stored inside the object using instance variables such as:

```python
self.name
self.age
self.emp_id
self.salary
self.department
```

This keeps the data associated with its respective object.

---

## 🏗️ Class Structure

### 👤 Person Class

The `Person` class is the base class.

It stores:

* Name
* Age

It contains:

```python
display()
```

which displays the person's information.

---

### 👨‍💼 Employee Class

The `Employee` class inherits from `Person`.

It stores:

* Name
* Age
* Employee ID
* Salary

It reuses the `Person` class constructor and display method.

---

### 👨‍💼 Manager Class

The `Manager` class inherits from `Employee`.

It stores:

* Name
* Age
* Employee ID
* Salary
* Department

It also reuses the functionality of the parent classes.

---

## 🔄 Program Flow

The program works through a menu-driven system.

```text
                START
                  |
                  ↓
          Display Main Menu
                  |
        ┌─────────┼─────────┐
        ↓         ↓         ↓
      Person   Employee   Manager
        |         |         |
        └─────────┼─────────┘
                  ↓
            Show Details
                  |
                  ↓
             Continue?
              /       \
            Yes        No
             |          |
             ↓          ↓
          Main Menu    EXIT
```

---

## 📋 Main Menu

When the program starts, the following menu is displayed:

```text
--- Python OOP Project: Employee Management System ---

Choose an operation:

1. Create a Person
2. Create an Employee
3. Create a Manager
4. Show Details
5. Exit
```

---

## ⚙️ Features

### 1️⃣ Create a Person

The user can create a Person by entering:

```text
Name
Age
```

Example:

```text
Enter your choice: 1
Enter name: Rahul
Enter age: 25
```

---

### 2️⃣ Create an Employee

The user can create an Employee by entering:

```text
Name
Age
Employee ID
Salary
```

Example:

```text
Enter your choice: 2
Enter name: Rahul
Enter age: 25
Enter employee id: E101
Enter salary: 35000
```

---

### 3️⃣ Create a Manager

The user can create a Manager by entering:

```text
Name
Age
Employee ID
Salary
Department
```

Example:

```text
Enter your choice: 3
Enter name: Amit
Enter age: 35
Enter employee id: M101
Enter salary: 65000
Enter department: IT
```

---

### 4️⃣ Show Details

The user can select which object's information should be displayed.

```text
1. Person
2. Employee
3. Manager
```

The program checks whether data exists before displaying it.

If no data has been created, it displays:

```text
No data available
```

---

### 5️⃣ Exit

The user can exit the program by selecting:

```text
5. Exit
```

The program displays:

```text
Exiting the system. All resources have been freed.

Goodbye!
```

---

## 💻 Technologies Used

| Technology        | Purpose                        |
| ----------------- | ------------------------------ |
| Python            | Programming Language           |
| OOP               | Program Structure              |
| Classes           | Data and behavior organization |
| Inheritance       | Code reusability               |
| Constructors      | Object initialization          |
| Method Overriding | Polymorphism concept           |
| `while` loop      | Menu repetition                |
| `if-elif-else`    | Decision making                |
| `input()`         | User input                     |

---

## 🛠️ Requirements

To run this project, you need:

* Python 3.x
* Any Python IDE or code editor

Recommended IDEs:

* VS Code
* PyCharm
* IDLE
* Jupyter Notebook
* Python Online Compiler

No external libraries are required.

---

## ▶️ How to Run the Project

### Step 1: Install Python

Install Python 3.x on your computer.

Check the installation using:

```bash
python --version
```

---

### Step 2: Save the Program

Save the Python program as:

```text
employee_management.py
```

---

### Step 3: Open Terminal

Navigate to the folder containing the Python file.

---

### Step 4: Run the Program

Use:

```bash
python employee_management.py
```

---

## 🧪 Sample Output

```text
--- Python OOP Project: Employee Management System ---

Choose an operation:

1. Create a Person
2. Create an Employee
3. Create a Manager
4. Show Details
5. Exit

Enter your choice: 3

Enter name: Amit
Enter age: 35
Enter employee id: M101
Enter salary: 65000
Enter department: IT

Manager created with name: Amit and age: 35 id: M101 salary: 65000.0 department: IT

--- Choose another operation ---

Choose an operation:

1. Create a Person
2. Create an Employee
3. Create a Manager
4. Show Details
5. Exit

Enter your choice: 4

1. Person
2. Employee
3. Manager

Show which one: 3

Name: Amit
Age: 35
Employee ID: M101
Salary: 65000.0
Department: IT
```

---

## 📊 Example of Inheritance

### Person

```text
Name
Age
```

↓

### Employee

```text
Name
Age
Employee ID
Salary
```

↓

### Manager

```text
Name
Age
Employee ID
Salary
Department
```

This shows how each child class extends the functionality of its parent class.

---

## 🔍 Important Code Explanation

### Creating a Person

```python
person = Person(name, age)
```

This creates an object of the `Person` class.

---

### Creating an Employee

```python
employee = Employee(name, age, emp_id, salary)
```

This creates an Employee object.

The Employee constructor first initializes the Person attributes:

```python
Person.__init__(self, name, age)
```

and then initializes:

```python
self.emp_id = emp_id
self.salary = salary
```

---

### Creating a Manager

```python
manager = Manager(name, age, emp_id, salary, dept)
```

The Manager constructor calls:

```python
Employee.__init__(self, name, age, emp_id, salary)
```

and then adds:

```python
self.department = department
```

---

## 🛡️ Error Handling

The program checks whether an object has been created before displaying its information.

For example:

```python
if opt == "1" and person is not None:
```

If no object exists, the program displays:

```text
No data available
```

This prevents the program from trying to display information from an empty variable.

---

## 🌟 Advantages of the Project

* Easy to understand
* Simple menu-driven interface
* Demonstrates OOP concepts clearly
* Uses inheritance effectively
* Avoids unnecessary code duplication
* Easy to modify and expand
* Beginner-friendly
* Does not require external libraries

---

## 🚀 Possible Future Improvements

The current project can be expanded by adding:

1. Multiple employee records
2. Delete employee functionality
3. Update employee information
4. Search employee by ID
5. Search employee by name
6. Store data in a file
7. Database connectivity
8. Login and authentication
9. Salary calculation
10. Department-wise employee listing
11. Exception handling for invalid input
12. Graphical User Interface (GUI)

---

## 📁 Project Structure

```text
Employee-Management-System/
│
├── employee_management.py
│
└── README.md
```

---

## 🎓 Learning Outcomes

After completing this project, I learned:

* How to create classes and objects in Python.
* How constructors work.
* How inheritance can be implemented.
* How multilevel inheritance works.
* How methods can be overridden.
* How to reuse parent class functionality.
* How to create a menu-driven application.
* How to validate whether object data exists.
* How OOP can be used to model real-world entities.

---

## 📌 Conclusion

The **Employee Management System** is a simple Python-based OOP project that demonstrates the practical implementation of classes, objects, constructors, inheritance, multilevel inheritance, and method overriding.

The project provides a strong understanding of how Object-Oriented Programming can be used to organize and manage related data efficiently.

It can also be extended into a complete employee management application by adding databases, file handling, search, update, delete, and GUI features.

---

## 👨‍💻 Author

**Name:** __________________________

**Course/Class:** ___________________

**Subject:** Python / Object-Oriented Programming

**Project:** Employee Management System

**Academic Year:** 2026–2027

---

## ⭐ Project Highlights

```text
✔ Python OOP
✔ Classes & Objects
✔ Constructors
✔ Inheritance
✔ Multilevel Inheritance
✔ Method Overriding
✔ Encapsulation
✔ Menu-Driven Program
✔ User Input
✔ Data Validation
✔ Beginner Friendly
```

---

## 📜 License

This project is created for **educational and academic purposes**.

You are free to study, modify, and improve the project for learning purposes.

---

# 🙏 Thank You

### Thank you for reviewing my Python OOP project!

````

### ⭐ For a 10/10 presentation

I recommend adding these **3 things to your project folder**:

```text
Employee-Management-System/
│
├── employee_management.py
├── README.md
└── screenshots/
    ├── main_menu.png
    ├── employee_created.png
    └── manager_details.png
````

This makes your submission look much more like a **complete academic project**, rather than just a Python program.


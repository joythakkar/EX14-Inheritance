# EX14-Inheritance

# Aim

To study and implement different types and modes of inheritance in C++ through practical examples and visual representations.
# Objectives

    To grasp the fundamental concept of inheritance in Object-Oriented Programming.

    To distinguish between various modes of inheritance: public, private, and protected.

    To implement different types of inheritance: single, multiple, multilevel, and hierarchical.

    To examine real-world applications of inheritance in software development.

    To understand how base class members are inherited under different access modes.

# Tools and Environment

    Programming Language: C++

    Compiler: g++ or any standard C++ compiler

    Development Platforms: Code::Blocks, Visual Studio Code, Turbo C++, or OnlineGDB

# Theoretical Background
## Understanding Inheritance

Inheritance stands as a cornerstone of Object-Oriented Programming (OOP), enabling a derived class to inherit properties and behaviors from a base class. This mechanism offers several advantages:

    Enhances code reusability by allowing derived classes to utilize existing code

    Supports extensibility through adding new features without modifying existing code

    Models real-world relationships through IS-A relationships

## Practical Examples:

    A Car is a type of Vehicle → Car inherits Vehicle's properties

    A Student is a type of Person → Student inherits Person's attributes

## Modes of Inheritance

C++ provides three distinct modes of inheritance that determine how base class members are accessible in derived classes:

  ## Public Inheritance

        Base class public members become public in derived class

        Base class protected members remain protected

        Base class private members are not accessible

        Application: Most commonly used; maintains the base class interface

   ## Protected Inheritance

        Base class public and protected members become protected in derived class

        Base class private members remain not accessible

        Application: Useful when hiding base class interface while allowing derived classes access

  ## Private Inheritance

        Base class public and protected members become private in derived class

        Base class private members remain not accessible

        Application: Implements functionality using base class without exposing its interface

## Comparison of Inheritance Modes
Mode	Base Class Member Accessibility	External Visibility	Key Characteristics
Public	Public→Public, Protected→Protected	Private: Not inherited	Preserves base class interface
Protected	Public→Protected, Protected→Protected	Private: Not inherited	Base interface becomes protected
Private	Public→Private, Protected→Private	Private: Not inherited	Hides base class interface
Types of Inheritance

   ## Single Inheritance

        One derived class inherits from one base class

        Example: Vehicle → Car

  ## Multiple Inheritance

        One derived class inherits from multiple base classes

        Example: Student inherits from PersonalInfo and AcademicInfo

  ## Multilevel Inheritance

        Derived class becomes base for another class (chain inheritance)

        Example: Vehicle → Car → ElectricCar

  ## Hierarchical Inheritance

        Multiple derived classes inherit from a single base class

        Example: Animal → Dog, Cat, Horse

## Comparison of Inheritance Types
Characteristic	Single	Multiple	Multilevel	Hierarchical
Relationship	One-to-one	Many-to-one	Chain inheritance	One-to-many
Complexity	Low	High (ambiguity)	Moderate	Moderate
Reusability	Basic	High	Stepwise	Broad
Ambiguity Risk	None	Diamond problem	Minimal	None
Use Case	Simple extension	Feature combination	Progressive specialization	Common base with variations
Visual Representations
Modes of Inheritance
Public Inheritance
text

+----------------+
|   Base Class   |
| (public, prot.)|
+----------------+
        |
        v (public inheritance)
+----------------+
| Derived Class  |
| public→public  |
| protected→prot.|
+----------------+
        |
        v
+----------------+
|   External     |
| Public access  |
+----------------+

Private Inheritance
text

+----------------+
|   Base Class   |
| (public, prot.)|
+----------------+
        |
        v (private inheritance)
+----------------+
| Derived Class  |
| public→private |
| protected→priv.|
+----------------+
        |
        v
+----------------+
|   External     |
| No access      |
+----------------+

Protected Inheritance
text

+----------------+
|   Base Class   |
| (public, prot.)|
+----------------+
        |
        v (protected inheritance)
+----------------+
| Derived Class  |
| public→prot.   |
| protected→prot.|
+----------------+
        |
        v
+----------------+
|   External     |
| No access      |
+----------------+

Types of Inheritance
Single Inheritance
text

+----------------+
|   Base Class   |
+----------------+
        |
        v
+----------------+
| Derived Class  |
+----------------+

Multiple Inheritance
text

+----------------+    +----------------+
|  Base Class A  |    |  Base Class B  |
+----------------+    +----------------+
          \             /
           \           /
            v         v
           +----------------+
           | Derived Class  |
           +----------------+

Multilevel Inheritance
text

+----------------+
|   Base Class   |
+----------------+
        |
        v
+----------------+
| Intermediate   |
| Derived Class  |
+----------------+
        |
        v
+----------------+
| Final Derived  |
|    Class       |
+----------------+

Hierarchical Inheritance
text

         +----------------+
         |   Base Class   |
         +----------------+
           /      |      \
          /       |       \
         v        v        v
+----------+ +----------+ +----------+
| Derived1 | | Derived2 | | Derived3 |
+----------+ +----------+ +----------+

Practical Applications
Real-World Applications of Inheritance

    Transportation Systems: Base class Vehicle with derived classes Car, Bike, Bus

    Corporate Structures: Base class Employee with derived classes Manager, Developer, Tester

    Banking Solutions: Base class Account with derived classes SavingsAccount, CurrentAccount

    Educational Systems: Base class Person with derived classes Student, Teacher

Real-World Applications of Inheritance Modes

    Public Inheritance: Car inheriting Vehicle publicly to access properties like speed and fuel externally

    Protected Inheritance: TeachingAssistant inheriting Teacher with protected access for internal use

    Private Inheritance: SecureDatabase inheriting Database privately to reuse methods without external exposure

Real-World Applications of Inheritance Types

    Single Inheritance: Car inheriting from Vehicle (direct relationship)

    Multiple Inheritance: Smartphone inheriting from Camera and Phone (feature combination)

    Multilevel Inheritance: SportsCar inheriting from Car, which inherits from Vehicle (progressive specialization)

    Hierarchical Inheritance: Car, Bike, Bus inheriting from Vehicle (common base with variations)

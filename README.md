# Experiment-14

### 1. Hierarchical Inheritance

#### Theory:
Hierarchical inheritance occurs when multiple subclasses inherit from a single superclass. This structure allows for shared attributes and methods in the base class, while enabling the derived classes to implement or extend functionality specific to themselves. Hierarchical inheritance promotes code reusability and organizes code in a logical manner.

#### Algorithm:
1. Define a base class (e.g., `Animal`).
2. Define multiple derived classes (e.g., `Dog`, `Cat`) that inherit from the base class.
3. Implement methods in the base class.
4. Override or add specific methods in the derived classes.
5. Create objects of the derived classes to demonstrate functionality.

#### Example Code:
```cpp
#include <iostream>
using namespace std;

class Animal {
public:
    void sound() {
        cout << "Animal makes a sound" << endl;
    }
};

class Dog : public Animal {
public:
    void sound() {
        cout << "Dog barks" << endl;
    }
};

class Cat : public Animal {
public:
    void sound() {
        cout << "Cat meows" << endl;
    }
};

int main() {
    Dog dog;
    Cat cat;

    dog.sound(); // Dog barks
    cat.sound(); // Cat meows

    return 0;
}
```

### Conclusion:
Hierarchical inheritance simplifies the management of classes by promoting reusability and a clear structure. It is beneficial in scenarios where multiple entities share common characteristics.

---

### 2. Multiple Inheritance

#### Theory:
Multiple inheritance allows a class to inherit features from more than one base class. This can lead to complex relationships but provides flexibility in using functionalities from various classes. It can help combine features from different sources but can also lead to ambiguity if not handled properly.

#### Algorithm:
1. Define multiple base classes (e.g., `Vehicle`, `Engine`).
2. Create a derived class (e.g., `Car`) that inherits from both base classes.
3. Implement methods in the base classes.
4. Create an instance of the derived class to demonstrate combined functionality.

#### Example Code:
```cpp
#include <iostream>
using namespace std;

class Vehicle {
public:
    void start() {
        cout << "Vehicle starts" << endl;
    }
};

class Engine {
public:
    void rev() {
        cout << "Engine revs" << endl;
    }
};

class Car : public Vehicle, public Engine {
public:
    void drive() {
        cout << "Car is driving" << endl;
    }
};

int main() {
    Car car;
    car.start(); // Vehicle starts
    car.rev();   // Engine revs
    car.drive(); // Car is driving

    return 0;
}
```

### Conclusion:
Multiple inheritance can enhance functionality by allowing a derived class to access features from multiple sources. However, care must be taken to manage potential ambiguities and ensure clarity in code design.

---

### 3. Multilevel Inheritance

#### Theory:
Multilevel inheritance is a type of inheritance where a class is derived from another derived class, forming a chain of inheritance. This allows for extending the properties and methods of base classes through multiple layers, providing a structured and hierarchical way to organize code.

#### Algorithm:
1. Define a base class (e.g., `Animal`).
2. Create a derived class (e.g., `Dog`) that inherits from the base class.
3. Create another derived class (e.g., `Puppy`) that inherits from the second derived class.
4. Implement methods in the base classes.
5. Create an instance of the last derived class to demonstrate functionality.

#### Example Code:
```cpp
#include <iostream>
using namespace std;

class Animal {
public:
    void eat() {
        cout << "Animal eats" << endl;
    }
};

class Dog : public Animal {
public:
    void bark() {
        cout << "Dog barks" << endl;
    }
};

class Puppy : public Dog {
public:
    void weep() {
        cout << "Puppy weeps" << endl;
    }
};

int main() {
    Puppy puppy;
    puppy.eat(); // Animal eats
    puppy.bark(); // Dog barks
    puppy.weep(); // Puppy weeps

    return 0;
}
```

### Conclusion:
Multilevel inheritance effectively models relationships in hierarchical structures. It promotes code reusability and a clearer organization of functionalities across related classes, making it easier to maintain and extend.

### Single Inheritance

#### Theory:
Single inheritance is a type of inheritance in object-oriented programming where a class (known as a derived class or child class) inherits from only one base class (parent class). This relationship forms a simple hierarchy, allowing the derived class to access the properties and methods of the base class. Single inheritance promotes code reuse and simplifies class relationships.

#### Key Points:
- **Simplicity**: Since there’s only one parent class, the relationship is straightforward, making the code easier to understand and maintain.
- **Reusability**: The derived class can reuse the functionality of the base class, reducing code duplication.
- **Clear Structure**: It creates a clear parent-child relationship between classes.

#### Algorithm:
1. Define a base class (e.g., `Animal`).
2. Create a derived class (e.g., `Dog`) that inherits from the base class.
3. Implement methods in the base class.
4. Create an instance of the derived class to demonstrate access to base class methods.

#### Example Code:
```cpp
#include <iostream>
using namespace std;

// Base class
class Animal {
public:
    void eat() {
        cout << "Animal eats" << endl;
    }
};

// Derived class
class Dog : public Animal {
public:
    void bark() {
        cout << "Dog barks" << endl;
    }
};

int main() {
    Dog dog;

    // Accessing methods from the base class
    dog.eat(); // Animal eats

    // Accessing method from the derived class
    dog.bark(); // Dog barks

    return 0;
}
```

### Conclusion:
Single inheritance is a fundamental concept in object-oriented programming that allows a derived class to inherit attributes and behaviors from a single base class. This leads to simpler class structures and promotes reusability of code, making it easier to manage and extend applications. Single inheritance is particularly useful when there is a clear "is-a" relationship between the classes.

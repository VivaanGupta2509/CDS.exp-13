# Experiment - 13
# Constructor Overloading

## Aim - 
To study and implement constructor overloading.

## Theory - 
Constructors are special class functions automatically called when an object is created. 
Constructor overloading occurs when a class has multiple constructors with the same name but different parameter lists. 
Each must have a unique set of arguments, distinguished by the number and type of parameters.

### Key Concepts about constructor overloading :

1. **Multiple Constructors**: 
   In constructor overloading, each constructor has a unique signature determined by the number and types of parameters. This lets developers initialize objects in different ways depending on the situation.

2. **No Return Type**:
   Constructors do not have a return type (not even `void`), as their primary function is to initialize an object. Once the constructor is called, the object gets initialized.

3. **Default Constructor**:
   A constructor without parameters, known as the **default constructor**, initializes an object with default values. If no constructors are defined in a class, the compiler provides a default constructor.

4. **Parameterized Constructor**:
   This constructor accepts parameters, allowing the object to be initialized with specific values during creation.

5. **Copy Constructor**:
   A copy constructor takes a reference to another object of the same class and creates a new object as a copy of the existing one.

## Code - 
```
#include <iostream>
using namespace std;

class Room {
private:
    double length;
    double breadth;

public:
    
    Room() {
        length = 9;
        breadth = 7;
    }

    
    Room(double l, double b) {
        length = l;
        breadth = b;
    }

    
    Room(double len) {
        length = len;
        breadth = 8.1;
    }

    double calculateArea() {
        return length * breadth;
    }
};

int main() {
    Room r1;
    Room r2(8.6, 6.9);
    Room r3(9, 9);
       
    cout << "Area of r1: " << r1.calculateArea() << endl;
    cout << "Area of r2: " << r2.calculateArea() << endl;
    cout << "Area of r3: " << r3.calculateArea() << endl;

    return 0;
}
```

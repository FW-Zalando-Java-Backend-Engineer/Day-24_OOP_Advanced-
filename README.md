# **📘 Day-24: Advanced OOP – Inheritance, Abstract Classes & Polymorphism**

Welcome to **Day-24** of our Java backend adventure! Today, we unlocked some of the **most powerful tools** in object-oriented programming – **Inheritance**, **Abstract Classes**, and **Polymorphism**. These concepts enable **code reuse**, **flexibility**, and **extensibility** – the foundations of scalable Java applications.

> TL;DR – You now know how to make Java code feel more like magic (but still way more structured than PHP 😄).

---

## **📌 Lesson Structure**

### **1️⃣ Inheritance: Code Reuse Made Easy**

* Allows a class to **inherit fields and methods** from another class.
* Promotes **DRY** (Don’t Repeat Yourself) principles.
* Enables **hierarchical design**.

---

### **🧬 Example: Base and Subclass**

```java
public class Vehicle {
    String brand = "Generic";
    void honk() {
        System.out.println("Beep beep!");
    }
}

public class Car extends Vehicle {
    int doors = 4;
}
```

```java
Car myCar = new Car();
myCar.honk();          // Inherited from Vehicle
System.out.println(myCar.brand);  // Inherited field
```

---

## **📚 Abstract Classes: Forcing Structure**

### 🔹 Why Use Abstract Classes?

* Can’t be instantiated – they act as **blueprints**.
* Can define **abstract methods** (no implementation).
* Can also have **implemented methods** and fields.

---

### **📌 Abstract Class Example**

```java
public abstract class Animal {
    abstract void makeSound();  // Must be implemented
    void sleep() {
        System.out.println("Zzz...");
    }
}

public class Dog extends Animal {
    void makeSound() {
        System.out.println("Woof!");
    }
}
```

```java
Animal pet = new Dog();
pet.makeSound();  // Woof!
pet.sleep();      // Zzz...
```

> 🔥 Abstract classes enforce contracts while allowing partial implementation.

---

## **🌀 Polymorphism: One Interface, Many Forms**

* Objects of different classes can be **treated as objects of a common superclass**.
* Actual method called depends on the **runtime object** – not the reference type.
* Achieved through **method overriding**.

---

### **📌 Polymorphism in Action**

```java
public class Animal {
    void makeSound() {
        System.out.println("Some sound");
    }
}

public class Cat extends Animal {
    void makeSound() {
        System.out.println("Meow");
    }
}

public class Cow extends Animal {
    void makeSound() {
        System.out.println("Moo");
    }
}
```

```java
Animal a1 = new Cat();
Animal a2 = new Cow();

a1.makeSound();  // Meow
a2.makeSound();  // Moo
```

> 🧠 **Runtime polymorphism** is what powers Java frameworks like Spring.

---

## **🧠 Key Concepts Recap**

| Concept               | Summary                                                             |
| --------------------- | ------------------------------------------------------------------- |
| **Inheritance**       | Subclass inherits from superclass; enables code reuse               |
| **Abstract Class**    | Cannot be instantiated; used to enforce a base contract or skeleton |
| **Polymorphism**      | Same interface, different behavior depending on object type         |
| **Method Overriding** | Redefine superclass method in subclass                              |

---

## **🎮 Practice Challenges**

✅ Create a base class `Employee` with `calculateSalary()` as an abstract method.

✅ Subclass `Developer`, `Manager`, and implement custom salary logic.

✅ Use a `List<Employee>` to store and call `calculateSalary()` polymorphically.

✅ Add a shared concrete method in `Employee` like `displayInfo()`.

---

## **🧪 Demo Exercise**

Check out this hands-on demo exercise to reinforce what you've learned today:

🔗 [OOP-Demo-in-Java – GitHub Repository](https://github.com/FW-Zalando-Java-Backend-Engineer/OOP-Demo-in-Java)

Clone it, run it, modify it, break it – it's yours to explore!

---

## **📚 Additional Resources**

* [Baeldung – Inheritance in Java](https://www.baeldung.com/java-inheritance)
* [Oracle Docs – Abstract Classes](https://docs.oracle.com/javase/tutorial/java/IandI/abstract.html)
* [GeeksForGeeks – Polymorphism](https://www.geeksforgeeks.org/polymorphism-in-java/)
* [Java Method Overriding](https://www.programiz.com/java-programming/method-overriding)

---

## **🎥 Video Lesson Recording**

📺 [*Watch the Session*](https://us06web.zoom.us/rec/share/gYZYQuuiX_yVMji6bhDdlcxaLJJMS2GwiLy_4o7H9e1w8HRHmXW5zHuVcQaADJ1E.S3MCdNe3KAaZGNsz?startTime=1744874658000)

---

🚀 **Phenomenal progress today! With inheritance and polymorphism under your belt, you're stepping into real backend engineering territory. Get ready – interfaces and design patterns are up next. (And yes, they’re cooler than PHP's attempt at OOP 😉)**

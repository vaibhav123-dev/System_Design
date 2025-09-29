# 📘 System Design

**System Design** is the process of defining the **architecture, components, modules, interfaces, and data flow** of a system to meet specific requirements.  

It focuses on **how to build a system that is scalable, reliable, maintainable, and efficient**, rather than just coding features.  

> ✅ Think of system design as the **blueprint** for building and organizing software to handle **real-world scale and requirements**.

---

## 🔑 Key Aspects of System Design

### 1. Requirement Analysis
- **Functional Requirements** → What the system should do (features, workflows).  
- **Non-Functional Requirements** → How the system should perform:
  - Scalability
  - Reliability
  - Performance
  - Security
  - Availability  

---

### 2. High-Level Design (HLD)
- Focuses on **big-picture architecture**.  
- Defines **major components** and their interactions.  

**Example (Food Delivery App):**
- User Service  
- Order Service  
- Payment Service  
- Delivery Service  

---

### 3. Low-Level Design (LLD)
- Focuses on **detailed design** of each module/class.  
- Includes **database schema, API contracts, algorithms**.  

**Example (Order Service):**
- Entities:
  - `Order`  
  - `Item`  
  - `Payment`  

---

### 4. System Characteristics
- **Scalability** → Handle growth in users and requests.  
- **Reliability & Availability** → Ensure uptime and fault tolerance.  
- **Performance** → Optimize response time and resource usage.  
- **Maintainability & Extensibility** → Easy to fix bugs and add features.  
- **Security** → Protect against vulnerabilities and threats.  

---

### 5. Technology Choices
- **Databases** → SQL (structured data) vs NoSQL (flexible schema).  
- **Caching** → Redis, Memcached (for speed).  
- **Message Queues** → Kafka, RabbitMQ (for async processing).  
- **Infrastructure** → Load balancers, CDNs, microservices, containerization (Docker/Kubernetes).  

---

# 📘 Low Level Design

### Defination: 
- LLD involves detailing the system's components, their relationships, and interactions.
- It is the blueprint for developers to write code.
### Focus: 
- Classes, methods, data structures, algorithms, and their interactions
### Objective:
- Classes, methods, data structures, algorithms, and their interactions

## 🔑 Key Design Principles 

#### 1. Solid Principles 
#### 2. DRY (Don’t repeat yourself) 
#### 3. KISS (Keep it simple, stupid) 
#### 4. YAGNI (You aren’t gonna need it) 
#### 5. Composition over Inheritance 
#### 6. Encapsulate what changes

---

# 📘 Introduction to Class & Object in Node.js

## 🔹 Class
A **class** is a **blueprint** for creating objects.  
It defines:  
- **Properties (fields)** → Represent the state.  
- **Behaviors (methods)** → Represent the actions.  

---

## 🔹 Object
An **object** is an **instance of a class**.  
It:  
- Holds **state** (fields).  
- Provides **behavior** (methods).  

---

## 🛠 How Objects are Created in Node.js?

1. **Using Object Literals**
   ```javascript
   const user = {
     name: "Alice",
     age: 25,
     greet: function() {
       console.log(`Hello, my name is ${this.name}`);
     }
   };
   
   user.greet(); // Output: Hello, my name is Alice

1. **Using Constructor Function**
   ```javascript
   function User(name, age) {
    this.name = name;
    this.age = age;
    this.greet = function() {
      console.log(`Hello, my name is ${this.name}`);
    };
    }
   
    const user1 = new User("Bob", 30);
    user1.greet(); // Output: Hello, my name is Bob

1. **Using Class**
   ```javascript
   class User {
    constructor(name, age) {
      this.name = name;
      this.age = age;
    }
  
    greet() {
      console.log(`Hello, my name is ${this.name}`);
    }
    }
    
    const user2 = new User("Charlie", 28);
    user2.greet(); // Output: Hello, my name is Charlie


# 📘 Constructors in Node.js

## 🔹 What is a Constructor?
A **constructor** is a special function used to **initialize objects** in Node.js.  

- It is **called automatically** when an object of a class is created.  
- It sets the **initial state** of an object by assigning values to its attributes.  

---

## 🔹 Types of Constructors

1. **Constructor Functions**
- In JavaScript/Node.js, you can use a **regular function** as a constructor with the `new` keyword.

   ```javascript
   function User(name, age) {
    this.name = name;
    this.age = age;
    this.greet = function() {
      console.log(`Hello, my name is ${this.name}`);
    };
    }
    
    const user1 = new User("Alice", 25);
    user1.greet(); // Output: Hello, my name is Alice
   
1. **ES6 Class-based Constructors**
- With ES6, JavaScript introduced the class syntax which includes a built-in constructor method.
   ```javascript
   class User {
      constructor(name, age) {
        this.name = name;
        this.age = age;
      }
    
      greet() {
        console.log(`Hello, my name is ${this.name}`);
      }
    }
    
    const user2 = new User("Bob", 30);
    user2.greet(); // Output: Hello, my name is Bob
---

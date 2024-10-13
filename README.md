Object-Oriented Programming (OOP) is a way of organizing code around "objects." These objects represent real-world things and have:

1. **Properties** (data) – like characteristics of the object.
2. **Methods** (actions) – things the object can do.

OOP makes code easier to manage, reuse, and understand. The main ideas are:

- **Encapsulation**: Keeping data and actions together.
- **Inheritance**: Sharing features between objects.
- **Polymorphism**: Using different objects in the same way.
- **Abstraction**: Hiding unnecessary details from the user.

# Why use oops

- **Code Reusability**: OOP allows you to reuse existing code through inheritance, saving time and reducing redundancy.
- **Modularity**: Breaking down complex problems into smaller objects makes code more organized and easier to manage.
- **Maintainability**: Changes to one part of the program (object) don’t affect other parts, making it easier to update and fix.
- **Scalability**: OOP makes it easier to expand or modify programs as they grow by adding new objects or features.
- **Data Security**: Encapsulation protects data by keeping it private within objects, improving security and preventing unauthorized access.
- **Real-World Mapping**: OOP closely models real-world entities, making code more intuitive to understand and work with.

## 1. Constructer Functions

Why Use a Constructor Function?

A **constructor function** is a special type of function in JavaScript that helps us create **multiple objects** with the same structure, without writing repetitive code for each object. In your example, the constructor function is used to create **bank account objects** with specific properties like the customer's name, account number, and balance.

Let's break it down with simple steps and why constructors are helpful.

### The Problem Without a Constructor:

Imagine you need to create multiple bank accounts. Without a constructor, you'd have to manually write the same properties and values for each account like this:

```jsx
const account1 = {
  customerName: "Ayan",
  accountNo: Date.now(),
  balance: 100,
};

const account2 = {
  customerName: "Komal",
  accountNo: Date.now(),
  balance: 200,
};

// More accounts...
```

This becomes repetitive and inefficient as you need to create more accounts. You would have to write the same structure again and again. This is where a **constructor function** helps.

### What is a Constructor?

A constructor is like a **template**. Instead of manually creating objects one by one, you define the structure once using a constructor function, and then you can create as many objects as you want by just calling the constructor with different values.

### Example: Constructor for Bank Accounts

```jsx
function bankAccount(customerName, balance = 0) {
  this.customerName = customerName; // Assign customer name to the object
  this.accountNo = Date.now(); // Generate a unique account number using the current time
  this.balance = balance; // Assign the initial balance; default is 0
}

// Create a new account for "Ayan" with a balance of 100
const obj = new bankAccount("ayan", 100);

// Output the newly created object
console.log(obj);

bankAccount {
  customerName: "ayan",
  accountNo: 1728791401905,
  balance: 100,
}

### How the Constructor Helps:

1. **Reusability**: You define the structure once, and you can use it repeatedly to create as many objects as needed. For example:


const obj1 = new bankAccount("ayan", 100);
const obj2 = new bankAccount("komal", 200);
const obj3 = new bankAccount("alex", 150);


- **Avoids Repetition**: Instead of writing the same code over and over for each object (like manually typing `customerName`, `accountNo`, `balance`), the constructor function automates this process.
- **Dynamic Object Creation**: With the constructor, you can dynamically generate unique properties (like `accountNo` using `Date.now()`), so each object has its own distinct values.
- **Easier Maintenance**: If you need to change the structure (e.g., add new properties), you only update the constructor function, and it will apply to all future objects.
```

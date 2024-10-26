## goit-neo-js-hw-06

## Task 1. User account

Before leaving, the developer broke the original code for managing user accounts in our food delivery service. Refactor the methods of the customer object by correctly using this when accessing object properties.

Use this starter code and perform the refactoring. After declaring the object, we added method calls. The results of their execution will be printed on the console. Please do not change anything there.

const customer = {
  username: "Mango",
  balance: 24000,
  discount: 0.1,
  orders: ["Burger", "Pizza", "Salad"],
  // Change code below this line
  getBalance() {
    return balance;
  },
  getDiscount() {
    return discount;
  },
  setDiscount(value) {
    discount = value;
  },
  getOrders() {
    return orders;
  },
  addOrder(cost, order) {
    balance -= cost - cost * discount;
    orders.push(order);
  },
  // Change code above this line
};

customer.setDiscount(0.15);
console.log(customer.getDiscount()); // 0.15
customer.addOrder(5000, "Steak");
console.log(customer.getBalance()); // 19750
console.log(customer.getOrders()); // ["Burger", "Pizza", "Salad", "Steak"]



## Task 2. Warehouse

Create a class Storage that creates objects to manage a warehouse of goods. The class expects only one argument — an initial array of goods stored in the created object's private property items.

Declare the following methods of the class:

getItems() — returns the array of current goods in the private property items.
addItem(newItem) — takes a new item newItem and adds it to the array of goods in the private property items of the object.
removeItem(itemToRemove) — takes a string itemToRemove with the item's name and removes it from the array of goods in the private property items of the object.

Take the code below with the instance initialization and method calls and insert it after the class declaration for correctness checking. The results of their operation will be output to the console. Please do not modify anything there.

const storage = new Storage(["Nanitoids", "Prolonger", "Antigravitator"]);
console.log(storage.getItems()); // ["Nanitoids", "Prolonger", "Antigravitator"]
storage.addItem("Droid");
console.log(storage.getItems()); // ["Nanitoids", "Prolonger", "Antigravitator", "Droid"]
storage.removeItem("Prolonger");
console.log(storage.getItems()); // ["Nanitoids", "Antigravitator", "Droid"]



## Task 3. String constructor

Write a class StringBuilder that accepts one parameter initialValue — an arbitrary string stored in the created object's private property value.

Declare the following methods of the class:

getValue() — returns the current value of the private property value.
padEnd(str) — takes parameter str (a string) and appends it to the end of the value of the private property value of the object that calls this method.
padStart(str) — takes parameter str (a string) and prepends it to the beginning of the value of the private property value of the object that calls this method.
padBoth(str) — takes parameter str (a string) and appends it to the end, and prepends it to the beginning of the private property value of the object that calls this method.

Take the code below with the instance initialization and method calls and insert it after the class declaration for correctness checking. The results of their operation will be output to the console. Please do not modify anything there.

const builder = new StringBuilder(".");
console.log(builder.getValue()); // "."
builder.padStart("^");
console.log(builder.getValue()); // "^."
builder.padEnd("^");
console.log(builder.getValue()); // "^.^"
builder.padBoth("=");
console.log(builder.getValue()); // "=^.^="


## Requirements
- Code must be formatted with Prettier.
- There must be no errors or warnings in the console after running the tasks.
- Execution of tasks 1, 2 and 3.

## Formatting the code with Prettier:

* You must have Node.js installed, then install Prettier in your project. This can be done with the command in the terminal:

```bash
npm install --save-dev prettier
```

* Then you can run Prettier on your code with:

```bash
npx prettier --write .
```

This command will format all files in the project.
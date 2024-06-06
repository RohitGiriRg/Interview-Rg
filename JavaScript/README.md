### **JS Concepts**

---

Hoisting in Javascript.

Youtube : - https://www.youtube.com/watch?v=EvfRXyKa_GI

Explanation :

All the code in the javascripts runs from top to bottom.

Hoisting in JavaScript is a behavior in which variable and function declarations are moved to the top of their containing scope during the compilation phase. This means that you can use variables and functions before they are declared in the code. However, the way hoisting works for variables and functions is different.

```
console.log(x); // Output: undefined
var x = 5;
console.log(x); // Output: 5

```

In the above example, the `var x` declaration is hoisted to the top, but the assignment `x = 5` is not.

Variables declared with `let` and `const` are also hoisted, but they are not initialized. Accessing them before their declaration results in a `ReferenceError` due to the "temporal dead zone" (TDZ).

### Function Hoisting

Function declarations are fully hoisted, which means both the declaration and the body of the function are moved to the top of the containing scope. This allows you to call functions before they appear in the code.

```
greet(); // Output: Hello, world!

function greet() {
  console.log("Hello, world!");
}

```

In the above example, `var sayHello` is hoisted to the top, but the assignment `sayHello = function() {...}` is not. Hence, `sayHello` is `undefined` when it is called the first time.

### Summary

- **Variables (var):** Declaration is hoisted, initialization is not.
- **Variables (let/const):** Declaration is hoisted but not initialized, leading to the temporal dead zone (TDZ).
- **Functions (declarations):** Fully hoisted (both declaration and definition).
- **Functions (expressions):** Only the variable declaration is hoisted, not the assignment.

Understanding hoisting helps in avoiding unexpected behaviors and bugs in JavaScript code, especially when dealing with variable and function scopes.

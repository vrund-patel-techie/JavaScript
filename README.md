# 📒 JavaScript – Daily Learning & Revision Log

This file tracks what I study every day so I can **quickly revise core JS concepts before interviews, coding rounds, or project work.**

---

## 🗓️ 12 / 01 / 2026

### Topics to discover by self

- **Concept of Shadowing**
  - How inner scope variables hide outer scope variables.
  - Difference in behavior for `var`, `let`, and `const`.

- **Window Object**
  - Global object in browser.
  - `var` becomes property of `window`, `let` & `const` do not.

- **Execution Test**
  - Call stack  
  - Execution context  
  *(Based on: Chai aur Code & Namaste JavaScript)*

- **Primitive vs Non-Primitive Data Types**
  - Memory storage difference (Stack vs Heap)
  - Mutability concept

- **Call by Value vs Call by Reference**
  - How primitives copy values.
  - How objects/arrays share reference.

### 📄 Notes / Slides  
🔗 https://www.genspark.ai/slides?project_id=e12425c6-7425-4a1c-b31e-a019b440942f&export_dialog=true

---

## 🗓️ 13 / 01 / 2026

### Topics Practiced

- **`var`, `let`, `const` in `for` loop**
  - Scope issue  
  - Closure behavior

- **`setTimeout()`**
  - Asynchronous execution  
  - Event loop & callback queue behavior

- **Array Slice inside Loop**
  - Creating same/similar arrays  
  - Preventing mutation of original array

### 📄 Notes / Document  
🔗 https://docs.google.com/document/d/1cQrakFROGFPwKOzDZ_HNWyUz_HTRWB3u1GDzt2DRzEo/edit?tab=t.0

## ✅ Task 1 — Try `var`, `let`, and `const` in a `for` loop  

### Objective:
To understand **scope of variables in JavaScript**.

### Key Concepts Learned:

| Keyword | Scope | Reassignable? | Redeclarable? |
|--------|--------|---------------|---------------|
| `var` | Function scope | ✅ Yes | ✅ Yes |
| `let` | Block scope | ✅ Yes | ❌ No |
| `const` | Block scope | ❌ No | ❌ No |

### Observations:

#### Using `var`
```js
for (var i = 0; i < 3; i++) {
  console.log("Inside:", i);
}
console.log("Outside:", i);
```
Result:
i is accessible outside the loop → shows that var is not block scoped.

```js
for (let i = 0; i < 3; i++) {
  console.log("Inside:", i);
}
console.log("Outside:", i);
```
Result:
Throws ReferenceError → proves that let is block scoped.

```js
for (const i = 0; i < 3; i++) {
  console.log(i);
}
```
Result:
Error occurs because const cannot be reassigned — so it is not suitable for loop counters.
Final Takeaway:
👉 Always prefer let for loop variables.

## ✅ Task 2 — Try setTimeout()
Objective:
To understand asynchronous behavior of JavaScript.
```js
console.log("Start");

setTimeout(() => {
  console.log("Executed after 2 seconds");
}, 2000);

console.log("End");

Output :
Start  
End  
Executed after 2 seconds  
```
### Concept Learned:
JavaScript is single-threaded but asynchronous.
Flow:
console.log("Start") runs
setTimeout is sent to Web APIs
JS continues execution
After delay, callback goes to callback queue
When call stack is free, callback executes
This mechanism is called the Event Loop.

## ✅ Task 3 - Slice a similar array inside a for loop
Objective:
To understand array copying vs mutation.
Example using slice():

```js
let arr = [1, 2, 3, 4, 5];

for (let i = 0; i < arr.length; i++) {
  let newArr = arr.slice(0, i + 1);
  console.log(newArr);
}

Output:
[1]
[1,2]
[1,2,3]
[1,2,3,4]
[1,2,3,4,5]
```
### Concept Learned:
slice() creates a new array
It does not modify the original array
It is a non-mutating method
Contrast with splice():

```js
let arr = [1,2,3,4,5];
arr.splice(0,2);
console.log(arr);

Output:
[3,4,5]
```
Here, splice() modifies the original array → it is a mutating method.
## Summary of Learnings
✔ Scope of variables (var, let, const)
✔ Asynchronous behavior (setTimeout)
✔ Event loop concept
✔ Difference between slice() and splice()
✔ Mutating vs non-mutating methods

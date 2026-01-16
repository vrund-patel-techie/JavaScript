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

# JavaScript Learning Notes – Practice Tasks

This document contains my understanding and learnings from the following JavaScript practice tasks suggested by my senior.

---

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

---

## 🎯 Purpose of This File

- Daily revision  
- Interview preparation  
- Strengthen JavaScript fundamentals  
- Track consistency in learning

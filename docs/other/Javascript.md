## var / let / const 的区别？
- `var`：函数作用域、可重复声明、存在变量提升。  
- `let / const`：块级作用域、不可重复声明、存在暂时性死区。  
- `const`：必须初始化，不能重新赋值（对象内部属性可修改）。

---

## 原型链与作用域链的区别？
- 原型链：对象属性查找时沿 `__proto__` 向上追溯，用于实现继承。  
- 作用域链：变量查找时沿当前执行上下文的作用域向上查找。

---

## 什么是闭包？应用场景与注意事项？
- 定义：函数与其词法环境的组合，能访问外部作用域变量。  
- 场景：模块化封装、防抖节流、数据缓存。  
- 注意：可能导致内存泄漏，需适时释放引用。

---

## Promise 的状态与方法？async/await 原理？
- 状态：`pending` → `fulfilled` / `rejected`  
- 方法：`then`、`catch`、`finally`、`all`、`race`  
- async/await：基于 Promise 的语法糖，使异步代码看起来像同步，await 会暂停 async 函数执行直到 Promise 完成。

---

## 事件循环（Event Loop）运行机制？
- JS 单线程，通过事件循环处理异步任务。  
- 宏任务（setTimeout、I/O）与微任务（Promise.then、MutationObserver）交替执行：先执行完当前宏任务的所有微任务，再取下一个宏任务。

---

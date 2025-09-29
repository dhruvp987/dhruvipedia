---
layout: ../../layouts/ArticleLayout.astro
title: 'Lisp'
---

Common Lisp, otherwise simply known as Lisp, is one of the oldest programming languages in the world. It is a unique, powerful, and innovative language,
unlike most others.

Programs in many programming languages, such as C, Java, and Python, are composed of *statements*. A statement is some code that performs some effect on the state of a program.
Meanwhile, Lisp programs, inspired by lambda calculus, are composed of *expressions*. An expression is some code whose result is evaluated and returned,
without necessarily changing the state of the program. Composing programs with expressions is also known as *functional programming*, and contrasts with the 
statement-oriented *imperative programming* of C, Java, Python, and others. Functional programming can lead to more predictable programs, improving maintainability.

The predictability of functional programming that Lisp naturally provides have recently resurged in popularity due to its value in large, distributed, 
data-driven programs, as predictability can simplify complex data workloads and coordination within systems, improving scalability and maintainability.

Expressions in Lisp are denoted by a pair of parentheses. Thus, most executable chunks of code are surrounded by parentheses. 
Many people find Lisp programs hard to read due to this syntax.

Here is an example of a Lisp program that calculates and outputs 5!:
```lisp
(defun factorial (n &optional (a 1))
  (if (<= n 1) a
    (factorial (- n 1) (* n a))))

(format t "~a~%" (factorial 5))
```
*factorial* is a recursive function that uses tail call optimization, which is achieved by using an accumulating parameter.

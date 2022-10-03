---
layout: post
title: "Best Practices for Writing Scientific Code"
categories: coding
author: Mardochée Réveil
---

Scientists are typically not trained on how to write readable and maintainable code. However,
good coding hygiene can save you a lot of time in your research. Here are some best
practices that I learned the hard way. Hopefully, you can avoid some of the mistakes I made.

## 1. Write Modular Code

Break your code down into functions and split large codebases into multiple files.

This also holds for what you'd consider simple analysis scripts. And yes, even MATLAB scripts.

There is no universal limit for when a function or script is too long but...

If your code is hundreds of lines long, you should break it down into functions.

My rule of thumb: if I can describe a block of code with a couple of words, I refactor it into a function.

Functions make your code easier to understand but also help with unit testing (see below).

Group your functions into files in a logical fashion.

If you use a language that supports Object-Oriented Programming (OOP), take advantage of the features afforded by OOP such as abstraction, inheritance, etc.

## 2. Use Meaningful Names

The names that you choose for your files, functions and variables should be as descriptive as possible.

Avoid generic names like a, b, c, sol, solution, etc.

This will lower the cognitive load needed for you and others to understand your code later.

## 3. Write Unit Tests

Unit tests ensure your code is robust and works as intended.

This is critical for scientific applications because one simple mistake can throw your entire program off.

The extra time spent writing unit tests will save you many hours later.

Most programming languages offer libraries to write and run unit tests.

Python's standard unit testing library is unittest but I use pytest, one of several alternatives.

Include edge cases in your test suites.

If your code is modular, writing unit tests is easier.

Sometimes it helps to use a test-driven dev workflow where you write your tests first and then the code.

As you write more tests however, you need to strike a balance between how comprehensive your test suite needs to be and the expected lifecycle of your code.

## 4. Use Version Control

This is a must if you want to manage your code well.Even more so if you share your code with other people.

The most popular version control system is git (not to be confused with GitHub, a popular online platform to manage git repositories).

git can be a little hard to understand at first but once you get a hold of it, you will never go back.

The best way to get started is to use it in one of your projects. Try it on your local machine first. Here's the official website if you don't already have it: https://git-scm.com/downloads

Focus on the following:

- Initialize a new repo

- Stage and commit your changes

- Create a new branch

- Switch branch

- Merge branches

Once you master these, try to add an online repo to your workflow.

@GitHub, @GitLab and @BitBucket are popular online options to consider.

## 5. Document your Code

Each function should be documented with:

- a short description of what it does

- the expected type and description of all inputs and outputs

- additional inline comments to further explain specific sections

- Optionally, a long description with examples

## 6. Use consistent formatting

Follow the style guide of the language that you use.

Pay special attention to:

- Variables and function names (use camelCase or snake_case, not both)

- Max line length (usually between 79-100)

- Code layout

- spaces vs tabs (choose one)

## 7. Use a linter to catch errors

Linters analyze your code to identify violations against your language's style guide.

They can also spot common issues such as unused variables.

Setup your linter to run automatically in your git workflow.

flake8 is my go-to linter in Python.

## 8. Use a formatter to fix errors

Unlike linters, formatters automatically reformat your code to fix styling issues.

Black https://github.com/psf/black is a good choice for Python.

If you use VS Code, set it up to run automatically after each save operation

To summarize, follow these best practices when you write scientific code:

1. Write modular code
2. Use meaningful names
3. Write unit tests
4. Use version control
5. Document your code
6. Use consistent formatting
7. Use linters to detect issues
8. Use formatters to fix issues

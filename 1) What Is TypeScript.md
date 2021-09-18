# What Is TypeScript?

Typescript is an extension to JavaScript - it's not a programming language by itself,
but more of a 'tool' to develop a better JavaScript.


* TypeScript is a superset of JavaScript, meaning it's another layer around JavaScript.
* Browsers, or other JavaScript engines, can't run TypeScript. You need to compile the TypeScript code down to JavaScript code
* All the new features in TypeScript is compiled into workarounds in JavaScript (Pollyfills and Transpilers).
* **TypeScript allows you static typing in JavaScript.**

### What is Static Typing?

> A statically-typed language is a language (such as Java, C, or C++) where variable types are known at compile time. In most of these languages, types must be expressly indicated by the programmer;

[Reference] (https://developer.mozilla.org/en-US/docs/Glossary/Static_typing)

### What Static Typing Is Good For?

Example:
```
function add(num1, num2) {
    return num1 + num2;
}
```

This is a valid function, but what if the next developer working on the code, \
will use this function like this: `add('10', '20')` ?

Because the two arguments are of type string, instead of type number, \
the code won't generate a runtime error at this moment, \
but a logical error that will cause an unwanted behavior on our code.


**JavaScript Solution:**

In JavaScript, we can validate the input for each function, which will cause extra code writing and error potential.
```
function add(num1, num2) {
    if (typeof(num1) !== 'number') {
        throw Error(`num1 argument must be a number!`);
    }
    if (typeof(num2) !== 'number') {
        throw Error(`num2 argument must be a number!`);
    }
    return num1 + num2;
}
```

**TypeScript Solution:**

In TypeScript, we can avoid logical errors, or runtime errors, by static typing.
```
function add(num1: number, num2: number): number {
    return num1 + num2;
}
```

**Extra Reading**

[TypeScript Docs](https://www.typescriptlang.org/) \
[TypeScript in Wikipedia](https://en.wikipedia.org/wiki/TypeScript)
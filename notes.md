# Eloquent JavaScript Fourth Edition
# by Marijn Haverbeke
# Personal Notes

**Reader:** Emre Önsür

## What is JavaScript?

> 2026-11-26 Potsdam, Germany

Javascript was introduced in 1995 as a way to add programs to web pages in the *Netscape Navigator Browser*. It has made modern web applications possible—that is, applications with which you can interact directly without doing a page reload for every action.

Javascript has almost nothing to do with the programming language *Java*. The name was inspired by marketing considerations. When JavaScript was being introduced, Java was gaining popularity, so that someone thought it was a good idea to try to ride along on this success.

After its adoption outside of Netscape, a standart document was written to describe the way the JavaScript language should work so that the various pieces of software that claimed to support JavaScript could make sure they actually provided the same language. The Ecma International organization conducted the standardization, and this is called the **ECMAScript standart**. ECMAScript and JavaScript can be used interchangeably.

## The Atomic Elements of JavaScript

In JavaScript, the **atomic elements** are the smallest, indivisible pieces you use to build *everything else*.

There are two core atomic elements in JavaScript:

- **Simple (primitive) value types**
- **Operators**

### Numbers

> 2026-11-27 Potsdam, Germany

JavaScript `Number` type is stored in 64 bits and follows the [IEEE-754](https://en.wikipedia.org/wiki/IEEE_754). Consuquently, whole numbers are represented by 53 of those bits.

Therefore, the **range_ of whole numbers** that can be represented with the `Number` type is **[-9_007_199_254_740_991, +9_007_199_254_740_991]**.

A `Number` value can be written in several ways:

- As an integer: `23`
- As a fractional number using a dot: `9.81`
- Using scientific notation: `2.998e2`

> Calculations with integers that are in the aforementioned range are guaranteed to always be precise. However, calculations with fractional numbers are generally not.

```javascript
console.log(0.1 + 0.2);
```

#### Arithmetic Operators

```javascript
console.log(20 + 10);
console.log(20 - 10);
console.log(20 * 10);
console.log(20 / 10);
console.log(10 % 3);
```

#### Special Numbers

There are three special values that are considered numbers but don't behave like normal numbers:

- `Infinity`
- `-Infinity`
- `NaN` — which stands for "not a number"

For IEEE-754 64-bit floating point numbers (e.g. JS `Number`), x as a non-zero value:

- If `x > 0`, then `x / 0` is `Infinity`
- If `x < 0`, then `x / 0` is `-Infinity`
- `0 / 0` is `NaN`

For being JS-specific:

```javascript
console.log(3 / 0); // Infinity
console.log(-3 / 0); // -Infinity
console.log(3 / -0); // -Infinity
console.log(-3 / -0); // Infinity
console.log(0 / 0); // NaN
console.log(-0 / 0); // NaN
console.log(0 / -0); // NaN
console.log(-0 / -0); // NaN
console.log(Infinity + Infinity); // Infinity
console.log(Infinity - Infinity); // Nan
console.log(Infinity * Infinity); // Infinity
console.log(Infinity / Infinity); // NaN
console.log(Infinity % Infinity); // NaN
```

### Strings


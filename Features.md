# Features

## Macros

Built in support for [hygenic macros](https://en.wikipedia.org/wiki/Hygienic_macro).
Allows prototyping and simplifies feature addition.
Allows for simple syntax-transformations:

- define new operators

#### Prior Art

Elixir, Scheme, Kit, Sweet.js

## Literals and Primitives

### Numbers

Numeric literals should follow the [ECMAScript specification](https://www.ecma-international.org/ecma-262/6.0/#sec-literals-numeric-literals)

Examples:

- hex literal :: `0(x|X)[a-fA-F0-9]+`
- binary literal :: `0(b|B)[0|1]+`
- octal literal :: `0(o|O)[0-7]+`

### Dates

Would a date literal type be useful?

Depends on the level of support for dates in the standard library

## Comments

Use C/ECMAScript style comments:

- block comment `/* */`
- line comment `//`

Allow nested comments

Documentation comments should be in the form `/** */`  
Only allowed in some places and part of the AST for easy documentation generation:

#### Prior Art

Python, Nim

## Observables and Generators

Built in support for [observables](https://en.wikipedia.org/wiki/Observer_pattern) and [generators/iterables](<https://en.wikipedia.org/wiki/Generator_(computer_programming)>).

Observables are push based - the observable pushes changes to its subscribers

Generators are pull based - they yield values that must be pulled by consumers

See [article](https://staltz.com/why-we-need-callbags.html)

Generators should be immutable (can be reused, unlike ECMAScript generators)

#### Prior Art

- Generators: Python, ECMAScript
- Observables: callbags, rxjs, cyclejs

## Promises

Similar to ECMAScript promises / single-valued observable  
deferred by default - must explicitly start the request

## Paridigm

### Strongly Typed

Strongly typed, with higher kinded types, GADTs.
Strong type inference

#### Prior Art

Haskell

### Functional

Support for functional programming - functions are first-class values
Everything is an expression. No statements like for, while

#### Prior Art

Haskell, ECMAScript, Scheme/Lisp

### Lazy

Language is inherently lazy

#### Prior Art

Haskell

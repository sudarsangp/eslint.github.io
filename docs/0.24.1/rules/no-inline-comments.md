---
title: Rule no-inline-comments
layout: doc
---
<!-- Note: No pull requests accepted for this file. See README.md in the root directory for details. -->
# Disallows comments after code. Comments must come on their own lines (no-inline-comments)

Some style guides disallow a comments on the same line as code.
If there are comments immediately following code, it can make it harder to read the code.
On the other hand, it is sometimes faster and more obvious to put comments immediately following code.


## Rule Details

This rule will disallow comments on the same line as code.

This rule takes no arguments.

The following patterns are considered warnings:

```js
var a = 1; // declaring a to 1
```

```js
function getRandomNumber(){
return 4; // chosen by fair dice roll.
          // guaranteed to be random.
}
```

```js
/* A block comment before code */ var a = 2;
```

```js
var a = 3; /* A block comment after code */
```

The following patterns are not warnings:

```js
// This is a comment above a line of code
var foo = 5;
```

```js
var foo = 5;
//This is a comment below a line of code
```

## Version

This rule was introduced in ESLint 0.10.0.

## Resources

* [Rule source](https://github.com/eslint/eslint/tree/master/lib/rules/no-inline-comments.js)
* [Documentation source](https://github.com/eslint/eslint/tree/master/docs/rules/no-inline-comments.md)

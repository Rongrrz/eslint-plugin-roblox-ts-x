# Disallow unsupported syntax in roblox-ts

<!-- end auto-generated rule header -->
<!-- Do not manually modify this header. Run: `npm run eslint-docs` -->

## Rule details

This rule bans the use of certain TypeScript syntax features that are not supported or behave differently in the roblox-ts environment.

Currently, this rule disallows:

-   `globalThis`: This global object is not available in the Roblox environment.
-   `.prototype`: Accessing the `prototype` property of constructors is not supported and can lead to errors.
-   Regex Literals (`/pattern/flags`): These are not directly supported. Use the
    `RegExp` constructor instead (from `@rbxts/luau-polyfill`) or an alternative.
-   Spread operator (`...`): Not supported for object or array destructuring.
-   Labeled Statements (`label:`): These are not supported in roblox-ts.

## Examples

### Incorrect

```js
// globalThis
const win = globalThis; // ❌ globalThis is not supported

// .prototype
function MyConstructor() {}
const proto = MyConstructor.prototype; // ❌ .prototype is not supported

class MyClass {}
const classProto = MyClass.prototype; // ❌ .prototype is not supported

// Regex Literals
const pattern = /abc/i; // ❌ Regex literals are not supported
if (/test/.test(str)) { // ❌ Regex literals are not supported
  // ...
}

// Operator ...
const { a, ...b } = { a: 1, b: 2 }; // ❌ Spread operator is not supported
const arr = [1, 2, 3];
const newArr = [...arr, 4]; // ❌ Spread operator is not supported

// Labeled Statements
myLabel: for (let i = 0; i < 5; i++) { // ❌ Labeled statements are not supported
  if (i === 1) continue myLabel;
}

myBlock: { // ❌ Labeled statements are not supported
  if (true) break myBlock;
}
```

### Correct

```js
// Instead of .prototype, use static methods or other patterns.
class MyClass {
  static staticMethod() {}
}
MyClass.staticMethod();

// Instead of regex literals, you can use the RegExp constructor from `@rbxts/luau-polyfill`.
const pattern = new RegExp("abc", "i");
if (new RegExp("test").test(str)) {
  // ...
}
```

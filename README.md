# eslint-plugin-roblox-ts-x

[![npm version][npm-version-src]][npm-version-href]
[![npm downloads][npm-downloads-src]][npm-downloads-href]
[![bundle][bundle-src]][bundle-href]
[![JSDocs][jsdocs-src]][jsdocs-href]
[![License][license-src]][license-href]

A collection of ESLint rules specifically targeted to flag common issues when
using [roblox-ts](https://roblox-ts.github.io/roblox-ts/). These rules are
nearly all designed to help avoid compiler errors for features that are not
supported by the roblox-ts compiler, despite being valid TypeScript.

These rules should help users move from TypeScript to roblox-ts, as well as help
users who wish to learn roblox-ts when coming from Lua.

## Rules

<!-- Do not manually modify this list. Run: `npm run eslint-docs` -->
<!-- begin auto-generated rules list -->

🔧 Automatically fixable by the [`--fix` CLI option](https://eslint.org/docs/user-guide/command-line-interface#--fix).\
💡 Manually fixable by [editor suggestions](https://eslint.org/docs/latest/use/core-concepts#rule-suggestions).\
💭 Requires [type information](https://typescript-eslint.io/linting/typed-linting).

| Name                                                                                  | Description                                                                                                         | 🔧 | 💡 | 💭 |
| :------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------------------------------------ | :- | :- | :- |
| [lua-truthiness](src/rules/lua-truthiness/documentation.md)                           | Enforces the use of lua truthiness in roblox-ts                                                                     |    |    | 💭 |
| [misleading-lua-tuple-checks](src/rules/misleading-lua-tuple-checks/documentation.md) | Disallows the use of LuaTuple in conditional expressions                                                            | 🔧 |    | 💭 |
| [no-any](src/rules/no-any/documentation.md)                                           | Disallow values of type `any` is not supported! Use `unknown` instead                                               | 🔧 | 💡 |    |
| [no-array-pairs](src/rules/no-array-pairs/documentation.md)                           | Disallows usage of pairs() and ipairs() with Array<T>                                                               |    |    | 💭 |
| [no-enum-merging](src/rules/no-enum-merging/documentation.md)                         | Disallow merging enum declarations                                                                                  |    |    |    |
| [no-export-assignment-let](src/rules/no-export-assignment-let/documentation.md)       | Disallow using `export =` on a let variable as it is not supported in roblox-ts                                     |    |    |    |
| [no-for-in](src/rules/no-for-in/documentation.md)                                     | Disallows iterating with a for-in loop                                                                              | 🔧 |    |    |
| [no-function-expression-name](src/rules/no-function-expression-name/documentation.md) | Disallow the use of function expression names as they are not supported                                             | 🔧 |    |    |
| [no-get-set](src/rules/no-get-set/documentation.md)                                   | Disallows getters and setters                                                                                       | 🔧 |    |    |
| [no-invalid-identifier](src/rules/no-invalid-identifier/documentation.md)             | Disallow the use of Luau reserved keywords as identifiers                                                           |    |    |    |
| [no-namespace-merging](src/rules/no-namespace-merging/documentation.md)               | Disallow merging namespace declarations                                                                             |    |    |    |
| [no-null](src/rules/no-null/documentation.md)                                         | Disallow usage of the 'null' keyword in TypeScript                                                                  | 🔧 |    |    |
| [no-object-math](src/rules/no-object-math/documentation.md)                           | Disallow using objects in mathematical operations                                                                   | 🔧 |    | 💭 |
| [no-post-fix-new](src/rules/no-post-fix-new/documentation.md)                         | Disallow the use of .new() on objects without a .new() method. This is useful to help users transition to roblox-ts | 🔧 |    | 💭 |
| [no-preceding-spread-element](src/rules/no-preceding-spread-element/documentation.md) | Disallow spread elements not last in a list of arguments from being used,                                           |    |    | 💭 |
| [no-private-identifier](src/rules/no-private-identifier/documentation.md)             | Disallow the use of private identifiers (`#`)                                                                       | 🔧 |    |    |
| [no-unsupported-syntax](src/rules/no-unsupported-syntax/documentation.md)             | Disallow unsupported syntax in roblox-ts                                                                            |    |    |    |
| [no-value-typeof](src/rules/no-value-typeof/documentation.md)                         | Disallow using `typeof` to check for value types                                                                    |    |    |    |
| [prefer-task-library](src/rules/prefer-task-library/documentation.md)                 | Enforce use of task.wait(), task.delay(), and task.spawn() instead of global wait(), delay(), and spawn()           | 🔧 |    |    |
| [size-method](src/rules/size-method/documentation.md)                                 | Enforce use of .size() method instead of .length or .size property for Roblox compatibility                         | 🔧 |    | 💭 |

<!-- end auto-generated rules list -->

## License

[MIT](./LICENSE) License © [Christopher Buss](https://github.com/christopher-buss)

<!-- Badges -->

[npm-version-src]: https://img.shields.io/npm/v/eslint-plugin-roblox-ts-x?style=flat&colorA=080f12&colorB=1fa669
[npm-version-href]: https://npmjs.com/package/eslint-plugin-roblox-ts-x
[npm-downloads-src]: https://img.shields.io/npm/dm/eslint-plugin-roblox-ts-x?style=flat&colorA=080f12&colorB=1fa669
[npm-downloads-href]: https://npmjs.com/package/eslint-plugin-roblox-ts-x
[bundle-src]: https://img.shields.io/bundlephobia/minzip/eslint-plugin-roblox-ts-x?style=flat&colorA=080f12&colorB=1fa669&label=minzip
[bundle-href]: https://bundlephobia.com/result?p=eslint-plugin-roblox-ts-x
[license-src]: https://img.shields.io/github/license/christopher-buss/eslint-plugin-roblox-ts-x.svg?style=flat&colorA=080f12&colorB=1fa669
[license-href]: https://github.com/christopher-buss/eslint-plugin-roblox-ts-x/blob/main/LICENSE
[jsdocs-src]: https://img.shields.io/badge/jsdocs-reference-080f12?style=flat&colorA=080f12&colorB=1fa669
[jsdocs-href]: https://www.jsdocs.io/package/eslint-plugin-roblox-ts-x

---
id: tslint
title: What About TSLint?
sidebar_label: What About TSLint?
---

TSLint was a linter equivalent to ESLint that was written specifically to work directly on TypeScript code.

**TSLint is deprecated** and you should use `typescript-eslint` instead.

## Migrating from TSLint to ESLint

The standard tool to convert a TSLint configuration to the equivalent ESLint configuration is [`tslint-to-eslint-config`](https://github.com/typescript-eslint/tslint-to-eslint-config).
If you are still using TSLint, we strongly recommend you use this tool to switch.

You can look at [the alternatives list](https://github.com/typescript-eslint/typescript-eslint/blob/main/packages/eslint-plugin/TSLINT_RULE_ALTERNATIVES.md) for an up to date overview of how TSLint rules compare to the ones in this package.

There is also the ultimate fallback option of using both linters together for a while during your transition if you
absolutely have to by using TSLint _within_ ESLint.
For this option, check out [`@typescript-eslint/eslint-plugin-tslint`](https://github.com/typescript-eslint/typescript-eslint/tree/main/packages/eslint-plugin-tslint).

## Why Deprecate TSLint?

One advantage of TSLint over ESLint was that there was no tooling required to reconcile differences between JavaScript and TypeScript syntax.
Unfortunately, that meant TSLint couldn't reuse any of the previous work which has been done in the JavaScript ecosystem around ESLint.
TSLint had to reimplement everything from editor extensions to auto-fixing to rules.

TSLint's backers announced in 2019 that **they would be deprecating TSLint in favor of supporting `typescript-eslint`** in order to benefit the community.
You can read more about that here: https://medium.com/palantir/tslint-in-2019-1a144c2317a9.

The TypeScript team also migrated move the TypeScript codebase from TSLint to `typescript-eslint`, and they have been supporters of this project.
See more details at https://github.com/microsoft/TypeScript/issues/30553.

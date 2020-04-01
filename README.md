# A Simple Babel Repo

A simple repository that uses BabelJS to create CommonJS module and ES module

## Tools

* I use [pnpm](https://pnpm.js.org) as my package manager, I can use npm or yarn if you wish.
* Require `npm` to run some tasks.

## Explanation

### Files

* `*.babelrc` are config files for Babel to read:
  * `cjs.babelrc` is to generate CommonJS files.
  * `esm.babelrc` is to generate ES modules.
* `src/` contains all JavaScript source code.
* `lib/` contains all compiled JavaScript:
  * `lib/cjs/` contains all CommonJS product.
  * `lib/esm/` contains all ES module product.

### NPM Scripts

* `npm run build:cjs` to build all CommonJS files.
* `npm run build:esm` to build all ES module files.
* `npm run build` to build both of them.

### Entry points

* CommonJS: Set `main` and `exports['.'].require` to `lib/cjs/index.js`.
* ES Module: Set `module` and `exports['.'].module` to `lib/esm/index.js`.

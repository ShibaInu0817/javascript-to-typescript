# Declare javascript module for typescript

✨ **A simple JavaScript package with basic arithmetic functions, packaged it, and installed it into a TypeScript project.** ✨

## App Structure

- sample-math-package
- ts-project

## Presentation Diagram

```js
// index.js

function add(a, b) {
  return a + b;
}

function subtract(a, b) {
  return a - b;
}

function multiply(a, b) {
  return a * b;
}

function divide(a, b) {
  if (b === 0) {
    throw new Error("Cannot divide by zero!");
  }
  return a / b;
}

module.exports = {
  add,
  subtract,
  multiply,
  divide,
};
```

```ts
declare module "sample-math-package" {
  export function add(a: number, b: number): number;
  export function subtract(a: number, b: number): number;
  export function multiply(a: number, b: number): number;
  export function divide(a: number, b: number): number;
}
```

<img src='./asset/example diagram.png'></img>

## Prerequisite

- npm
- nodeJs

## Start the flow

To start the development server run :

```bash script
cd ./sample-math-package
npm pack
# You should see the generated tgz file after npm pack

cd ../ts-project
npm install
# or
npm install ../sample-math-package/sample-math-package-1.0.0.tgz

## Run the typescript
npx tsc
node main.js ## JS file
```

## Output

```bash script
Add: 15
Subtract: 5
Multiply: 50
Divide: 2
```

# Learn Typescript

> Run code `npx ts-node <code_file>.ts`
> Compile `npx tsc <code_file>.ts`

## Typescript setup

```sh
yarn init -y
yarn add typescript ts-node -D
npx tsc --init
```

## Everyday Types

- Specifying Types

  > Just hover on the variables that you want to know what is it type, then copy the type and pass it for your variable

- **Examples**

```ts
let name: string = "Lê Anh Vũ";
let age: number = 22;
const fooRegex: Regex = /foo/;
const names: string[] = name.split("");
const numbers: Array<number> = [1, 2, 3];

interface Person {
  first: string;
  last: string;
}

const person: Person = {
  first: "Raymond",
  last: "Le",
};

const ids: Record<number, string> = {
  10: "a",
  20: "b",
};
// if not use Record<number, string> type the below line of code will be error alerting
ids[30] = "c";

for (let i = 0; i < 10; i++) {
  console.log(i);
}

[1, 2, 3].forEach((v) => console.log(v));
const out: number[] = [1, 2, 3].map((v) => v * 10);
```

## Typescript Functions

```ts
const addNumbers = (a: number, b: number): number => a + b;
export default addNumbers;

export const addStrings = (str1: string; str2: string = ""): string => `${str1} ${str2}`;

import addNumbers, { addStrings } from "./functions";
addNumbers(1, 2);
addStrings('a', 'b')
```

> What is 'any'? -> any is the type, and it could be anything [number, string, ...], I don't want that, i want to be able to control the types and we want to be able to specify in this
> Typing parameters
> Typing return values
> Const functions
> Destructured imports
> Default parameters
> Union types `const a: number | string;`
> Void functions
> Promise functions
> Rest parameters `` function introduce(salutation: string, ...names: string[]): string { return `${salutation} ${name.join(' ')}`} ``

## Typescript Functions with Functions

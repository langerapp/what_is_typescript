# Boolean

Simple true/false value, supported both in JS & TS called boolean. \
`let isEqual: boolean = false`

# Number
All numeric variables (except for BigIntegers) gets the `number` datatype. 
```
let decimal: number = 6;
let hex: number = 0xf00d;
let binary: number = 0b1010;
let octal: number = 0o744;
let big: bigint = 100n;
```
* BigInteger is a number bigger than max safe integer. 2^53 - 1 or 9,007,199,254,740,991

# String
String refer to textual values
```
let color: string = "blue";
```

# Array
Array refer to array values
```
let list: number[] = [1, 2, 3];
```

# Tuple
Tuple allow you to express an array with a fixed number of elements with known different types.
```
let x: [string, number];
let y: [number, number];
let z: [string, string, string];

```

# Enum
Enum is a more human way to address sets of numeric values.
```
enum Animal {
  Cat,
  Dog,
  Cow,
}
let dog: Animal = Animal.Dog;
```

* By default, members in Enum got numbered at 0, you can initiate each member with any number or string.

# Unknown
Whenever a value may come from a dynamic content
```
let userInput = unknown = '28';
```

# Any
Default type for untyped value, accept all values. Best practice is to be never used.
```
let number: any = 'dog';
```

# Void
Commonly used as a return type to a function that do not have a return statement
```
function warnUser(): void {
  console.log("This is my warning message");
}
```

# Null and Undefined
By default, null and undefined are subtypes of all other types. \
That means you can assign null and undefined to something like number. Unless when using the --strictNullChecks flag.
```
let u: undefined = undefined;
let n: null = null;
```

# Never
A type of values that never occur. For example, throw error, or never ending loop.
```
function error(message: string): never {
  throw new Error(message);
}

function infiniteLoop(): never {
  while (true) {
    // do something forever
  }
}
```

# Object
non-primitive type
```
let person = { age: 21, gender: 'Male' };
function isMale(p: object): boolean {
    return p.gender === 'Male';
}
```

**Extra Reading:**

[TypeScript Basic Types](https://www.typescriptlang.org/docs/handbook/basic-types.html#string) \
[Max Safe Integer](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/MAX_SAFE_INTEGER) \
[Enums In TypeScript](https://www.typescriptlang.org/docs/handbook/enums.html) \
[Hex Colors](https://www.pluralsight.com/blog/tutorials/understanding-hexadecimal-colors-simple)
[Null- and undefined-aware types](https://www.typescriptlang.org/docs/handbook/release-notes/typescript-2-0.html)
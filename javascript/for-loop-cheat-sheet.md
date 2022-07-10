# JavaScript For Loop Cheat Sheet
This is a supplement to [soundof.it JavaScript For Loop](https://soundof.it/javascript-for-loop).

---

## ES1 Classic For Loop
The classic for loop was introduced in ES1.

### Syntax
The classic ES1 for loop is constructed through using the `for` keyword, the three initialization statements and the loop body.
```
for (statement_1, statement_2, statement_3) {
  // body
}
```
`statement_1` initializes values. `statement_2` specifies conditions for the initialized values. `statement_3` changes the initialized values. The loop continues until `statement_2` conditions are no longer met.
```JavaScript
for (var i = 0; i < 6; i++) {
  console.log(i)
} // 0 1 2 3 4 5
```

### Usage
The classic ES1 for loop can be used in multitude of scenarios. For example it can be used to iterate over an array or a string.
```JavaScript
const foo = 'bar'

for (var i = 0; i < foo.length; i++) {
  console.log(foo[i])
} // b a r
```

### Returning
Using the `return` keyword within the block of the classic ES1 for loop throws `Uncaught SyntaxError: Illegal return statement`.

### Breaking
The classic ES1 for loop can be halted using the `break` keyword.

---

## ES1 for...in Loop
The for...in loop was introduced in ES1.

### Syntax
The ES1 for...in loop is constructed through using the `for` keyword, a loop key variable name, the keyword `in` and the object reference.

```JavaScript
const captains = {
  picard: 'Enterprise',
  hook: 'Jolly Roger',
  blackbeard: 'Queen Anne\'s Revenge'
}

for (var captain in captains) {
  console.log(captain)
}  // picard hook blackbeard
```

### Usage
The ES1 for...in loop can be used to loop over object keys when the order of the keys is not important as the order is not guaranteed by the ES1 for...in loop.

### Returning
Using the `return` keyword within the block of the ES1 for...in loop throws `Uncaught SyntaxError: Illegal return statement`.

### Breaking
The ES1 for...in loop can be halted using the `break` keyword.

---

## ES5 forEach Loop
The `forEach` Array instance method was introduced in ES5.

### Syntax
The `forEach` method is being called on an array and iterates over the array values in ascendance order using a callback function which parameters are the currently iterated value, index and the array as a whole.

```JavaScript
const ships = ['Enterprise', 'Jolly Roger', 'Queen Anne\'s Revenge']

ships.forEach((ship, index, arr) => {
  console.log(ship, index, arr)
})
// Enterprise 0 (3) ['Enterprise', 'Jolly Roger', "Queen Anne's Revenge"]
// Jolly Roger 1 (3) ['Enterprise', 'Jolly Roger', "Queen Anne's Revenge"]
// Queen Anne's Revenge 2 (3) ['Enterprise', 'Jolly Roger', "Queen Anne's Revenge"]
```

### Usage
The ES5 `forEach` array method ensures that values are being iterated over in the order of the array numeric index. Therefore the ES5 `forEach` is suited to loop over an array as opposed to the ES1 `for...in` loop.

### Returning
It is allowed to explicitly return within the `forEach` callback function which transitions to the next loop iteration but does not stop the loop as a whole.

### Breaking
The way to break the `forEach` loop is to throw an exception. Using the `break` keyword is not allowed.

---

## ES6 for...of Loop
Incoming...

| **Method**           | **Description**                                                                 | **Example**                                                                 |
|-----------------------|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| `push()`             | Adds one or more elements to the end of an array and returns the new length.    | `let arr = [1, 2]; arr.push(3); // [1, 2, 3]`                              |
| `pop()`              | Removes the last element of an array and returns it.                            | `let arr = [1, 2, 3]; arr.pop(); // [1, 2]`                                |
| `unshift()`          | Adds one or more elements to the beginning of an array and returns the new length. | `let arr = [2, 3]; arr.unshift(1); // [1, 2, 3]`                          |
| `shift()`            | Removes the first element of an array and returns it.                           | `let arr = [1, 2, 3]; arr.shift(); // [2, 3]`                              |
| `concat()`           | Merges two or more arrays and returns a new array.                              | `let arr = [1, 2]; arr.concat([3, 4]); // [1, 2, 3, 4]`                   |
| `slice()`            | Returns a shallow copy of a portion of an array into a new array.               | `let arr = [1, 2, 3]; arr.slice(1, 3); // [2, 3]`                         |
| `splice()`           | Adds/removes elements to/from an array and returns the removed elements.        | `let arr = [1, 2, 3]; arr.splice(1, 1, 5); // [1, 5, 3]`                  |
| `indexOf()`          | Returns the first index of a specified element, or -1 if not found.             | `let arr = [1, 2, 3]; arr.indexOf(2); // 1`                               |
| `lastIndexOf()`      | Returns the last index of a specified element, or -1 if not found.              | `let arr = [1, 2, 2, 3]; arr.lastIndexOf(2); // 2`                        |
| `includes()`         | Checks if an array includes a specified value.                                  | `let arr = [1, 2, 3]; arr.includes(2); // true`                           |
| `find()`             | Returns the first element that satisfies a provided condition.                  | `let arr = [1, 2, 3]; arr.find(x => x > 1); // 2`                         |
| `findIndex()`        | Returns the index of the first element that satisfies a condition.              | `let arr = [1, 2, 3]; arr.findIndex(x => x > 1); // 1`                    |
| `forEach()`          | Executes a provided function once for each array element.                       | `[1, 2, 3].forEach(x => console.log(x)); // 1 2 3`                        |
| `map()`              | Creates a new array with the results of calling a function on every element.    | `[1, 2, 3].map(x => x * 2); // [2, 4, 6]`                                 |
| `filter()`           | Creates a new array with elements that pass a condition.                        | `[1, 2, 3].filter(x => x > 1); // [2, 3]`                                 |
| `reduce()`           | Reduces an array to a single value using a callback function.                   | `[1, 2, 3].reduce((sum, x) => sum + x, 0); // 6`                          |
| `reduceRight()`      | Same as `reduce()` but operates from right to left.                             | `[1, 2, 3].reduceRight((sum, x) => sum + x, 0); // 6`                     |
| `some()`             | Checks if at least one element satisfies a condition.                          | `[1, 2, 3].some(x => x > 2); // true`                                     |
| `every()`            | Checks if all elements satisfy a condition.                                    | `[1, 2, 3].every(x => x > 0); // true`                                    |
| `sort()`             | Sorts the elements of an array in place.                                        | `[3, 1, 2].sort(); // [1, 2, 3]`                                          |
| `reverse()`          | Reverses the order of elements in an array.                                     | `[1, 2, 3].reverse(); // [3, 2, 1]`                                       |
| `join()`             | Joins all elements of an array into a string.                                   | `[1, 2, 3].join('-'); // "1-2-3"`                                         |
| `toString()`         | Converts an array to a string.                                                  | `[1, 2, 3].toString(); // "1,2,3"`                                        |
| `flat()`             | Flattens nested arrays into a single array.                                     | `[1, [2, [3]]].flat(2); // [1, 2, 3]`                                     |
| `flatMap()`          | Maps and flattens an array in one step.                                         | `[1, 2].flatMap(x => [x, x * 2]); // [1, 2, 2, 4]`                        |
| `fill()`             | Fills all or part of an array with a static value.                              | `[1, 2, 3].fill(0, 1, 3); // [1, 0, 0]`                                   |
| `copyWithin()`       | Copies a part of an array to another location within the array.                 | `[1, 2, 3, 4].copyWithin(1, 2); // [1, 3, 4, 4]`                          |
| `Array.from()`       | Creates a new array from an array-like object or iterable.                      | `Array.from('abc'); // ['a', 'b', 'c']`                                   |
| `Array.isArray()`    | Checks if the value is an array.                                                | `Array.isArray([1, 2, 3]); // true`                                       |

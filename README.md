# Lecture4-April
# Homework
## _Array_

[![N|Solid](https://www.javascripttutorial.net/wp-content/uploads/2022/08/JavaScript-Array.svg)
    
### An array is an object that holds values (of any type) not particularly in named properties/keys, but rather in numerically indexed position In JavaScript, an array is an ordered list of values. Each value is called an element specified by an index. ... First, an array can hold values of mixed types.

## _Array methods_

- ## pop() 

- ## push()

- ## unshift()

- ## toString()

- ## splice()

- ## reverse()

- ## concat()
- ## join() 

- ## map()

- ## filter()
- ## find() 

- ## reduce()

- ## forEach()
- ##  sort() 

- ## indexOf()

- ## includes()
# Array methods
![The San Juan Mountains are beautiful!](https://i.ytimg.com/vi/OMoxLUxW7Wc/maxresdefault.jpg)
- ### `pop()`
> The `pop()` method removes the last element from an array and returns that element. This method changes the length of the array.
```
const plants = ['broccoli', 'cauliflower', 'cabbage', 'kale', 'tomato'];

console.log(plants.pop());
// Expected output: "tomato"
```

- ### `push()`
> The `push()` method adds one or more elements to the end of an array and returns the new length of the array.
```
const animals = ['pigs', 'goats', 'sheep'];

const count = animals.push('cows');
console.log(count);
// Expected output: 4
console.log(animals);
// Expected output: Array ["pigs", "goats", "sheep", "cows"]
```

- ### `unshift()`
>The `unshift()` method adds one or more elements to the beginning of an array and returns the new length of the array.
```
const array1 = [1, 2, 3];

console.log(array1.unshift(4, 5));
// Expected output: 5

console.log(array1);
// Expected output: Array [4, 5, 1, 2, 3]
```

- ### `toString()`
> The `toString()` method returns a string representing the specified array and its elements.
```
const array1 = [1, 2, 'a', '1a'];

console.log(array1.toString());
// Expected output: "1,2,a,1a"
```

- ### `splice()` 
>The `splice()` method changes the contents of an array by removing or replacing existing elements and/or adding new elements in place. To access part of an array without modifying it, see slice().
```
const months = ['Jan', 'March', 'April', 'June'];
months.splice(1, 0, 'Feb');
// Inserts at index 1
console.log(months);
// Expected output: Array ["Jan", "Feb", "March", "April", "June"]  
```

- ### `reverse()`
>The `reverse()` method reverses an array in place and returns the reference to the same array, the first array element now becoming the last, and the last array element becoming the first. In other words, elements order in the array will be turned towards the direction opposite to that previously stated.
```
const array1 = ['one', 'two', 'three'];
console.log('array1:', array1);
// Expected output: "array1:" Array ["one", "two", "three"]

const reversed = array1.reverse();
console.log('reversed:', reversed);
// Expected output: "reversed:" Array ["three", "two", "one"]
```


- ### `concat ()`
>The `concat()` method is used to merge two or more arrays. This method does not change the existing arrays, but instead returns a new array.
```
const array1 = ['a', 'b', 'c'];
const array2 = ['d', 'e', 'f'];
const array3 = array1.concat(array2);

console.log(array3);
// Expected output: Array ["a", "b", "c", "d", "e", "f"]
```


- ### `join()`
>The `join()` method creates and returns a new string by concatenating all of the elements in an array (or an array-like object), separated by commas or a specified separator string. If the array has only one item, then that item will be returned without using the separator.
```
const elements = ['Fire', 'Air', 'Water'];

console.log(elements.join());
// Expected output: "Fire,Air,Water"

console.log(elements.join(''));
// Expected output: "FireAirWater"

console.log(elements.join('-'));
// Expected output: "Fire-Air-Water"
```

- ### `map()`
>The `map()` method creates a new array populated with the results of calling a provided function on every element in the calling array.
```
const array1 = [1, 4, 9, 16];

// Pass a function to map
const map1 = array1.map(x => x * 2);

console.log(map1);
// Expected output: Array [2, 8, 18, 32]
```

- ### `filter()`
>The `filter()` method creates a shallow copy of a portion of a given array, filtered down to just the elements from the given array that pass the test implemented by the provided function.
```
const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];

const result = words.filter(word => word.length > 6);

console.log(result);
// Expected output: Array ["exuberant", "destruction", "present"]
```

- ### `find()`
>The `find()` method returns the first element in the provided array that satisfies the provided testing function. If no values satisfy the testing function, undefined is returned.
```
const array1 = [5, 12, 8, 130, 44];

const found = array1.find(element => element > 10);

console.log(found);
// Expected output: 12
```

- ### `reduce()`
>The `reduce()` method executes a user-supplied "reducer" callback function on each element of the array, in order, passing in the return value from the calculation on the preceding element. The final result of running the reducer across all elements of the array is a single value.
```
const array1 = [1, 2, 3, 4];

// 0 + 1 + 2 + 3 + 4
const initialValue = 0;
const sumWithInitial = array1.reduce(
  (accumulator, currentValue) => accumulator + currentValue,
  initialValue
);

console.log(sumWithInitial);
// Expected output: 10
```

- ### `forEach()`
>The `forEach()` method executes a provided function once for each array element.
```
const array1 = ['a', 'b', 'c'];

array1.forEach(element => console.log(element));

// Expected output: "a"
// Expected output: "b"
// Expected output: "c"
```
- ### `sort()`
>The sort() method sorts the elements of an array in place and returns the  reference to the same array, now sorted. The default sort order is ascending, built upon converting the elements into strings, then comparing their sequences of UTF-16 code units values.
```
const months = ['March', 'Jan', 'Feb', 'Dec'];
months.sort();
console.log(months);
// Expected output: Array ["Dec", "Feb", "Jan", "March"]

const array1 = [1, 30, 4, 21, 100000];
array1.sort();
console.log(array1);
// Expected output: Array [1, 100000, 21, 30, 4]
```

-  ### `indexOf()`
>The indexOf() method returns the first index at which a given element can be found in the array, or -1 if it is not present.
```
const beasts = ['ant', 'bison', 'camel', 'duck', 'bison'];

console.log(beasts.indexOf('bison'));
// Expected output: 1

// Start from index 2
console.log(beasts.indexOf('bison', 2));
// Expected output: 4
```

- ### `includes()`
>The `includes()` method determines whether an array includes a certain value among its entries, returning true or false as appropriate.
```
const array1 = [1, 2, 3];

console.log(array1.includes(2));
// Expected output: true

const pets = ['cat', 'dog', 'bat'];

console.log(pets.includes('cat'));
// Expected output: true
```

![The San Juan Mountains are beautiful!](data:image/jpeg;base64,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)


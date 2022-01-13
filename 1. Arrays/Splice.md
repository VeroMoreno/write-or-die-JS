# 🍕 Splice
- Removing and adding new elements in an array
- This method return the deleted elements

array.splice(start, deleteCount, item1, item2)

## Take care
- This array will be modified, because that, we need a copy before.

## Remove all elements starting at index 2
```js
const numbers = [1,2,3,4,5];
const del = numbers.splice(2); // del = [3,4,5]
console.log(numbers); // [1,2]
```

## Removes ONE ELEMENT at index 2
```js
const numbers = [1,2,3,4,5];
const del = numbers.splice(2, 1) // del = [3]
console.log(numbers); // [1, 2, 4, 5]
```

## Removes 3 elements starting at index 3
- As the index is negative (-2), what it does is put itself at index 3.
- The second element indicates how many elements to delete (3 in this case). Since it can only delete two (there are no more) it only deletes 4 and 5, which is what it returns
```js
const numbers = [1,2,3,4,5];
const del = numbers.splice(3, 3) // del = [4, 5]
console.log(numbers); // [1, 2, 3]
```

## Replaces 2 elements starting at index 2 by numbers 6 and 7
```js
const numbers = [1,2,3,4,5];
const del = numbers.splice(2, 2, 6, 7) // del = [3, 4]
console.log(numbers); // [1,2,6,7,5]
```

### Bonus
A slice before splice creates a copy, and thus the original object is not modified. Tadaaaa! 🎉🎉
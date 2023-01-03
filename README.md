# Welcome to Ultimate JavaScript Array Series.

## In JavaScript we can define array **two** way.

<br/>

> - Array Constructor.
> - Array Literal.

<br />

### *Both* are syntactically different.

<br />

Array constructor
``` Javascript
const method1 = new Array(1, 2, 3);
```

Array literal
``` Javascript
const method2 = [4, 5, 6];
```


The array is a very often used data type in JavaScript.


An array can be used for a variety of activities to easily store and access values.

You may use arrays for a variety of activities, such as the following:

- Adding components
- Element removal
- Elements being sorted
- Changing components
- Elements that loop
- Elements being copied
- And a whole lot more.

There are several useful built-in methods included with the Array data structure.

Without wasting time on re-inventing the wheel, you can do the most frequent tasks using these methods.


</br>
</br>

There are two categories of methods in JavaScript:

- **Static methods**. These are called in the class itself.
- **Instance methods**. These are called on the class instance.


The overall number of array methods includes **34** instance array methods and **3** static array methods.

</br>

# Instance Methods


- [Array.prototype.at()](#01)
- [Array.prototype.concat()](#02)
- [Array.prototype.copyWithin()](#03)
- [Array.prototype.entries()](#04)
- [Array.prototype.every()](#05)
- [Array.prototype.fill()](#06)
- [Array.prototype.filter()](#07)
- [Array.prototype.find()](#08)
- [Array.prototype.findIndex()](#09)
- [Array.prototype.findLast()](#10)
- [Array.prototype.findLastIndex()](#11)
- [Array.prototype.flat()](#12)
- [Array.prototype.flatMap()](#13)
- [Array.prototype.forEach()](#14)
- [Array.prototype.includes()](#15)
- [Array.prototype.indesOf()](#16)
- [Array.prototype.join()](#17)
- [Array.prototype.keys()](#18)
- [Array.prototype.lastIndexOf()](#19)
- [Array.prototype.map()](#20)
- [Array.prototype.pop()](#21)
- [Array.prototype.push()](#22)
- [Array.prototype.reduce()](#23)
- [Array.prototype.reduceRight()](#24)
- [Array.prototype.reverse()](#25)
- [Array.prototype.shift()](#26)
- [Array.prototype.slice()](#27)
- [Array.prototype.some()](#28)
- [Array.prototype.sort()](#29)
- [Array.prototype.splice()](#30)
- [Array.prototype.toLocalString()](#31)
- [Array.prototype.toString()](#32)
- [Array.prototype.unshift()](#33)
- [Array.prototype.values()](#34)

<br/>
<br/>


# Static Method
- [Array.form()](#35)
- [Array.isArray()](#36)
- [Array.of()](#37)

<br>

<!-- Array.prototype.at()  -->

### 01
# Array.at()

The at() method takes an integer and returns the item at that index.

<br>

> #### Use case !
> - It works the same way as the square bracket accessing operator
**(e.g. myArr[OI = myArr.at(O))**
> - You can use at() method both positive or negative 
> - This at() method is new JavaScript Features in **ES2022**


<br>
Syntax

``` javascript 
array.at(index)
```

<br />

Example 
``` javascript
const friends = ['Tomal', 'Alex', 'Smith'];
console.log(friends.at(0));

const role = 2;
console.log(`${friends.at(role)} role was ${role} class three`);

// Smith role was 2 class three
```

The at() method is really useful when you want to access the index elements of an array.

<br />

<!-- Array.prototype.concat()  -->

### 02
# Array.concat()

In JavaScript, you can call concat() method on an array to merge one or more arrays into it

<br>

> #### Use case !
> - This method does not modify the original array. Instead,
it creates a new array.
> - It's merge an array with another array.
> - This concat() method is an **ES1** **(JavaScript 1997)** Feature.


It's a very old feature.



<br>
Syntax

``` javascript 
array.concat(other, other1, other2)
```

<br />

Example 01
``` javascript
const arr = ['one', 'two', 'three'];
const arr1 = ['four', 'five', 'six'];
const arr2 = ['seven', 'eight', 'nine'];

// ES1
const margeArray = arr.concat(arr1, arr2);
console.log(arr, arr1, arr2)

// ES6 You can use spread operator
const spread = [...arr, ...arr1, ...arr2 ]

console.log(margeArray);

// ['one', 'two', 'three', 'four', 'five', 'six', 'seven', 'eight', 'nine']
```

Example 02

```javascript
const languages1 = ["JavaScript", "Python", "Java"];
const languages2 = ["C", "C++"];

// concatenating two arrays
const new_arr = languages1.concat(languages2);
console.log(new_arr); 
// [ 'JavaScript', 'Python', 'Java', 'C', 'C++' ]

// concatenating a value and array
const new_arr1 = languages2.concat("Lua", languages1);
console.log(new_arr1); 

// [ 'C', 'C++', 'Lua', 'JavaScript', 'Python', 'Java' ]
```

The concat() method is really useful when you want to combine multiple array.

<br>


<!-- Array.prototype.copyWithin()  -->

### 03
# Array.copyWithin()

The copyWithin() method copies array elements from one position to another in the given array.

<br />

> #### Use case !
> - Copies a part of an array. Take integer value. 
> - Puts the part into another position in the same array. 
> - Returns the array without changing its length.
> - The copyWithin method is an ES6 feature.

<br>
Syntax

``` javascript 
array.copyWithin(index, start, end)
```

Example 1
``` javascript

const arr = ['one', 'two', 'three', 'four', 'five'];
// arr.copyWithin(); // Shallow copy
// Modify your array
// Can not modify arr length
console.log(arr.copyWithin(0, 1, 3));
console.log(arr.copyWithin(1, 3));
console.log(arr.copyWithin(-1, 3));
console.log(arr.copyWithin(3));

console.log(arr);

// [ 'two', 'three', 'three', 'four', 'five' ]
// [ 'two', 'four', 'five', 'four', 'five' ]
// [ 'two', 'four', 'five', 'four', 'four' ]
// [ 'two', 'four', 'five', 'two', 'four' ]
// [ 'two', 'four', 'five', 'two', 'four' ]
```

Example 2

```javascript
let laptops = ["dell", "hp", "acer", "asus"];

// copying elements from index 2 to 4(excluding 4) to index 0
laptops.copyWithin(0, 2, 4);

// modifies the original array
console.log(laptops); // [ 'acer', 'asus', 'acer', 'asus' ]
```

The copyWithin() method change your main array but your length won't be change.


<br />

<!-- Array.prototype.entries()  -->

### 04
# Array.entries()

The entries method, return and iterator that consists of key value pairs from the array elements.

<br />

> #### Use case !
> - The entries method, return and iterator  that consists of key value pairs from the array elements. 
> - The enters method does not change the original array 
> - The enters() method is an **ES6** feature.

<br />

Syntax

``` javascript 
array.entries() // Empty slot
```

<br />

Example
``` javascript
const cities = ['New York', 'London', 'Sydney'];

const city = cities.entries();
console.log(city.next().value);
console.log(city.next().value);
console.log(city.next().value);

for (let city of cities.entries()){
    console.log(city[1])
}

for (let [i, e] of cities.entries()){
    console.log(i, e)
}
```

The entries() method is a iterator method you can use next() function iterate every single element.

<br />

<!-- Array.prototype.every()  -->

### 05
# Array.every()

If the function returns true for all elements, the every() method returns true. If the function returns false for one element, the every() method returns false.

<br />

> #### Use case !
> - Array.every() method return boolean value.
> - The every() method is an iterative method.
> - For empty elements, the every() method does not run the code
> - Every() is an ECMAScript5 (ES5) feature that preserves the original array's structure.

<br />

Syntax

``` javascript 
array.every( callback(), thisArg)
```

<br />

Example
``` javascript
const number = [33, 34, 47, 80, 99];
const result = number.every(n => n < 100);

console.log(result); // true

// even number
const arr = [12, 22, 34, 44, 48, 98] 

function isEven (element, index, array) {
    return element % 2 === 0;
}

const output = arr.every((ele, idx, arr) => ele % 2 === 0);
console.log(output); // true
```

The every() method take callback function.


<!-- Array.prototype.every()  -->

### 06
# Array.fill()

The fill() method replaces array elements with static values starting from a specific index.

<br />

> #### Use case !
> - The fill() method replaces array elements with static values starting from a specific index.
> - The fill() method overwrites the original array.
> - ECMAScript6 or (ES6) introduces the fill() function.

<br/>

Syntax

``` javascript 
array.fill(value, start, end)
```

<br />

Example
``` javascript
// it's count length
const num = [1, 2, 3]; 
 
console.log(num.fill(10)) // [10, 10, 10]
console.log(num.fill(20, 1, 2)) // [10, 20, 10]
console.log(num.fill(20, 0, 3)) // [20, 20, 20]

const car = ['Tesla', 'BMW', 'Toyota']; 
console.log(car.fill('Rolls Royce', 0, 3));

console.log(car); 
// [ 'Rolls Royce', 'Rolls Royce', 'Rolls Royce' ]
```

The fill() method muted your original array.


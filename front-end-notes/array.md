
## Array
An array is a special variable that stores a list of __values__. </br>
You can create an array using two different techniques. The most preferred method is known as an __array literal__. It is written as a list of values between square brackets, separated by commas. </br>
```
var fruits = ["Apple", "Banana", "Orange"];
```
The other method is known as an __array constructor__. </br>
```
var fruits = new Array("Apple", "Banana", "Orange");
```
</br>
Remember, _the array literal is most preferred over the array constructor._
</br>

Consider using an array whenever you are working with a __list__ or a set of values that are __related__ to each other. </br>
Arrays are especially helpful when you do not know _how many items a list will contain_ because, when you create the array, _you do not need to specify how many values it will hold._</br>
If you do not know how many items a list will contain, rather than creating enough variables for a long list (when you might only use a small percentage of them), using an array is considered a better solution. </br>
For example, an array can be suited to storing the individual items on a shopping list because it is a list of related items. Additionally, each time you write a new shopping list, the number of items may differ. </br>
## Values in Arrays
Values in an array are accessed as if they are in a numbered list. It is important to know that the numbering of this list __starts__ at _zero_ and *not one*.
Each item in an array is automatically given a number called an __index__.
This can be used to access specific items in the array. 
Example:
```
var fruits = ["Apple", "Banana", "Orange"];
```
 INDEX | VALUE
---------- | -----------
          0 | Apple
          1 | Banana
          2 | Orange
To retrieve the third item on the list, the array name is specified along with the index number in square brackets. 
Example:
```
var itemThree = fruits[2];
```
Each array has a property called __length__, which holds the number of items in the array. Below you can see the variable `numFruits` is declared. Its value is set to be the number of items in the array. 
```
var numFruits = fruits.length
// 3
```

### Create an Array
```
var fruits = ["Apple", "Banana"];

console.log(fruits.length);
// 2
```

### Access an Array Item
```
fruits[0];
// Apple

```

###Loop an Array
```
fruits.forEach(function (item, index, array) {
  console.log(item, index);
});
// Apple 0
// Banana 1
```
### Add to the end of an Array
You can add one or more elements to the end of an array using the keyword push.
```
fruits.push("Orange");
// ["Apple", "Banana", "Orange"]
```
You can also append an array item using:
```
fruits[fruits.length] = "pineapple"
```
### Remove from the end of an Array
You can remove the last element of an array by using the keyword pop.
```
fruits.pop(); // remove Orange (from the end)
// ["Apple", "Banana"];
```
### Remove from the front of an Array
You can remove the first element at the beginning of the array using the keyword shift.
```
fruits.shift(); // remove Apple from the front
// ["Banana"];
```
### Add to the front of an Array
You can add one or more elements to the beginning of the array using the keyword unshift.
```
fruits.unshift("Strawberry") // add to the front
// ["Strawberry", "Banana"];
```
### Find the index of an item in the Array
To find the index number of an item in an array.
```
var pos = fruits.indexOf("Banana");
// 1
```
### Remove an item by Index Position
To add one or more elements at any location in the array use the splice method.  When using splice you also have the option to remove elements at the same time. </br>
```
var fruits = [“apples”, “bananas”, “oranges”, “grapes”];
```
```
fruits.splice(1, 2, “lemons”, “grapefruit”);
```
The first number, 1, is the index position where you want to start adding. (Remember an array index starts at 0!)</br>
The second number, 2, is the number of elements you want to remove.</br>
 The resulting array will be </br>
```
[“apples”, “lemons”, “grapefruit”, “grapes”];
```
</br>
 To add elements without removing any: </br>
```
fruits.splice(1, 0, “lemons”, “grapefruit”);
```
</br>
 To only remove elements:</br>
```
fruits.splice(1, 2);
```

### Copy an Array
You can create a new array by copying one or more consecutive elements from an existing array by using the slice method. </br>
Using slice will not change the original array.

```
var fruits = [“apples”, “bananas”, “oranges”, “grapes”];
var myFruit = fruit.slice(1, 3);
```
</br>
myFruit now contains the elements</br>

```
myFruit = [“bananas”, “oranges”];
```
The first number, 1, is the index number you want to copy.  The second number, 3, is the number AFTER the last element you want to copy.

### Other Methods
There are a number of other methods to use with an array. Google is your friend! Also, see Sources and Further Reading for more material on arrays.

## Sources and Further Reading
* http://eloquentjavascript.net/04_data.html
* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array
* Javascript & jQuery - Jon Duckett
* A Smarter Way to Learn Javascript - Mark Myers

# Array

### Create an Array
```
var fruits = ["Apple", "Banana"];
```
### Get Length of the array
```
console.log(fruits.length);
```
### Get last element in an array
```
var last = fruits[fruits.length - 1];
```
### Add to the end of an Array
```
fruits.push("Orange"); // adds and returns item to the end of the array
```
### add to the front
```
fruits.unshift("Strawberry") // adds and returns item to the beginning of the array
```
## Remove from the end of an Array
```
fruits.pop(); // removes and returns last item in the array
```
### Remove from the front of an Array
```
fruits.shift(); // removes and returns first item in the array
```
### Remove an item by Index Position
```
fruits.splice(pos, 1);
```
### Copy an Array
```
var shallowCopy = fruits.slice(); // this is how to make a copy
```
### indexOf
```
var arr = ['apple', 'orange', 'pear'];
console.log("found orange", arr.indexOf("orange") != -1, "at index of ", arr.indexOf("orange"));
```
### filter
```
var arr = [
    { "name": "apple", "count": 2 },
    { "name": "orange", "count": 5 },
    { "name": "pear", "count": 3 },
    { "name": "orange", "count": 16 },
];

var newArr = arr.filter(function(item) {
    return item.name === "orange";
});

console.log("Filter results:", newArr);
```
### map
```
var oldArr = [
    { first_name: "Colin", last_name: "Toh" },
    { first_name: "Addy", last_name: "Osmani" },
    { first_name: "Yehuda", last_name: "Katz" }
];

var newArr = oldArr.map(function(item, index) {
    item.full_name = [item.first_name, item.last_name].join(" ");
    return item;
});

console.log("newArr", newArr);
```
## loops

### forEach
```
var arr = [1, 2, 3, 4, 5, 6, 7, 8];
arr.forEach(function(item, index) {
    console.log("forEach", item);
});
```
### ES6 forEach
```
var arr = [1, 2, 3, 4, 5, 6, 7, 8];
arr.forEach(item => console.log("ES6 forEach", item))
```
### for increment
```
var arr = [1, 2, 3, 4, 5, 6, 7, 8];
for (var i = 0; i < arr.length; i++) {
    console.log("for loop increment ",arr[i]);
}
```
### for decrement
```
var arr = [1, 2, 3, 4, 5, 6, 7, 8];
for (var i = arr.length - 1; i >= 0; i--) {
    console.log("for loop decrement ",arr[i]);
}
```
### find
```
var arr = [
    {
        type: 'apple',
        color: 'green'

    },
    {
        type: 'orange',
        color: 'orange'
    }
];
var find = 'apple';
var result = arr.find(function (fruit) {
    return fruit.type === find;
})
console.log("result",result);
```

### find ES6
```
var arr = [
    {
        type: 'apple',
        color: 'green'

    },
    {
        type: 'orange',
        color: 'orange'
    }
];

var find = 'apple';
var result = arr.find(fruit => fruit.type === find)
console.log("arr",result)

```
## concat
var arr1 = ["1","2"];
var arr2 = ["3","4"];
var arr3 = arr1.concat(arr2);
console.log("arr3",arr3)
### ES6 spread operator
```
var arr = ["apple","orange","apple","orange","pear","orange"];
console.log("my favorite fruit are ", ...arr)
```

### ES6 rest operator
```
var first = {
    "mango": {
        "taste": "good"
    }
}
var obj = {
    "apple": {
        "taste": "good"
    },
    "orange": {
        "taste": "fair"
    },
    "pear": {
        "taste": "bad"
    },
    "apple": {
        "taste": "excellent"
    }
};

function getObject (first, ...value) {
    return value;
}

var objectContents = getObject(first, obj);

console.log("objectContents",objectContents)
```

# Object

## for in
```
var obj = {a:1, b:2, c:3};

for (var prop in obj) {
  console.log("obj." + prop + " = " + obj[prop]);
}
```
## get length of object
```
var obj = {
    "apple": {
        "taste": "good"
    },
    "orange": {
        "taste": "fair"
    },
    "pear": {
        "taste": "bad"
    },
    "apple": {
        "taste": "excellent"
    }
};
var objLength = Object.keys(obj).length + 1;
console.log("objLength",objLength);
```

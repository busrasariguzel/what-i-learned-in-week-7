# `What I Learned In Week 7`



## For Loops vs While Loops
``` 
const numbers = [1,3,5,7,9]
let i = 0
while (i< numbers.length){
    console.log(numbers [i] + 2)
    i ++
}

for (let i = 0; i < numbers.length ; i++){
    console.log(numbers[i] + 2);

}
```

## `String Building`

* We cannot change an already existing string. However, we can create a new one with string building method. Some examples include :
  

```
function crazyCase2ReturnOfCrazyCase(str) {
let newStr= ''
let counter = 0;
str = str.toLowerCase();

  for (let i = 0; i < str.length; i++) {
  if (counter % 2 === 0) {
  newStr = newStr + str[i].toLowerCase()
  
  } else {
  newStr = newStr + str[i].toUpperCase()
  }
  if (str[i] !==  ' ') {
    counter++;
  }
  }
  return newStr
}
```

```
function crazyCase3SonOfCrazyCase(str) {
  let newStr = '';
  let counter = 0;
  str = str.toLowerCase();
  for (let i = 0; i < str.length; i++) {
    if(str[i] ===  ' ') {
      newStr = newStr + ' '
      counter++;
    }
    else if ('0123456789!@#$.,()'.includes(str[i])) {
      newStr = newStr + str[i]
      counter++;
    }
    else if(counter % 2 === 0) {
      newStr = newStr + str[i];
    }
    else {
      newStr = newStr + str[i].toUpperCase();
    }counter++
  }
  return newStr;
}
```

## `Array Building`

* Just like strings, we cannot mutate arrays. Instead, we build new arrays as follows:

```
function add1ToLeft(arr) {
  const newArr = [];
  for(let i = 0; i < arr.length; i++){
    if (arr[i] > 0){
      newArr.push(Number('1' + arr[i]))
    } else if (arr[i] < 0){
      newArr.push(Number('-1' + arr[i]*-1))
    }
  }
return newArr
}
```
```
function doubleOdd(arr) {
  const newArr = [];
  for(let i=0; i < arr.length; i++){
    if (arr[i] % 2 === 1){
    newArr.push(arr[i] * 2)}
    else if (arr[i] < 0 && arr[i]*-1 % 2 ===1){
    newArr.push(arr[i] * 2)
    }
    else { 
      newArr.push(arr[i])}
      }
  return newArr
}
```



## `Dot Chaining`

By using dot chaining, we do not change the original  arrays.We build a new one with the changes we make. Some methods include :

`slice()` - 
name.slice(3) from index 3 to the end.
name.slice(3,8) from index 3 to 8, exclusive.

`repeat()`
name.repeat(n) - repeats n times

`startsWith()`
name.startsWIth('hello') - false

`endsWith()`
name.endsWith('hello')- false
name.endsWith('sra')-  true

`trimStart()` - removes space from the start.

`trim()` removes space rom start and end.

`trimEnd()` removes space from the end.

`includes()` name.includes('aeiou')

`join()` - for array of strings, joints string in array and they become one string.
name.join('and) - puts "and" between items and makes it a one string. Joins items with whats inside of the parenthesis. 

`split()`







# **WHAT I LEARNED IN  WEEK 7** 
___

## `cripples-bastards-and-broken-things`

Useful activity which required us to fix broken code. The assignment consisted of many past assignments.

```javascript
function crazyCase(str) {
  let crazyCased = '';

  for (let i = 0; i < str.length; i++) {
    if (i % 2 === 0) {
      crazyCased = crazyCased + str[i].toLowerCase()
    } else {
      crazyCased = crazyCased + str[i].toUpperCase()
    }
  }

  return crazyCased;
}

function ciEmailify(name) {
  let email = '';
  for (let i = 0; i < name.length; i++) {
    if (name[i] === ' ') {
      email = email + '.';
    } else {
      email = email + name[i].toLowerCase() ;
    }
  }

  return email + '@codeimmersives.com';
}

function exclaim(sentence) {
  let exclaimed = '';

  for (let i = 0; i < sentence.length; i++) {
    const character = sentence[i];
    if (character === '?' || character === '.') {
      exclaimed = exclaimed + '!';
    } else {
      exclaimed = exclaimed + character;
    }
  }
  return exclaimed;

}

function reverse(str) {
  let reversed = '';

  for (let i = str.length-1; i >= 0; i--) {
    reversed = reversed + str[i];
  }

  return reversed ;
}

function crazyCase2ReturnOfCrazyCase(str) {
  let crazyCased = '';
  let crazyIndex = 0;
  
  for (let i = 0; i < str.length; i++) {
    if (str[i] !== ' ') {
      if (crazyIndex % 2 === 0) {
        crazyCased = crazyCased + str[i].toLowerCase()
      } else {
        crazyCased = crazyCased + str[i].toUpperCase()
      }

      crazyIndex++;
    } else {
      crazyCased = crazyCased + ' ';
    }
  }
  
  return crazyCased;
}

```

## `Methods to my madness`

Went under the hood with this one. Rewrote methods by writing them as functions.



```javascript
function slice(string, start = 0, end = string.length) {
  let newStr = ''
  for (let i=start; i<end; i++) {
    newStr = newStr + string[i]
  }
  return newStr
  }


function repeat(str, repetitions) {
  let newStr = ''
  for (let i=0; i<repetitions; i++) {
    newStr =  newStr + str
  }
  return newStr
}

function startsWith(str, substring) {
  for (let i=0; i<substring.length; i++) {
    if(str[i]!==substring[i]) {
      return false
    } 
    } return true
  }



function endsWith(str, substring) {
  for (let i=0; i<str.length; i++) {
    return  str[str.length -1].includes(substring[substring.length-1])
  }
}

function includes(arr, item) {
  for (let i=0;i<arr.length;i++) {
    if (arr[i]===item) {
      return true
    }
  }
  return false 
}

const arr = [3, 6, 9];
includes(arr, 6);

function join(arr, separator = '') {
  let newStr =''
  for(let i=0; i <arr.length; i++){
    if(i=== arr.length-1){
    newStr =newStr + arr[i]}
    else{
    newStr =newStr + arr[i] + separator}
}
return newStr
}

```
## `mapmaker-mapmaker`

changeToInitials and add1ToLeft were the most difficult. Worth redoing this activity for extra practice.


```javascript
function doubleAll(arr) {
  const newArr = []
  for (i=0;i<arr.length;i++) {
    newArr.push(arr[i] * 2)
  }
  return newArr
}

function absoluteValues(arr) {
  const newArr = []
  for (i=0;i<arr.length;i++) {
    if (arr[i]>0 || arr[i]===0) {
    newArr.push(arr[i])
  } else {
    newArr.push(-1*arr[i])
  }
  }
  return newArr
}

function yelledGreetings(arr) {
  const newArr = []
  for (i=0;i<arr.length;i++) {
    newArr.push(arr[i]+'!')
  }
  return newArr
}


// let arr = ['Jim Smith','Mark Jones']
// following function outputs [ 'J', 'S', 'M', 'J' ] 
// and not sure how to join them 

// function changeToInitials(arr) {
//   const newArr = []
//   for (i=0;i<arr.length;i++) {
//     for(j=0;j<arr[i].length;j++){
//     if( j === 0){
//       //console.log(arr[i].length)
//       newArr.push(arr[i][j])
//     } else if (arr[i][j] === ' ') {
//       newArr.push(arr[i][j+1])
//     }
//   }
//   }
//   return newArr
//  }
//  changeToInitials(arr)

function changeToInitials(arr) {
  const newArr = [];
  for (let i = 0; i < arr.length; i++){
    let component = arr[i];
    let newStr = '';
    for (let i = 0; i < component.length; i++){
    if (i===0 || component[i-1] === ' '){
      newStr = newStr + component[i];
    }
  }newArr.push(newStr)
  }return newArr
}


function doubleOdd(arr) {
  const newArr = []
  for (let i=0;i<arr.length;i++) {
    if (arr[i] % 2 === 1 || arr[i] % 2 === -1){
    newArr.push(arr[i] * 2)
  } else {
    newArr.push(arr[i])
  }
}
return newArr
}


function upperCaseFirstLetters(arr) {
  const newArr = [];
  for (let i = 0; i < arr.length; i++){
    let component = arr[i];
    let newStr = '';
    for (let i = 0; i < component.length; i++){
    if (i===0){
      newStr = newStr + component[i].toUpperCase();
    } else {
      newStr = newStr + component[i].toLowerCase();
    }
  }newArr.push(newStr)
  }return newArr
}

function add1ToLeft(arr) {
  const newArr = [];

  for(let i = 0; i < arr.length; i++) {
    if(arr[i] < 0) {
    newArr.push(Number(`1${arr[i] * -1}` * -1))
  } else if (arr[i] >= 0) {
    newArr.push(Number(`1${arr[i]}`))
    }
  }
  return newArr;
}

```
## `String Theory`

This assignment was difficult as the challenges required a lot of thinking. All the functions took in strings. 


```javascript
function crazyCase(str) {

  let newStr= ''
  for (i=0;i<str.length;i++) {
    if (i % 2 ===0) {
    newStr = newStr + str[i].toLowerCase()
    } else {
    newStr = newStr + str[i].toUpperCase()
    }
  } 
  return newStr
}

const nextCrazyCase = crazyCase('hello')
console.log(nextCrazyCase);

const theNextCrazyCase = crazyCase('you')
console.log(theNextCrazyCase);

function ciEmailify(str) {
  let newStr= ''
  str = str.toLowerCase()
  for (i=0; i<str.length; i++) {
    if (str[i] === " ") {
      newStr = newStr + '.'
    } else {
      newStr = newStr + str[i]
    }
    }
  return newStr + '@codeimmersives.com'
  }



function exclaim(str) {
  let newStr= ''
  for (i=0;i<str.length;i++) {
    if (str[i]==='?') {
      newStr = newStr + '!'
    } else if (str[i]==='.') {
      newStr = newStr + '!'
    } else {
      newStr = newStr + str[i]
    }
  } 
  return newStr
}



function reverse(str) {
  let newStr= ''
  for (i=str.length-1;i>-1;i--) {
    newStr = newStr + str[i]
  }
  return newStr
}

// function crazyCase2ReturnOfCrazyCase(str) {

//   let newStr= ''
//   str = str.toLowerCase()
//   let counter = 0
//   for (i=0;i<counter.length;i++) {
//     if (str[i] ===" ") {
//     newStr = newStr + " "
//     } else if (i % 2 ===0) {
//     newStr = newStr + str[i].toLowerCase()
//     } else {
//     newStr = newStr + str[i].toUpperCase()
//     } 
//   } 
//   return newStr
// }

// console.log(crazyCase2ReturnOfCrazyCase("multiple words here"))

function crazyCase2ReturnOfCrazyCase(str) {
  let newStr = '';
  let counter = 0;
  str = str.toLowerCase();

  for (let i = 0; i < str.length; i++) {
    if(counter % 2 === 0) {
      newStr = newStr + str[i];
    } else {
      newStr = newStr + str[i].toUpperCase();
    }

    if(str[i] !==  ' ') {
      counter++;
    }
  }
  return newStr;
}

function titleCase(str) {
  let newStr= ''
  for (i=0;i<str.length;i++){
  if(i == 0){
    newStr = newStr + str[0].toUpperCase()
  }else{
  if (str[i-1] === ' ') {
  newStr = newStr + str[i].toUpperCase()}
  else {
  newStr = newStr + str[i].toLowerCase()
    }
    }
  }
    return newStr;
  }

  // function onlyVowels(str) {
  //   let newStr=''
  //   for (i=0;i<str.length;i++){
  //     if (str[i] === 'a' || str[i] === 'e' || str[i] === 'i' || str[i] === 'o' || str[i] === 'u') {
  //       newStr = newStr + str[i]
  //     }
  //     else if (str[i] === 'A' || str[i] === 'E' || str[i] === 'I' || str[i] === 'O' || str[i] === 'U') {
  //       newStr = newStr + str[i]
  //     }
  //   }
  //   return newStr
  // }

  function onlyVowels(str) {
    let newStr=''
    for (i=0;i<str.length;i++){
      if ('aeiouAEIOU'.includes(str[i])) {
        newStr = newStr + str[i]
      }
    }
    return newStr
  }

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

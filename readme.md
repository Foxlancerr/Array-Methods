# Arrays Methods

- slice
- splice
- reverse
- concate
- split
- jion

## slice in arrays

- The slice operater give new array and not modify the original arrays.
- it passes two arguments start,end.

  syntex is

```js
array.slice(2, 8);
```

#### Example

```js
let arrSlice = [12, 33, 34, 54, 45, 77, 35, 89];
let slice = arrSlice.slice(1, 2);
console.log(arr);
console.log(slice);
```

## splice in arrays

- The splice operater give new array and also modify the original arrays.
- it passes two arguments start,end.
- it is differ only because it modify the origanal arrays also

syntex is

```js
array.splice(4, 8);
```

#### example

```js
let arrSplice = [12, 33, 34, 54, 45, 77, 35, 89];
console.log(arrSplice.length);
let splice = arrSplice.splice(0, 7);
console.log(arrSplice);
console.log(arrSplice.length);
console.log(splice);
```

## reverse in arrays

- The reverse method give the array but in reverse in order and also modify the original arrays.
- it passes no arguments.
  syntex is

```js
array.reverse();
```

#### example

```js
let arrReverse = [12, 33, 34, 54, 45, 77, 35, 89];
console.log(arrReverse.length);
console.log(arrReverse);
let reverrse = arrReverse.reverse();
console.log(arrReverse.length);
console.log(reverrse);
console.log(arrReverse);
```

//---------------- how to combine two arrays--------------

//--> concate in arrays

/_
The conate method combine the two arrays and not modify the original arrays.
syntex is arr1.concat(arr2);
example are mention below
_/

let arrConcat1 = [12, 33, 34, 54, 45, 77, 35, 89];
let arrConcat2 = [2, 73, 84, 70, 35, 9];
console.log(arrConcat1);
console.log(arrConcat2);
let concate = arrConcat1.concat(arrConcat2);
console.log(concate);
console.log(arrConcat1);
console.log(arrConcat2);

//--> split method in arrays

/_
The split method is also used to combine the two arrays and not modify the original arrays.
syntex is let arr3 = [...arr1,...arr2];
example are mention below
_/

let arrSplit1 = [12, 33, 34, 54, 45, 77, 35, 89];
let arrSplit2 = [2, 73, 84, 70, 35, 9];
console.log(arrSplit1);
console.log(arrSplit2);
let splitt = [...arrSplit1, ...arrSplit2];
console.log(splitt);
console.log(arrSplit1);
console.log(arrSplit2);

//--> jion method in arrays

/_
The jion method is used to all data which is presented in
arrays to convert into a single index.
by default is passes commas (,)in its arguments
syntex is arr.jion();
example are mention below
_/

//for a number-------

let arr1 = [12, 33, 34, 54, 45, 77, 35, 89];
console.log(arr1);
console.log(arr1.join("-"));
console.log(arr1.join());
console.log(arr1.join(" "));

//for a string-------

let arr2 = ["a", "b", "c", "d", "e"];
console.log(arr2);
console.log(arr2.join("-"));
console.log(arr2.join());
console.log(arr2.join(" "));

//\***\*\_\_\_**\*\*\***\*\*\***\* lecture one is completed now **\*\*\*\***\*\*\*\***\_\_**\*\*\*\*

//\***\*\_\_\_**\*\*\***\*\*\***\* lecture two is completed now **\*\*\*\***\*\*\*\***\_\_**\*\*\*\*

/\*

forEach function in javascript

foreach work same as looping but its easeir way to loop a code.
foreach have a higher precendence function because it have passing
function as arguments the function which it have passed three more
arguments the 1st one is essentiol but the two other is for your choice.

syntex is forEach(function(elem, index ,array){
your code is here............
............................
})

the elem store every value of the array when it runs.
the index store every index No. of the array when it runs.
the array store the array which will be for looping.

the example are mention it.
\*/

let arr = [23, 45, 56, 78, 75, 47, 90]
arr.forEach(function (elem, index, array) {
console.log("the students marks of paper " + index + " is " + elem);
});

/_using for loop to calculate students marks ,its percentage
and decide that the students is fail or pass.
_/

//students record store in the arrays
let students = [
{ name: 'ali', class: '4rd', marks: [95, 97, 78, 90, 80] },
{ name: 'sudais', class: '2nd', marks: [65, 47, 88, 67, 40] },
{ name: 'ahmad', class: '9th', marks: [25, 77, 38, 40, 20] },
{ name: 'ishfaq', class: '11th', marks: [35, 37, 88, 70, 60] },
];

let maxMark = 500;

//total marks function
function totalMarks(marksArr) {
// console.log(marksArr);
let total = 0;
for (let mark of marksArr) {
total += mark;
}
return total;
}

//get result functon is here.
function getresult(stdArrays) {

    //forEach loap is used
    stdArrays.forEach(function (elem) {
        let eachStu = elem;
        //totalMarks function called
        let totaled = totalMarks(elem.marks);

        // percentag is calculated here
        let percentage = ((totaled / maxMark) * 100).toFixed(0) + "%";

        //check condition is a students pass or fail
        let ispass = percentage >= '45' ? "The student is pass" : "the students is fail";

        //log a result in devolper console
        console.log(eachStu);
        console.log(totaled);
        console.log(percentage);
        console.log(ispass);
    });

}

//getResult function is calling
getresult(students)

//\***\*\_\_\_**\*\*\***\*\*\***\* lecture two is completed now **\*\*\*\***\*\*\*\***\_**\*\*\*\*

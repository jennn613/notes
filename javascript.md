# Javascript



```javascript
'use strict';
console.log('Hello, World!');
```



------



## Variable



Javascript는 dynamic typing (할당 된 값에 따라 타입이 변경되는) 언어이다



### let

let을 이용한 변수 선언 (값 변경 가능, mutable)

```javascript
let name = 'jenny';
let a = 8;

{ let name = 'jenny';
console.log(name);} 
// {} 안에 쓰면 지역 변수
// var hoisting > 선언 위치에 상관없이 항상 제일 위로 선언을 끌어올려주는 것.
// var은 block scope 불가능. 이제는 사용X
```



### const

const 를 이용한 변수 선언. (값 변경 불가, immutable) 

안전하고, 실수를 줄일 수 있음.

```javascript
const dayInWeek = 7;
```



### boolean

false 일 때 0, null, undefined, NaN, ' ' 출력

null은 아무 것도 없는 텅 빈 상태, undefined는 정의가 되지 않은 상태

```javascript
const math 3<1; // false
const test = true;
console.log(`value: ${test}`); // true
```



### symbol

```javascript
const symbol1= Symbol('id');
const symbol2= Symbol('id');
// 이 둘의 symbol은 각각 다름. symbol은 고유한 식별자
// 같은 symbol을 사용하고 싶다면
const symbol1 = Symbol.for('id');
const symbol2 = Symbol.for('id');
console.log('value: ${symbol.description}');
// symbol은 .description을 이용해 string으로 변경 후 출력해야 함.
```



------



## Array



### declaration

```javascript
const arr1 = new Array();
const arr2 = [];
```



### index position

```javascript
const fruits=['apple', 'banana'];

console.log(fruits[0]);
// apple 출력
console.log(fruits.length);
// 배열의 길이 출력
console.log(fruits[fruits.length-1]);
// 마지막 배열 출력
```



### Looking for over an array

```javascript
// for of

for(let fruit of fruits) {
    console.log(fruit);}

// forEach

fruits.forEach((fruit)=>console.log(fruit));

// for
for(let i=0; i<fruits.length; i++) {
    console.log(Fruits[i];)
}
```



### Addition / Deletion 

```javascript
// push > 배열의 끝에 추가
fruits.push('melon', 'pear'); 
console.log(fruits); //apple, banana, melon, pear 출력

// pop > 배열의 끝부분부터 제거
fruits.pop();

// splice > 배열 포지션에 따라 제거
fruits.splice(1); // 1번 부터 전부 지우기
fruits.splice(1,1); // 1번 배열 하나 지우기
fruits.splice(1,1,'melon', 'pear'); // 1번 배열 하나 지운 후 그 자리에 melon과 pear 추가

// 두 개의 배열 합치기
const fruits2=['pear', 'coconut']
const newFruits=fruits.concat(fruits2);
console.log(newFruits); // 배열 끝에 pear, coconut 추가해서 출력
```



### Find the index

```javascript
Console.log(fruits);
Console.log(fruits.indexof('apple')); // 0출력, 배열에 없으면 -1 출력
Console.log(fruits.includes('watermelon')); // 있으면 true, 없으면 false 출력
Console.log(fruits.lastIndextof('apple')); // 만약 배열에 apple이 여러 개 있을 시 마지막 apple 배열 출력
```



------



## Operator



### string concatenation

```javascript
console.log('cute' + 'cat'); //cute cat 출력
console.log('1'+2); //12 출력
```



### numeric operator

```javascript
console.log(1+2); //add
console.log(1-2); //substract
console.log(1/2); //divide
console.log(1*2); //multiply
console.log(5%2); //remainder 
console.log(2**3); // exponentiation
```



### increment / decrement

```javascript
let counter = 2;
const preIncrement = ++counter;
// = counter = counter+1; preIncrement=counter; 증가 후 할당, 3출력

const postIncrement = counter++;
//할당 후 증가, 4출력
```



### assignment

```javascript
let x=3;
let y=4;
x+=y; // x=x+y;
x-=y;
x*=y;
x/=y;
```



### comparison

```javascript
console.log(10<6);
console.log(2<=4);
```



### logical

```javascript
// || 하나라도 true라면 true 출력
const value1 = false;
const value2 = 4<2;
console.log(`or: ${value1 || value2 || check()}`);

// && 둘 다 true일 때만 true 출력
// ! true일 때 false, false일 때 true 출력
```



### equality

```javascript
// == loose equality 타입이 달라도 됨 ex) 5, '5' 같다고 출력
// === strict equality 타입이 다르면 다름 ex) null, undefined는 다르다고 출력
```





### conditional

```javascript
// if, else if, else

if(name === 'jenny') {
    console.log('hi, jenny')}
else if (name === 'ellie') {
    console.log('hi, ellie')}
else { console.log ('unknown');}

// 만약(if) jenny일 때 hi, jenny 출력, jenny가 아닌 ellie일 때 (else if) hi, ellie출력, 둘 다 아니라면 unkown 출력

console.log(name === 'jenny' ? 'yes' : 'no');
//true일 때 yes 출력

//switch
const test = 'a';
switch (test) {
        case 'a';
        console.log('the first alphabet');
        break;
        
        case 'b';
        console.log('the second alphabet');
        break;
        
    default: console.log('undefined');
        break;
}

// case ''; case''; console.log(); case 두 개에 출력값 하나도 가능.
```



### loop

```javascript
// while

let i=3;
while(i>0) { 
console.log(`while : ${i}`)};
i--;
} // 3, 2, 1 출력
//i가 0 초과일 때 i--를 반복

// do while문
do {console.log (`do while : ${i}`);
i--;
} while (i>0); 
//i가 0초과일 때 i--를 반복

// for문
(i=3; i>0; i--) {
    console.log(`for : ${i}`);
}

//i가 3일 때 i가 0초과 일 때까지 i--를 반목
```



------



## Function

재사용 가능, 값 계산



### declaration

```javascript
function printHello () {
    console.log('Hello'); } // Hello 출력 함수
printHello ();
}
```



### parameter

```javascript
function changeName (obj) { //obj는 reference로 전달. 변경사항이 메모리에 그대로 적용
    obj.name = 'coder';
}
const jenny = {name : 'jenny'};
changeName (jenny);
console.log(jenny);

//name이 coder로 변경되어 출력
```



### rest parameter

```javascript
function printAll (...args) {
    for (let i = 0; i<args.length; i++) {
        console.log(args[i]);
    }
}
printAll('html' 'css', 'javascript')
// 배열 출력 함수
```



### local scope

```javascript
// 안에서는 밖이 보이지만 밖에서는 안이 보이지 않는다

let globalMessage = 'global'; //global variable
function printMessage() {
    let message = 'hello';
    console.log(message); // local variable, 밖에서 출력 불가
    console.log(globalMessage);
}
printMessage();
```



### return a value

```javascript
function sum(a,b) {
    return a + b;
}
const result = sum(1, 2); //3 출력
```



``` javascript
const print = function (){ //anonymous function}
console.log('print');
};
print(); // print 출력
printAgain = print; // print 출력

// function declaration은 hoisting이 가능. (정의 전 호출 가능)
```



### callback

```javascript
function quiz(answer, printYes, printNo) {
    if (answer === 'cat') {
        printYes();
    } else {
        printNo();
    }
}
const printYes = function () {
    console.log('yes');
} ;

const printNo = function print() {
    console.log('no');
};
quiz('wrong', printYes, printNo); // '정답', callback 함수
quiz ('cat', printYes, printNo);
```



### arrow function

```javascript
//always anonymous
const print = function () {
    console.log('simple!');
};
const print = () => console.log('simple!');

const add = (a, b) => a+b; 
```



### IIFE

```javascript
(function hello() { 
console.log('IIFE');}) ();

//선언 즉시 바로 출력
```


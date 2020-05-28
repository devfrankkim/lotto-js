
```js
 splice  

[1, 2, 3].splice(1, 2) // [2, 3] 배열로 return
[1, 2, 3].splice(1, 2)[0] // 2

정렬하기 sort()
sort는 사전 순이다. 
abc, def, ab, z
ab, abc, def, z
사전은 첫 글자부터 본다. 
숫자 크기 순서가 아니다.
ex) [30, 50, 40, 7].sort() // []

 [30, 50, 40, 7].sort((previous, current) => {
     return previous - current
 })

 previous - current => - or + 

 minus comes firt for small numbers
 
 summary 
 오름차순 => 뺐을 때, - 
 내림차순 => 뺐을 대, +
  

 className 넣어주는 이유는  CSS를 받게 하기 위해서.

반복문을 사용해서 unit을 따로 뜨게 할 수 있다.
setTimeout(() => {}, 1000 * i)

중복되면 반복문을 사용하자.
어디가 중복되는지 규칙을 파악해야 한다. 
변수 n or i 두고 반복문으로 바꾼다.

*클로저*
let 나오면서 없어졌다.

반복문
while
do while
for 

for each
filter
for of 
for in 
map

winBalls.forEach((number) => {
})

map, forEach 차이점?
map은 1:1 mapping  return사용
forEach는 단순 반복.



var candidate = Array(5).fill().map((v, i) => i + 1)
// [1, 2, 3, 4, 5]
// [1, 2, 3, 4]
// [1, 2, 3]
// [1, 2]


var shuffle = [];

// candidate 갯수 만큼 반복문을 돌린다.
// 0 < 5
// 0 - 5
// 1 - 4
// 2 - 3
// 3 - 2
for(let i = 0; candidate.length; i++) {

// 반복문 돌린 숫자를 0 ~ candidate.length  한번에 하나만 뽑힌다.
// maximum 4

 var random = Math.floor(Math.random() * candidate.length);
 // random  => 4, 3, 2

// 원본에서 잘라내야지, 똑같은 숫자가 반복 되지 않는다.
  var spliceArray = candidate.splice(random, 1)

  var value = spliceArray[0]
// spliceArray = [5, 4, 3]
// candidate = [1, 2]


  shuffle.push(value)
}

// shuffle [5, 4, 3]
```
```js
// for (let i = 0; i < 6; i++) { // 클로저 문제는 let 나오면서 X
//   setTimeout(() => {
//     const ball = document.createElement('div');
//     ball.className = 'ball';
//     colorize(winBalls[i], ball);
//     ball.textContent = winBalls[i];
//     resultTag.appendChild(ball);
//   }, 1000 * (i + 1))
// }
winBalls.forEach((number, index) => {
  setTimeout(() => {
    const ball = document.createElement("div");
    ball.className = "ball";
    colorize(number, ball);
    ball.textContent = number;
    resultTag.appendChild(ball);
  }, 1000 * (index + 1));
});
```



```js
const arr = [1, 2, 3]
for(let n = 0; n <= 2; n += 1){
    arr[n] = arr[n] * 10
}
```

```js

function add(a, b, c) {
    a + b + c
}
const add = (a, b, c) => {
    return a + b + c
}

Array로 만든 빈 배열은 fill을 사용해야 한다.

Array(45).fill().map(v => 1)
Array(45).fill().map(v => v + 1)
Array(45).fill(1).map(v => v + 1)


Array(45).fill(1).map((v, i) => i + 1) // 1 ~ 45

매개변수는 변수

인수는 변수는 실제 값.
```
# ES6

# Destructuring(using in React)
## Destructuring: ES6부터 도입, 구조화된 배열 또는 객체를 비 구조화, 파괴하여 개별적인 변수에 할당하는 것 (배열 또는 객체 리터럴에서 필요한 값만을 추출하여 변수에 할당하거나 반환할때 유용하다.)
---
1. 배열 디스트럭쳐링(Array destructuring)
    배열의 각 요소를 배열로부터 추출하여 변수 리스트에 할당함. 추출/할당 기준은 배열의 인덱스이다.
>CODE EXAMPLE

```
const arr = [1,2,3];
const [one, two, three] = arr;
console.log(one, two, three);
```
```
let x, y, z;
[x, y, z] = [1, 2, 3];
```
(ES6의 디스트럭처링 배열에서 필요한 요소만 추출하여 변수에 할당하고 싶을 경우 유용)
>CODE EXAMPLE

```
const today = new Date();
const formattedDate = today.toISOString().substring(0,10);
const [year, month, day] = formattedDate.split('-');
console.log([year, month, day]);
```
2. 객체 디스트럭처링(Object destructuring)
    객체의 각 프로퍼티를 객체로부터 추출하여 변수 리스트에 할당한다, 할당 기준은 프로퍼티 이름(키)이다.
>CODE EXAMPLE

```
const obj = { firstName: 'Ungmo', lastName: 'Lee' };
const { lastName, firstName } = obj;
console.log(firstName, lastName);
```

>중첩일 경우
```
const person = {
    name: 'Lee',
    address: {
        zipCode:'03068',
        city: 'Seoul'
        }
       };
       
  const { address: {city}} = person;
  console.lot(city);
  ```

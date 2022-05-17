# 2. x만큼 간격이 있는 n개의 숫자

### 프로그래머스 Level 1 연습문제

### 문제설명

<aside>
💡 함수 solution은 정수 x와 자연수 n을 입력 받아, x부터 시작해 x씩 증가하는 숫자를 n개 지니는 리스트를 리턴해야 합니다.
다음 제한 조건을 보고, 조건을 만족하는 함수, solution을 완성해주세요.

</aside>

### 제한 조건

- x는 -10000000 이상, 10000000 이하인 정수입니다.
- n은 1000 이하인 자연수입니다.

### 예시

[제목 없음](https://www.notion.so/80cff5a001264887b02a199095243f2b)

### JavaScript 기본 코드

```jsx
function solution(x, n) {
   
}
```

### 내 풀이 (부분)

```jsx
return Array(n).fill(x).map((item, index) => item * (index + 1));
```

1. 리스트를 return해야 하므로, 먼저 크기가 n인 Array를 만들었다.
2. fill 메소드를 사용해 시작하는 값인 x로 모두 채워주고,
3. map 메소드로 반복하면서 각각의 아이템에 index + 1의 값을 곱해주고 return 해주었다.
    
    (index값이 0부터 시작하면 처음 값의 결과가 0이 되어버리기 때문에 +1 하여 곱해줌)
    

### +) _.fill(array, value, [start=0], [end=array.length])

- **동작**
    
    배열의 요소들을 시작부터 끝까지 지정한 값으로 채운다. (끝은 포함하지 않음)
    
- **Arguments**
    1. array : 값으로 채울 배열
    2. value : 배열을 채울 값
    3. [start=0] : 시작 지점(기본값; 0)
    4. [end=array.length] : 끝 지점 (기본값; 배열의 길이)
- **Returns**
    
    배열을 반환한다.
    

```jsx
var array = [1, 2, 3];
 
_.fill(array, 'a');
console.log(array);
// => ['a', 'a', 'a']
 
_.fill(Array(3), 2);
// => [2, 2, 2]
 
_.fill([4, 6, 8, 10], '*', 1, 3);
// => [4, '*', '*', 10]
```

### 다른 풀이

```jsx
let answer = [];
for(let i = 1; i <= n; i++) {
	answer.push(x * i);
}

return answer;
```

for문을 사용하여 n번동안 x * i를 하여 answer 배열에 집어넣는다.

(여기도 마찬가지로 i는 1부터 시작함)
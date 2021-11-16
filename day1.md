[Javascript Codekata Day1]
---
<br>

# 문제 

<br>

`twoSum`함수에 숫자배열과 '특정 수'를 인자로 넘기면, 더해서 '특정 수'가 나오는 index를 배열에 담아 return해 주세요. 

<br>

nums: 숫자 배열		

target: 두 수를 더해서 나올 수 있는 합계		

return: 두 수의 index를 가진 숫자 배열			

<br>

## example

<br>

nums은 [4, 9, 11, 14] target은 13

nums[0] + nums[1] = 4 + 9 = 13 이죠?

그러면 [0, 1]이 return 되어야 합니다.

<br>

## 가정

<br>

target으로 보내는 합계의 조합은 배열 전체 중에 2개 밖에 없다.

<br>

```jsx
const twoSum = (nums, target) => {
  // 아래 코드를 작성해주세요.
  // 변수 findIndexArr에 빈 배열을 생성한다.
  // 1. 매개변수 nums
  // 2. 매개변수 target
  // 3. 매개변수로 받은 배열 nums를 각 각 순회하며
  // 3.2 2개가 순회되게 한다.
  // 3.3 첫 번째 순회 안에 두 번째 순회를 넣는다.
  // 3.4 순회하면서 요소1과 요소2의 합이 매개변수 target 값이 될때까지 순회한다.
  // 5. 요소 1과 요소 2의 인덱스를 찾는다.
  // 5.1 찾은 인덱스를 findIndexArr에 담는다.
  // 6. findIndexArr가 리턴 값이 된다.
	// index를 찾을 때 indexOf를 사용할 수 있다.

  for(let i = 0; i < nums.length; i++){
    for(let k = 0; k < nums.length; k++){
      if(nums[i] + nums[k] === target) return [nums.indexOf(nums[i]), nums.indexOf(nums[k])];
    }
  }
}
```

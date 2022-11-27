> # 구조 분해 할당

    - 배열 또는 객체 속성을 해체하여 개별로 변수에 담는 표현식이다.
    - 함수에 객체나 배열을 전달해야 하는 경우, 그 중에서도 배열 데이터의 일부만 필요할 때,
      함수의 매개변수가 많거나 매개변수 기본값이 필요한 경우 주로 사용된다.
      (*매개변수 기본값: 함수등에 매개변수로 undefined가 전달될 경우를 방지하기 위해
       지정하는 기본값)
    - '분해'는 '파괴'를 의미하는것이 아니며, 분해 대상이 수정되지 않는다.

### 🔍 과제 01.

    * 구조 분해 할당을 사용하여 값을 할당하고, alert를 통해 이를 실행하도록 함

```
let user = { name: "John", years: 30 };

// 할당 연산자 좌측에 답안을 작성하시면 되겠죠?
// ... = user

alert( name ); // John
alert( age ); // 30
alert( isAdmin ); // false
```

### 📝 해답 01.

```
let user = { name: "John", years: 30 };

let {name, years: age, isAdmin = false} = user;

alert( name ); // John
alert( age ); // 30
alert( isAdmin ); // false
```

### 🔍 과제 02.

    * 최대 급여를 받는 직원 이름을 반환하는 함수 만들기

```
let salaries = {
  "John": 100,
  "Pete": 300,
  "Mary": 250
};
```

### 📝 해답 02-1.(나의 풀이)

```
let salaries = {
  John: 100,
  Pete: 300,
  Mary: 250,
};

function topSalary(salaries) {
  for (const [name, pay] of Object.entries(salaries).sort((a, b) =>
    b[0].localeCompare(a[0])
  )) {
    if (pay > 0) {
      return name;
    }
  }
  return null;
}

topSalary(salaries); // 'Pete'
```

### 📝 해답 02-2.(JS.Info 해답)

```
let salaries = {
  John: 100,
  Pete: 300,
  Mary: 250,
};

function topSalary(salaries) {

  let max = 0;
  let maxName = null;

  for(const [name, salary] of Object.entries(salaries)) {
    if (max < salary) {
      max = salary;
      maxName = name;
    }
  }

  return maxName;
}

topSalary(salaries); // 'Pete'
```

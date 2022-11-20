> # switch문

    - 하나 이상의 case문으로 구성되며, 변수값과 일치하는 case를 찾아가는 방식이다.
    - if문의 조건문이 boolean을 주로 이용한다면 switch문은 문자열과 숫자를 이용하는 경우가 많다.
    - 복수의 if문을 switch문으로 대체하면 가독성을 높이기에도 좋다.

### 🔍 과제 01.

    - "switch"문을 "if"문으로 변환하기

```
switch (browser) {
  case 'Edge':
    alert( "Edge를 사용하고 계시네요!" );
    break;

  case 'Chrome':
  case 'Firefox':
  case 'Safari':
  case 'Opera':
    alert( '저희 서비스가 지원하는 브라우저를 사용하고 계시네요.' );
    break;

  default:
    alert( '현재 페이지가 괜찮아 보이길 바랍니다!' );
}
```

### 📝 해답 01.

```
    if(browser === 'Edge'){
        alert( "Edge를 사용하고 계시네요!" );
    }else if(browser === 'Chrome'
    || browser === 'Firefox'
    || browser === 'Safari'
    || browser === 'Opera'){
        alert( '저희 서비스가 지원하는 브라우저를 사용하고 계시네요.' );
    }else{
        alert( '현재 페이지가 괜찮아 보이길 바랍니다!' );
    }
}
```

### 🔍 과제 02.

    - "if"문을 "switch"문으로 변환하기

```
let a = +prompt('a?', '');

if (a == 0) {
  alert( 0 );
}
if (a == 1) {
  alert( 1 );
}

if (a == 2 || a == 3) {
  alert( '2,3' );
}
```

### 📝 해답 02.

```
let a = +prompt('a?', '');
switch (a) {
  case 0:
    alert(0);
    break;
  case 1:
    alert(1);
    break;
  case 2:
  case 3:
    alert("2,3");
    break;
}
```

# 1

json :
데이터를 전송할 때 많이 사용되는 경량의 DATA 교환 형식
장점 : 1. 문서화를 할 수 있다. 2. 재사용 가능.

DATA 형식

1. 중괄호
2. key(중복 x), value(중복 o) 구성
3. value(문자형, 정수형, 논리형, 배열, json...)

```js
ex)
emp = {
    empno : 7369,
    ename : "SMITH",
    mgr : [7902, 7370]
}
//SMITH 사수 직업과 급여를 알고 싶다.
emp = {
    empno : 7369,
    ename : "SMITH",
    mgr : [{
        empno:7902,
        sal:3000
        job:"CRERK"
    }, {
        empno:7370,
        sal:5000
        job:"CRERk"
    }]
}
//emp
SMITH의 직업과급여
SMITH의 부서이름
SMITH의 부서 인원수

emp={
    empno : 7369,
    ename : "SMITH",
    job : 'CRERK',
    sal : 3000,
    dname : "SALES" ,
    dname_ count : 5
}

SMITH의 사원번호와 급여
SMITH의 사수는 3명이고 사수의 번호와 직업을 알고싶다.

emp = {
    empno : 7369,
    sal : 3000
    mgr : [{
        empno: 7902,
        job : "CRERK"
    },{
        empno: 7370,
        job: "CRERK"
    },{
        empno : ,
        job : ""
    }
    ]
}
```

# 2

function()

한수(메소드 만드는 규칙) 1.작게 2.작게

1. 항상 함수는 작게 만들어야 한다.
2. 함수는 한 가지를 해야한다.
   그 한 가지를 잘 해야 한다.
   그 한 가지만 을 해야 한다.

3. 대가(Master) 프로그래머들은 시스템을 구현할 프로그램이 아니라 풀어갈 이야기로 여긴다.

왜 바닐라.js 에서 제이쿼리로 넘어갔을까?
기능적 한계
2008 ~ 2017 or 2018 제이쿼리시대
2018년 이후에는 React, Vue, 앵귤러
지금은 제이쿼리 or React

# 3

바닐라.js (순수 자바스크립트)

```js
document.getELementByid
                     className
                     name
:태그를 불러 옴

$('.classNAme').css('display','block')
```

## 자주 사용하는 jquery

- show,hide : 보여준다 , 숨기다
- append : 원하는 태그를 추가해줌.
- chidren
- **\*** val, text, focus
- \*attr

## 바닐라js -> jquery

- document -> $
- get -> ('')

```
document.getELementByid('name').style.display = 'none'
 -> $('#name')hide();
```

# 4

Jquery

- on :js 는 매개변수 사용가능 $('#name').on('이벤트' , funchion() { } ) // 쓰는 이유 프로젝트가 커지면 변수이름 짓기가 어려움
- append : 포스트윗(땟다 붙힘) & append to
- children : \*부모기준 (자식만)- 자식정보를 보고싶을 때.(배열형태로 가져옴) & find
- show&hide

var val = $('#name').children();
이 돼는이유 children()은 리턴값을 가지고 있기떄문에(메소드)

min(압축된 파일)
js 에서의

- ==(같다 '데이터 타입이 다르더라도 값이 같으면 같다표시')
- ===(같다 데이터 타입도 같아야 됨)

## 메소드 체이닝 & 내장함수

- var userId = $('#userId').val().trim(); (메소드 체이닝(return 값이 있는 함수만 사용가능))

- trim은 문자열함수이고 자바스크립트의 내장함수다
  > "라이츄".trim(); 문자열 자체가 함수를 가지고 있음.

```
$(**)val())
-> function val() {
    return 문자
    }
```

## 정규표현식(Relguler Expression)

:문자열을 처리하는 방법

```
ex)
 var Regex = /^[가-힣]+$/;//정규표현식(한글이름만 찾기)
```

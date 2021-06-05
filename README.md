# 김동희[201740107]
## [06월 1일]
>오늘 배운 내용
JQuery는 "유용한 자바스크립트를 모아놓은 집합체" 라고 할 수 있는데, 오늘 날 가장 인기있는 자바스크립트 라이브러리 중 하나이다. 

이러한 JQuery는 일단 가장 눈에 띄는 장점을 가지고 있는것이 바로 자바스크립트보다 간결하게 쓸 수 있다는 점이다. 

다음은 보통 일반적으로 쓰는 자바크립트의 언어이다. 

document.getElementById("divId"); 
document.getElementsByClassName("className");
 이 자바스크립트를 구문을 JQuery로 쓰게 되면 다음과 같다. 

$("#divId");
$(".className");
한눈에 봐도 훨씬 간결하고 깔끔하게 쓸 수 있다는 것이 보일것이다. 


이 외에도 ajax를 활용할 때에도 유용하게 쓸 수 있고, css를 통해 비교적 쉽게 페이지 내부에 접근할 수 있으며 다양한 애니메이션을 간편하게 사용할 수 있다는 장점 역시 가지고 있다. 

Jquery 사용법

JQuery를 사용하는 방법은 크게 2가지가 있다.

1. 파일을 다운받아서 프로젝트 폴더에 넣고 참조하는 방법

2. CND을 이용한 참조

파일을 다운받아서 넣어줘도 상관없지만 오늘은 2번의 CND를 이용한 참조방법​을 통해 JQuery를 사용해 보고자 한다. 

CND를 이용한 참조방법은 내 폴더있는 파일들 말고 다른 사이트에서 참조해서 쓰는 방법에 해당한다. 

때문에 다운받는 방법보다 훨씬 간편하게 사용할 수 있다. 

먼저 JQuery를 사용하기 위한 셋팅 방법은 다음 코드 중 한 가지를 HTML파일의 HEAD태그 안에 적어주기만 하면 된다. 

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
//아래 주소는 JQuery에서 제공하는 최근 버전의 url이다.
<script src="http://code.jquery.com/jquery-latest.js"></script>
간단한 JQuery 문법

자 앞서 언급한 링크주소를 HTML 안에 넣어주게 되면 이제 JQuery를 쓸 준비가 된 상태이다.

$(선택자).동작함수();
JQuery문법의 기본이 되는 $()선택자이다. 

기호는 JQuery를 의미하고, JQuery에 접근할 수 있게 해주는 식별자이다. 

이러한 선택자를 사용하여 원하는 HTML요소를 선택하고, 동작함수를 정의하여 선택된 요소에 원하는 동작을 설정한다. 

보통$() 함수를 통해 생성된 요소를 JQuery의 객체라고 한다. 

# 김동희[201740107]
## [05월 25일]
>오늘 배운 내용

exprss 모듈

- 웹 애플리케이션을 개발할 때 가장 많이 사용되고 있는 외부 모듈입니다.

- http 모듈에 비해 많은 기능을 갖추고 있어 보다 손쉽게 웹 애플리케이션을 개발할 수 있습니다.

- jade, ejs 등과 같은 동적 웹페이지 파일을 지원하고 있어 보다 손쉽게 애플리케이션 개발이 가능합니다.

 - 웹 서비스는 개방형 프로토콜과 표준의 조합으로 애플리케이션 또는 시스템  사이의 데이터 교환에 사용됨

 - 서로 다른 언어로 개발 되고 서로 다른 플랫폼에서 실행되는 애플리케이션들이  단일 컴퓨터의 프로세스간 통신과 유사한 방식으로 인터넷과 같은 네트워크를  통해 데이터를 교환할 수 있음

 - 이런 호환성은 개방형 표준을 따르기 때문에 가능

 - RESTful 웹 서비스는 REST 아키텍처를 사용하는 웹 서비스를 의미
 
  » REST 아키텍처를 구현하기 위해 HTTP 메서드 사용
  
  » 보통 JSON과 HTTP 메서드와 같이 리소스를 표현하는 URI (Uniform Resource  Identifier)를 정의합니다.
 
 ![image](https://user-images.githubusercontent.com/79896108/120063516-711ea200-c0a2-11eb-82aa-66f5b30376e2.png)




# 김동희[201740107]
## [05월 11일]
>오늘 배운 내용

예외처리

try 문은 하나 이상의 문을 포함하는 try- 블록으로 구성됩니다. 단일 문에도 {}를 항상 사용해야합니다. 최소한 하나의 catch-block 또는 finally-block이 있어야합니다. 이것은 try 문에 대한 세 가지 형식을 제공합니다.

try-block에서 예외가 발생하지 않으면 catch-block을 건너 뜁니다.

하나 이상의 try 문을 중첩 할 수 있습니다. 내부 try 문에 catch-block이 없으면 포함하는 try 문의 catch- 블록이 대신 사용됩니다.

try {
  // 이곳의 코드를 실행
} catch(err) {
  // 에러가 발생하면, 여기부터 실행됨
  // err는 에러 객체
} finally {
  // 에러 발생 여부와 상관없이 try/catch 이후에 실행됨
}
간단한 구문으로 테스트해보겠습니다.

const a = 500;
 
try {
  a = 1000;
} catch (e) {
  console.log(e); // TypeError: Assignment to constant variable.
}
특정 발생에러를 핸들링 할수 있습니다.

try {
  a = 1000;
} catch (e) {
  if (e instanceof TypeError) {
    console.log('Type error can handle here');
  } else {
    throw e; // Throw other errors
  }
}
finally 는 언제든 실행됩니다.

try {
  a = 1000;
} catch (e) {
  if (e instanceof TypeError) {
    console.log('Type error can handle here');
  }
} finally {
  console.log('I got this anyway');
}
중첩해서 사용할 수 있습니다.

const a = 100;
try {
  a.toString();
  try {
    a = 200;
  } catch (e) {
    if (e instanceof TypeError) {
      console.log('Error on second try');
    }
  }
} catch (e) {
  console.log(e);
} finally {
  console.log('No error on first try');
}
스펙정의

try {
  try_statements
}
[catch (exception_var) {
  catch_statements
}]
[finally {
  finally_statements
}]
try_statements
실행할 구문입니다.

catch_statements

try-block에서 예외가 발생하면 실행되는 구문입니다.

exception_var

연관된 catch-block에 대한 예외 개체를 보유하는 식별자입니다.

finally_statements

try 문이 완료된 후 실행되는 구문입니다. 예외가 발생했는지 포착되었는지에 관계없이 실행됩니다.

# 김동희[201740107]
## [05월 4일]
>오늘 배운 내용
Date 객체와 날짜
날짜를 저장할 수 있고, 날짜와 관련된 메서드도 제공해주는 내장 객체 Date에 대해 알아봅시다

Date 객체를 활용하면 생성 및 수정 시간을 저장하거나 시간을 측정할 수 있고, 현재 날짜를 출력하는 용도 등으로도 활용할 수 있습니다.

객체 생성하기
new Date()를 호출하면 새로운 Date 객체가 만들어지는데, new Date()는 다음과 같은 형태로 호출할 수 있습니다.

new Date()
인수 없이 호출하면 현재 날짜와 시간이 저장된 Date 객체가 반환됩니다.

![image](https://user-images.githubusercontent.com/79896108/117543135-80d43900-b056-11eb-8da1-c738ce6f7a55.png)

UTC 기준(UTC+0) 1970년 1월 1일 0시 0분 0초에서 milliseconds 밀리초(1/1000 초) 후의 시점이 저장된 Date 객체가 반환됩니다.

![image](https://user-images.githubusercontent.com/79896108/117543150-9184af00-b056-11eb-9c86-dddafd5d17e7.png)

1970년의 첫날을 기준으로 흘러간 밀리초를 나타내는 정수는 타임스탬프(timestamp) 라고 부릅니다.

타임스탬프를 사용하면 날짜를 숫자 형태로 간편하게 나타낼 수 있습니다. new Date(timestamp)를 사용해 타임스탬프를 사용해 특정 날짜가 저장된 Date 객체를 손쉽게 만들 수 있고 date.getTime() 메서드를 사용해 Date 객체에서 타임스탬프를 추출하는 것도 가능합니다

Array 객체

- 배열을 관리할 수 있는 객체이다.

- JavaScript의 배열은 Array객체이다.

- toString : 쉼표(,)로 구분하여 배열이 관리하는 값들을 하나의 문자열로 만들어 반환한다.

- join : 지정된 문자열을 구분하여 배열이 관리하는 값들을 하나의 문자열로 만들어 반환한다.

- push : 배열 뒤에 새로운 맴버를 추가한다.

- pop : 배열의 제일 마지막 맴버를 반환하고 제거한다.

- shift : 배열의 제일 앞의 맴버를 반환하고 제거한다.

- unshift : 배열의 제일 앞에 멤버를 추가한다.

- sort : 배열이 관리하는 값을 오름차순으로 정렬한다.

- reverse : 배열이 관리하는 값의 순서를 역순으로 정렬한다.

<script>
	var array1 = [10, 20, 30, 40, 50];

	//쉼표로 구분된 배열보여준다
	var a1 = array1.toString(); 
	document.write("a1 : " + a1 + "<br/>");

	//()안에 구분되는 문자
	var a2 = array1.join("_")
	document.write("a2 : " + a2 + "<br/>");


	//배열을 늘리거나 줄이는 것이 가능
	var a3 = [];
	document.write("a3.length : " + a3.length + "<br/>");
	document.write("a3 : " + a3 + "<br/>");

	a3[0] = 10;
	a3[1] = 20;
	document.write("a3.length : " + a3.length + "<br/>");
	document.write("a3 : " + a3 + "<br/>");
	
	//뒤에 추가
	a3.push(30);
	a3.push(40);
	a3.push(50, 60, 70, 80, 90, 100);
	document.write("a3.length : " + a3.length + "<br/>");
	document.write("a3 : " + a3 + "<br/>");

	//마지막 꺼 반환과 제거
	var a4 = a3.pop();
	document.write("a4.length : " + a4.length + "<br/>");
	document.write("a4 : " + a4 + "<br/>");
	document.write("a3 : " + a3 + "<br/>");

	//처음 꺼 반환과 제거
	var a5 = a3.shift();
	document.write("a3.length : " + a3.length + "<br/>");
	document.write("a5 : " + a5 + "<br/>");
	document.write("a3 : " + a3 + "<br/>");	

	//앞에 추가
	a3.unshift(10);
	document.write("a3.length : " + a3.length + "<br/>");
	document.write("a3 : " + a3 + "<br/>");

	
	var array3 = [50,30,10,20,40,30,80,90];
	var array4 = ["다","바", "가", "나", "사", "바"];

	//순서대로 정렬
	array3.sort();
	array4.sort();
	document.write("array3 : " + array3 + "<br/>");
	document.write("array4 : " + array4 + "<br/>");	

	//순서 뒤집어서 정렬
	array3.reverse();
	array4.reverse();
	document.write("array3 : " + array3 + "<br/>");
	document.write("array4 : " + array4 + "<br/>");	

</script>

# 김동희[201740107]
## [04월 27일]
>오늘 배운 내용
1.객체 기본

![image](https://user-images.githubusercontent.com/79896108/116817293-89cd9200-aba0-11eb-8eb8-e33216b38975.png)

객체를 구성하는 멤버의 값은 어떤 것이라도 될 수 있습니다. 

우리가 만든 person 객체는 문자열, 숫자, 배열 두개와 두개의 함수를 가지고 있습니다.

![image](https://user-images.githubusercontent.com/79896108/116817309-a5d13380-aba0-11eb-9bd8-33c90932a9e9.png)

처음 4개의 아이템은 데이터 아이템인데, 이걸 객체의 프로퍼티(속성) 라고 부릅니다. 

끝에 두개의 아이템은 함수인데 이 함수를 통해 데이터를 가지고 뭔가 일을 할 수 있게 됩니다. 

이걸 우리는 메소드 라고 부릅니다.

2.점 표기법

![image](https://user-images.githubusercontent.com/79896108/116817326-c0a3a800-aba0-11eb-8fe5-a5f04c1888fb.png)

우리는 객체의 프로퍼티와 메소드를 점 표기법을 통해 접근했습니다. 

객체 이름(person)은 네임스페이스처럼 동작합니다. 

객체내에 캡슐화되어있는것에 접근하려면 먼저 점을 입력해야합니다. 

그 다음 점을 찍고 접근하고자 하는 항목을 적습니다. 

간단한 프로퍼티의 이름일 수도 있을 것이고, 배열의 일부이거나 객체의 메소드를 호출할 수도 있습니다.

3.괄호 표기법

![image](https://user-images.githubusercontent.com/79896108/116817343-d1541e00-aba0-11eb-844d-e65bd4a3beb3.png)

person.age

person.name.first

person['age']

person['name']['first']

4.생성자 함수와 프로토타입
생성자 함수란 쉽게 말해서 new 키워드와 함께 쓰이는 함수이다. 우리가 직접 함수를 정의하여 new 키워드로 생성자 함수를 만들어 사용할 수도 있지만, 자바스크립트에 기본적으로 내장된 생성자 함수를 사용할 수도 있다.

생성자 함수는 특이하게 함수의 이름이 모두 대문자로 시작한다. 그래서 우리가 생성자 함수를 직접 정의해서 쓸 때에도 관례적으로 함수 이름의 첫 글자를 대문자로 쓴다.

![생성자](https://user-images.githubusercontent.com/79896108/116817412-2d1ea700-aba1-11eb-9921-c48b2f192ed2.PNG)


# 김동희[201740107]
## [04월13일]
>오늘 배운 내용

1. 함수생성 방법
함수 생성 방식(종류) - Normal, Arrow, Method
함수의 매개변수 리스트
함수 몸체 (함수 코드)
스코프 (Lexical Environment)
strict mode 여부
함수 객체의 프로토타입 - FunctionPrototype, Generator, AsyncFunctionPrototype 등과 같은 객체들로 사용

![함수](https://user-images.githubusercontent.com/79896108/115020044-f5530680-9ef4-11eb-842c-ddd1e061407c.PNG)


위 코드를 보면 <script>에서 function을 이용하여 showDialog라는 함수를 만들었다.

showDialog의 용도는 텍스트가 있는 대화상자를 출력할 때 사용할 것이다.

그리고 <body>를 보면 button을 만들고, onclick을 통해 클릭시 showDialog()함수를 호출하여 실행하게끔

만들었다.

즉, 미리 내가 사용할 재료를 만들어놓고 필요한 상황이 생기면 때에 맞게 재료를 사용하면 된다.
function 자체는 사실 어려운 내용이 아니다.

그 안에 어떤 문장, 명령이 들어가느냐가 더 중요하지 function은 말 그대로 함수를 만들어주는 역할만 하기 때문에
어려운 내용이 아니다!!

하지만, 자바스크립트를 이용하여 프로그래밍을 하다보면 function 또한 상당히 중요한 역할을 할 것이 뻔하기에 사용법은 꼭 숙지하도록 하자.

물론 뒤로 갈수록 function에 대한 존재감은 더 커질 것이라고 감히 예상해본다...

# 김동희[201740107]
## [04월06일]
>오늘 배운 내용

1. for문을 사용한 *찍기


 첫번째 별을 찍을때 i 도 0이고 j 도 0인 상태에서, 0<=0 을 만나면 아직 i 하고 j 가 같기때문에 조건을 한번 실행하게됩니다.

그러고 j++ 가 되고, 다시 비교를하려는데 i=0; j=1 이니까 조건식에서 1<=0 이됩니다

0은 1보다 작기때문에 두번째 for문을 빠져나게가되고, 첫번째 for문에서 줄바꿈을 해준다음, i++ 가 되는겁니다.

이게 반복되면 아래와 같은 결과가 나옵니다.

대부분 for문과 while문을 많이 쓰게 되는데 특히 for문을 가장 많이 사용하게 됩니다. 그 이유는 for문이 while문 보다 좀 더 가독성이 좋고 사용하기도 가장 편하기때문입니다.

2. push,pop,shit

push 는 배열의 끝에 원하는 값을 추가해주는 함수.

pop은 배열의 마지막 주소에 있는 값을 제거해주는 함수.

shift는 배열의 주소에 있는 값을 제거한 후에 반환해주는 함수.

push 와 pop를 이용하면 stack으로 이용할 수 있다.

push 와 shift를 이용하면 queue로 이용할 수 있다.

3. splice

console.log("\n splice");

foo = ["a","b","c","d","e"];

bar = foo.splice(1,3);

console.log(foo);

console.log(bar);

foo의 index 1에서 3개를 잘라서 bar에 저장

결과값:b,c,d

# 김동희[201740107]
## [03월 30일]
>오늘 배운 내용

switch 부분을 사용하여 내가 입력하는 값을 설정한 후, 결과값이 원하는 값이 출력
case 문 특정한 상황의 경우
break 문이 없더라면 멈추지않고 모두 실행

삼항 연산자
숫자의 부호를 비교해서 0보다 큰지 아닌지 판별
// 변수를 선언 후 조건을 구분한다.
삼항 연산자를 활용한 변수 초기화
변수가 undefined일때만 초기화

. 짧은 초기화 조건문

ll 연산자를 불이 아닌 자료에 사용할 경우

A ll B 에서 A가 참이라면 A로 대치

A ll B 에서 A가 거짓라면 B로 대치

예제 
//변수 선언
let text;
//짧은 초기화 조건문1

text = text ll "초기화 합니다_1"

console.log(text);

//짧은 초기화 조건문2

text = text ll "초기화합니다_2"

console.log(text);

![반복](https://user-images.githubusercontent.com/79896108/113471008-7ee5eb80-9494-11eb-82e3-c1844bc96452.PNG)

![반복2](https://user-images.githubusercontent.com/79896108/113471022-8e653480-9494-11eb-8654-12b3ff53928e.PNG)


# 김동희[201740107]
## [03월23일]
>오늘 배운 내용 <br/>

let date = new Date();
h = date.getHours();

console.log(h < 3 ll h > 8);
console.log(h >= 3 && h<= 8);

let type = typeof(date.getHours());
console.log(type);

const con1 = "상수선언";
console.log(con1);

# 김동희[201740107]
## [03월16일]
> 오늘 배운 내용 요약
> 여러줄 요약
> 3번

배운내용


![반복2](https://user-images.githubusercontent.com/79896108/113471015-860cf980-9494-11eb-80ae-69bdd400e5c7.PNG)

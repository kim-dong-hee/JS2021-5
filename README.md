# 김동희[201740107]
## [04월06일]
>오늘 배운 내용

1. for문을 사용한 *찍기


 첫번째 별을 찍을때 i 도 0이고 j 도 0인 상태에서, 0<=0 을 만나면 아직 i 하고 j 가 같기때문에 조건을 한번 실행하게됩니다.

그러고 j++ 가 되고, 다시 비교를하려는데 i=0; j=1 이니까 조건식에서 1<=0 이됩니다.

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

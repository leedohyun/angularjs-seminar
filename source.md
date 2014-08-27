name: inverse
class: center, middle, inverse
layout: true

---
class: titlepage, no-number
# AngularJS
## .author[부설연구소 통계분석파트 이도현<br>ZUM internet]

---
layout: false
# Agenda

- Javascript
- SPA(Single Page Application)
- AngularJS 철학
- AngularJS 마법 구경 하기
- AngularJS 내부 동작 이해

---
# Javascript

이 문제는 [Effective Javascript](http://www.yes24.com/24/goods/9375384?scode=032)에서 발췌

.x-small[
```javascript
3 + true = ?;	// 문법 에러 아닌가?..
```]

.x-small[
```javascript
function swap(a, i, j) {
	temp = a[i];	// 이게 동작은 하는데 나중에 문제가 될 수도...
	a[i] = a[j];
	a[j] = temp;
}
```]

.x-small[
```javascript
function hoistingTest() {
	console.log("뭐가 나올까? : " + test);
	if (true) {
		var test = "짠!";
	}
	console.log("변수를 블록안에서 선언했는데.... : " + test);
 }
 hoistingTest();
```]

---
# Javascript

앞의 질문에 대한 정답!

- 암묵적인 형변환
- var의 유무에 따라 변수 스코프가 달라짐 (전역? 지역?)
- 자바스크립트는 블록 단위 스코프를 지원하지 않고, 변수 선언과 할당이 나눠짐 (Variable Hoisting) -> 아래와 같아짐

.x-small[
```javascript
function hoistingTest() {
	var test;
	console.log("선언만 했군.. : " + test);
	if (true) {
		test = "짠!";
	}
	console.log("할당도 됐어.. : " + test);
 }
 hoistingTest();
```]

---
# Javascript

장점도 많지만 생각보다 잘못 사용 될 여지가 많은 언어

- 너무 유연함
- 암묵적인 형변환
- 전역변수
- 모듈 시스템 제공하지 않음

개발자의 이해도와 숙련도에 따라 결과물 차이가 클 것 같다

---
# Javascript

장점도 이야기 해줘야지...

- 그런데 왜 쓰냐고 묻는다면 '풍부한 접근성'과 '보편성'
- 유연함이 큰 무기가 될 수 있음
- CoffeeScript를 쓰면 많은 단점을 보완할 수 있다고 하던데.... 안써봤음ㅠ

---
# Javascript

올바르게 잘 쓰는 방법은?

- strict mode (var 없으면 에러)
- 모듈 시스템 (독립적인 실행 영역, Lazy-Load)
- 프로토타입 (Inheritance)
- 함수형 (Immutable, No side effect)
- 비동기 (Ajax, Callback, Promise)

---
# Single Page Application

A single-page application (SPA), also known as single-page interface (SPI), is a web application or web site that fits on a single web page with the goal of providing a more fluid user experience akin to a desktop application. - from wikipedia
- HTML, JavaScript, CSS를 이용하면 만들 수 있다.
- Gmail, Google Drive (이 분야 조차도 구글이 1등인 것 같네요.. 아닌가..)
- zum.com (프론트 줌도 SPA라고 볼 수 있어요)
- SPA를 아무런 도구 없이 만드는 건 너무 힘들다...
##### Backbone.js, AngularJS, Ember.js, KnockoutJS, Dojo, YUI, Agility.js, Knockback.js, CanJS, Maria, Polymer, React, Flight, Batman, Meteor, Derby, SocketStream (계속 뭔가 만들어지고 있음ㅠ)

---
# Single Page Application



---
name: last-page
class: center, middle, no-number
## Thank You!
### http://leedohyun.github.io/angularjs-seminar

.footnote[Slideshow created using [remark](http://github.com/gnab/remark).]

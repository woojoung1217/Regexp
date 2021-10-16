# <h1>정규표현식 공부(RegExp) ❀</h1>

자바스크립트를 사용하면서 정규표현식을 한 번도 사용하지 않은 분은 없을 것입니다.
하지만 많은 분이 ‘정규표현식은 검색해서 쓰는 정도’로 “나중에 배워야지”라는 생각을 하는 듯합니다.
물론 정규표현식이라는 것이 개발하면서 자주 사용되는 것도 아니고, 가독성이 좋다고 볼 수도 없기 때문에 패턴을 외우지 않으면 사용하기 어려워 공부를 미뤄오신 분이 많을 것으로 봅니다.

‘무조건 배워야 해!’ 보다는 조금 더 쉽게 배울 방법에 대해서 고민해 보고자 이 문서에 정리해 보았습니다.
정규표현식을 처음 시작하시는 분들에게 도움이 되었으면 합니다. 😣






<h1>정규표현식 with JavaScript</h1>

정규표현식이란 문자열을 검색하고 대체하는 데 사용 가능한 일종의 형식 언어(패턴)입니다.
간단한 문자 검색부터 이메일, 패스워드 검사 등의 복잡한 문자 일치 기능 등을 정규식 패턴으로 빠르게 수행할 수 있습니다.
단 정규식 패턴이 수행 내용과 매치가 잘 안 되어 가독성이 많이 떨어지기 때문에 입문자들이 어려워하는 경우가 많습니다.
하지만 초반 개념만 잘 잡으면 금방 익숙해질 수 있습니다.

정규표현식은 크게 다음과 같은 역할을 수행합니다.
## 역할 

문자 검색(search)
문자 대체(replace)
문자 추출(extract)

<br>

자바스크립트는 직접 빌드된 정규표현식을 지원하는 언어 중 하나로,
이 포스트에서는 자바스크립트에서 사용하는 정규표현식(정규식)을 기준으로 내용을 살펴보겠습니다.

```
특정한 언어나 환경에서만 동작하는 패턴이 있습니다.
모든 정규식을 다룰 수 없어 자바스크립트를 기준으로 문서를 정리했습니다.

```
## 정규식 생성
<!-- 생성자  -->
new RegExp('표현','옵션')<br>


new RegExp('[a-z]','gi')



## 메소드


메소드 | 문법 | 설명
--|--|--
test | 정규식.test(문자열) | 일치여부반환(boolean)
match | 문자열.match(정규식)|일차하는 문자열 반환(Array)
replace | 문자열.replace(정규식,대체문자) | 일치하는 문자를 대체

## 플래그(옵션)

플래그 | 설명
--|--
g | 모든문자 일치(global)
i | 영어 대소문자를 구분하지 않고 일치(ignore case)
m | 여러 줄 일치 (multie line)


## 패턴

패턴|설명
--|--
^ab | 줄(line) 시작에 있는 ab와 일치
ab$ | 줄(line) 끝에 있는 ab와 일치


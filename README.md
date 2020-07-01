# How JavaScript Works
더글러스 크락포드, How JavaScript Works(2020) 한글 번역판

## 목차

  1. [이름](#이름)
  2. [숫자](#숫자)

## 이름

자바스크립트는 변수 이름의 길이에 제한을 두지 않습니다. 가능하다면 이름만 보고도 무엇을 하는 것인지 짐작할 수 있게 만들어야 합니다.
### 모든 이름은 문자로 시작해서 문자로 끝나도록 하세요
자바스크립트는 `_, $`로 이름을 시작할 수 있으며  `_, $, 숫자`로 끝낼 수 있습니다.
이 외에도 해선 안되는 여러 문자를 허용하고 있습니다.
`_`로 시작하거나 끝나는 이름들은 `public` 속성이나 전역 변수를 의미하는데, 프로그램을 잘 작성했다면 이런 변수들은 전부 `private` 이었을 것입니다.
`$` 기호는 코드 제너레이터, 트렌스파일러, 매크로 처리기에서 사용할 목적으로 추가된 기호입니다. 이들은 달러 기호를 사용함으로써 일반 목적으로 사용되는 이름과 겹치지 않는 이름을 사용할 수 있다고 보장받습니다. 그렇기 때문에 코드 제너레이터와 같은 프로그램이 아닌 한 달러 기호는 사용하지 않는 것이 좋습니다.

### 서수형, 기수형을 의미하는 변수의 네이밍
* 순서를 나타내는 서수형 변수: `thing_nr` (e.g. `person_one`)
* 크기나 양을 나타내는 기수형 변수: `nr_things` (e.g. `two_persons`)

### 자바스크립트 내 모든 이름은 반드시 소문자로 시작해야 합니다.
이는 자바스크립트의 `new` 연산자 때문입니다. 함수 호출문의 `new`로 시작하면 해당 함수는 생성자로서 호출되고, 그렇지 않으면 함수로 호출됩니다.
생성자와 함수의 기능은 상당히 다르기 때문에 생성자를 잘못된 방식으로 호출하면 에러가 발생할 수 있습니다.
그래서 `new`를 써야 하는데 사용하지 않거나 잘못 사용한 경우 발생하는 문제를 자동으로 감지할 방법이 없습니다. 그래서 정한 약속이 **모든 생성자 함수의 이름은 대문자로 시작되어야 하며, 그렇지 않은 모든 경우에는 소문자로 시작되어야 한다**는 것입니다.

### 예약어

```
arguments await break case catch class const continue debugger default delete do else enum eval export extends false finally for function if implements import in Infinity instanceof interface let NaN new null package private protected public return static super switch this throw true try typeof undefined var void while with yield
```


**[⬆ back to top](#목차)**



## 숫자

자바스크립트의 `number`는 실수(real number)에서 영감을 받았지만, 진짜 실수는 아닙니다. 수학에 대한 이해나 직관은 자바스크립트의 `number`에 완벽하게 적용되지는 않습니다.

자바스크립트는 하나의 숫자형  `number` 를 가지고 있습니다. `number`는 인텔 iAPX-432 프로세서를 위해 처음 개발된 IEEE 부동소수점 연산 표준(IEEE 754)을 차용했습니다.



**[⬆ back to top](#목차)**


## 1. var VS let VS const 에 대해 설명하세요.

## 2. Javascript에서 this가 무엇이고 어떤역할을 하는지 설명하세요.

## 3. 클로저에 대해 설명하세요.

## 4. aysnc await에 대해 설명하세요.

## 5. 클래스형 컴포넌트와 함수형 컴포넌트의 차이점에 대해 설명하세요.

## 6. 깊은복사랑 얕은복사 차이점에 대해서 설명해주세요.

 <details>
<summary>환민</summary>

깊은 복사랑 얕은 복사는 복사되는 깊이에 차이점이 있습니다.

얕은 복사인 경우 Object.assign() 메서드를 사용하거나 스프레드 연산자를 사용해서 구현하게 되는데요.

객체를 복사했을 경우 뎊스가 1까지만 복사가 되고 같은 참조를 사용한다는 문제점이 있습니다.

하지만 깊은 복사의 경우 얕은 복사랑 다르게 뎊스에 상관없이 복사가 된다는 특징이 있습니다.

깊은 복사 같은 경우 structuredClone(), JSON 직렬화,역직열화 형식으로 바꿨다 푸는 방식으로 구현할 수 있습니다.

</details>

## 7. 호이스팅에 대해서 서명해주세요.

 <details>
<summary>환민</summary>

호이스팅이란 변수나 함수의 선언이 코드의 최상단으로 끌려 올러간 것 처럼 동작하는 것을 말합니다.

호이스팅은 발생하는 원리는 자바스크립트의 실행 컨텍스트가 코드 실행전 미리 식별자 정보를 등록하기 때문에 발생합니다.

val, 함수 선언은 undefined로 초기화 됩니다.

하지만 그 중 let, const 같은 변수들은 호이스팅이 일어나지 않는 것처럼 동작하는데요.

값이 초기화가 되지 않고 일시적 사각지대에 빠지기 때문입니다.

</details>

# 3장, 4장

# 3장 - 추상화

- 추상화란, 복잡다단한 현실을 concept 을 통해 symbol 과 intension 을 정의하고, 현실의 사물들을 그 intension 안의 element, 즉 extension(s)들로 classification 하는 걸 이야기한다.
- 타입이란, binary dataset 을 사람들이 만든 약속에 따라 (ex. 이런 binary data pattern 은 숫자간의 연산을 할 수 있게끔 Number 라는 type 으로 정의하자 등) 사람이 이해하기 쉬운 의미있는 정보의 형태로 분류하는 것을 의미한다.
- OOP 의 근간이 되는 Object 와 Type 은 비슷하면서도 다른데, 명백히 다른 점은 Type 의 경우 data 를 사람이 이해하기 쉬운 의미있는 정보들로 분류하는 약속을 의미하는 것이며, Object 의 경우는 behavior 를 기준으로 복잡다단한 문제를 협력으로 풀어나갈 개체들을 정의한 결과물이라는 점이다.
  - 그 Object 를 classification 하여 추상화를 진행한 결과물인 interface 와 abstract class 도 결국엔 행동을 기준으로 객체를 명세하는 것이고, 그걸 implements 하여 구체적인 무언가로 만들어내는 것은 자율에 맡긴다.
- Class 는 위에 나온 Object 와 Type 을 '구현' 하는 매개체이다.

---

# 4장 - 역할, 책임, 협력

## 들어가며

- 객체에 대해 생각해 볼 때는 앞에 나온 것처럼 객체의 행동을 기준으로 이 객체는 무엇인가를 고려하는 것도 좋지만, 협력이라는 문맥 속에서 객체의 행동을 고려해야 한다. 왜냐면, 결국 객체는 섬이 아니라 다른 객체들과 행동을 통해 소통을 하는 존재이기 때문이다. 협력관계를 기준으로 생각해보면 객체의 행동은 조금 더 쉽게 도출될 수 있다.
- 훌륭한 객체란, 협력을 우선적으로 고려하여 행동을 중점적으로 설계된 객체를 의미한다. 하나의 객체가 모든 걸 할 수 있게 모든 행동과 그에 대한 책임을 다 가지고 있는 오만한 객체는 좋은 객체라고 할 수 없다. 왜냐면, 협력을 하기 어렵기 때문이다.

## 협력

- 객체간의 협력이란 한 객체가 다른 객체에게 도움을 요청하고, 도움을 요청받은 다른 객체는 그 요청에 응답하는(request and response) 것으로 구성된다.
  - 그리고 현실, 그 현실을 옮겨놓은 프로그램은 대한 해결책은 여러 객체들 간의 여러 협력으로 구성된다.

## 책임

- 책임이란, 객체에 의해 정의되는 응집도 있는 행위의 집합을 의미한다.
- 해당 협력의 요청을 받은 객체는,

  - 요청에 대해 응답해 줄 수 있거나
  - 적절한 행동을 해야 할 의무가 있는 경우

  그 요청에 대해 응답해야 할 책임이 있다.

- 우리는 어떤 객체의 책임을 아는 것 (knowing) 과 하는 것 (doing) 으로 구성할 수 있으며, 이는 public interface 를 통해서 기술해낼 수 있다.
  - 해당 public interface 를 통해 외부 객체는 어떤 객체가 아는 것과 어떤 객체가 하는 것을 인지하고, 그 책임에 따른 요청을 한다.

## 역할

- 역할이란, 협력 관계 내에서 다른 객체로 대체할 수 있다는 사실을 나타내주는 일종의 표식이다.
- 다른 여러 개의 객체들이 같은 역할을 하는 객체라고 정의하기 전에, 행동이 호환되어야 한다는 점에 주목해야 한다.
  - 왜냐면, 객체란 위에서 말했듯 행동을 중심으로 정의되는 것이기 때문이다(속성 또한 존재하지만, 이는 행동에 필요한 혹은 행동의 결과물로 수반되는 요소이기 때문에 차후 순위로서 고려한다)

## 객체지향에 대한 오해들

- 객체는 어떤 값을 저장하는 수단이다.
  - 아니다, 객체란 어떠한 문제 해결을 위한 협력을 위해 역할을 나누어 갖고 상호간의 행위로서 소통하는 단위일 뿐이다.
- 객체지향 이란 클래스와 클래스의 관계를 표현하는 패러다임이다.
  - 아니다, 이는 정적인 요소(static)에 대한 설명이다. 실제 객체는 동적(dynamic)으로 동작한다.
- 이 관점에서 벗어나기 위해서
  - 객체라는 존재는 외톨이 섬이 아닌, 서로간의 협력으로 동작하는 요소들이라는 사실을 먼저 인지해야 하며
  - 데이터나 속성이 아닌 협력과 책임, 행동, 그리고 그 행동에 대한 응답과 반응, 그 응답과 반응을 촉발할 수 있는 메시지(message)부터 생각해야 한다.

## 객체 지향 설계 기법

### 책임 주도 설계

- 시스템의 기능에 대해 정의한다.
- 시스템의 기능을 나눠질 수 없을 때까지 작은 책임으로 분할한다.
- 책임을 할당한 객체를 만들거나 찾아 책임을 할당한다.
- 여기서 하나의 객체가 스스로 할 수 있는 게 아니라, 다른 객체와의 협력이 필요하다면 협력을 해 줄 다른 객체를 찾고, 그들의 협력관계에 대해서 정의한다.
- 하나의 책임을 여러 종류의 객체가 수행할 수 있다면, 그것은 구체적인 역할이 아닌 추상적인 역할로 대체한다.

### 디자인 패턴

> 효과적으로 일 하는 사람들의 한 가지 특징은, 아무것도 없는 상태에서 작업을 시작하지 않고 이전의 훌륭한 결과물을 모방하고 약간의 수정을 거쳐 원하는 결과물을 만들어낸다는 점이다 - 앨리스터 코오번, 2001

디자인 패턴이란

- 반복적으로 발생하는 문제
- 그 문제를 해결하기 위한 기법
- 해당 기법을 적용하기 적절한 상황
- 해당 기법을 적용하기 적절하지 않은 상황

에 대한 일련의 정보들을 의미한다.

- GOF 의 Design Pattern 이 해당 분야 명저로 유명하다.

### 테스트 주도 개발

- 테스트 주도 개발이란 개발을 하기 전 테스트를 먼저 작성하고 그 테스트를 간신히 통과할 정도로만 코드를 구현하는 걸 의미한다.
- 그렇지만 중요한 점은 테스트 주도 개발 또한 책임 주도 설계가 선행되어야 한단 점이다.
- 어떤 것을 미리 생각하고 그것을 테스트로 녹여내기 위해서는, 그것의 책임을 알아야 하며 그것의 역할에 대해서도 인지해야 한다.
- 이 뿐만 아니라, 가짜로 작동하고 원하는 값을 뱉어 solitary 를 보장하는 Mock 의 생성 및 주입을 알고 있어야 한다. 다른 객체와의 협력관계 또한 미리 알고있어야 한다는 이야기이다.

# 1장

# 중간 정리

- 객체지향이란 시스템을 상호작용하는 자율적인 객체들의 공동체로 바라보고 객체를 이용해 시스템을 분할하는 방법이다
- 자율적인 객체란 상태와 행위를 함께 지니며, 스스로 자기 자신을 책임지는 객체를 의미한다.
- 객체는 시스템의 행위를 구현하기 위해 다른 객체와 협력한다. 각 객체는 협력 내에서 정해진 역할을 수행하며 역할은 관련된 책임의 집합이다.
- 객체는 다른 객체와 협력하기 위해 메시지를 전송하고, 메시지를 수신한 객체는 메시지를 처리하는 데 적합한 메서드를 자율적으로 선택한다.

---

# 중간정리를 좀 더 구체적으로 녹여보자면?

- **객체지향이란 시스템을 상호작용하는 자율적인 객체들의 공동체로 바라보고 객체를 이용해 시스템을 분할하는 방법이다**
    - 큰 문제를 가장 쉽게 해결하는 방법은 그 문제를 나눠지지 않을 때까지 작은 문제들로 나누는 것이다.
    - 그렇게 큰 문제가 작은 문제들로 분할되면, 그 작은 문제들을 각각 해결한다.
    - 하나의 일을 하기 위해, 우리는 많은 객체를 만들어내고, 그 객체는 작은 일들을 해내며 다른 객체들과 상호작용을 한다.
- **자율적인 객체란 상태와 행위를 함께 지니며, 스스로 자기 자신을 책임지는 객체를 의미한다.**
    - 스스로가 자기 자신을 책임진다는 말은 무슨 말인지 잘 모르겠다.
    - 상태와 행위를 함께 지닌다. 행위를 위해 필요한 상태라면, 상태는 필요할 듯 하다. 이 정도의 의미일까. 재판에서의 판결이란 행위를 수행하기 위해서는 판사라는 상태가 필요한 것처럼.
- **객체는 시스템의 행위를 구현하기 위해 다른 객체와 협력한다. 각 객체는 협력 내에서 정해진 역할을 수행하며 역할은 관련된 책임의 집합이다.**
    - '협력 내에서', '정해진 역할을'
        - 이 말은 같이 일을 하기 위해서 위의 큰 문제를 작은 문제로 나누고, 그 작은 문제들을 위해 부여된 각각의 작은 책임, 그리고 그 책임에 기반한 역할을 의미하는 것이 아닐까?
- **객체는 다른 객체와 협력하기 위해 메시지를 전송하고, 메시지를 수신한 객체는 메시지를 처리하는 데 적합한 메서드를 자율적으로 선택한다.**
    - 메세지를 전송한다, 어떤 interface 를 통해 객체에게 요청한다. 어떤 일을 해달라고.
    - 그러면 그 객체는 그 일을 한다. 알아서.
    - 돈을 주고 커피를 만들어달라는 운동을 가기 전의 나와 커피숍의 직원분을 생각해보자.
        - 내가 그 직원분에게 여러가지 요청을 일일히 하진 않는다.
            - 샷을 내려주세요.
            - 샷에 꿀을 섞어주세요.
            - 기본 사이즈 컵에 얼음을 담아주세요.
            - 얼음을 담은 다음, 샷을 넣어주세요.
            - 얼음이 넘치지 않게, 컵에 물을 넣어주세요.
            - 저에게 전달해주세요.
        - 그냥 나는, "아이스 꿀 커피 하나 주세요" 라고 한다.
    - 그런 것처럼, 객체는 '역할' 과 '책임' 이 있는 것이고, 그래서 '자율' 이 있으며, '협력' 이 있을 뿐이다.
    - `Class` 라는건 이 역할과 책임이 가능하게끔 지정해 놓은 틀 같은 것이고, 그 뒤의 본질을 보면 이러하다.
## 협력하는 객체들의 공동체
객체지향의 목표는 실세계를 모방하는 것이 아니다. 오히려 새로운 세계를 창조하는 것이다. 소프트웨어 개발자의 역할은 단순히 실세계를 소프트웨어 안으로 옮겨 담는 것이 아니라 고객과 사용자를 만족시킬 수 있는 신세계를 창조하는 것이다.
<br>
객체지향에서 가장 중요한 개념은 역할, 책임, 협력 이다.

* 협력: 협력의 성공은 특정한 역할을 맡은 각 개인이 얼마나 요청을 성실히 이행하는가에 달려 있다.
* 역할과 책임: 역할이라는 단어는 의미적으로 책임이라는 개념을 내포한다. 따라서 특정한 역할은 특정한 책임을 암시한다.
<hr>

## 역할, 책임, 협력
객체지향 설계라는 예술은 적절한 객체에서 적절한 책임을 할당하는 것에서 시작된다. 역할은 유연하고 재사용 가능한 협력 관계를 구축하는데 중요한 설계 요소다. 대체 가능한 역할과 책임은 객체지향 패러다임의 중요한 기반을 제공하는 다형성과도 깊이 연관되어 있다.

    다형성: 동일한 요청에 대해 서로 다른 방식으로 응답할 수 있는 능력을 다형성(polymorphism) 이라고 한다.
<hr>

## 협력 속에 사는 객체
협력 공동체의 일원으로서 객체는 다음과 같은 두가지 덕목을 갖춰야 한다.
<br>
첫째, 객체는 충분히 '협력적'이어야 한다. 객체는 다른 객체의 명령에 복종하는 것이 아니라 요청에 응답할 뿐이다.
<br>
두번째, 객체가 충분히 '자율적'이어야 한다는 것이다. '자율적'이라는 단어의 뜻은 '자기 스스로의 원칙애 따라 어떤 일을 하거나 자기 스스로를 통제하여 절제하는 것'을 의미한다.
<br><br>
객체지향 설계의 묘미는 다른 객체와 조화롭게 협력할 수 있을 만큼 충분히 개방적인 동시에 협력에 참여하는 방법을 스스로 결정할 수 있을 만큼 충분히 자율적인 객체들의 공동체를 설계하는 데 있다.

### 상태와 행동을 함께 지닌 자율적인 객체
* 객체의 자율성은 객체의 내부와 외부를 명확하게 구분하는 것으로부터 나온다.
* 객체는 상태와 행위를 하나의 단위로 묶는 자율적인 존재다.
* 과거의 전통적인 개발 방법은 데이터와 프로세스를 엄격하게 구분한다. 이에 반해 객체지향에서는 데이터와 프로세스를 객체라는 하나의 틀 안에 묶어 놓음으로써 객체의 자율성을 보장한다.
* 자율적인 객체로 구성된 공동체는 유지보수가 쉽고 재사용이 용이한 시스템을 구축할 수 있는 가능성을 제시한다.

### 협력과 메시지
 * 객체지향의 세계에서 협력은 메시지를 전송하는 객체와 메시지를 수신하는 객체 사이의 관계로 구성된다. 이때 메시지를 전송하는 객체를 **송신자(sender)**라고 부르고 메시지를 수신하는 객체를 **수신자(receiver)**라고 부른다.

### 메서드와 자율성
* 메시지를 수신한 객체가 싱행 시간에 메서드를 선택할수 있다는 점은 다른 프로그래밍 언어와 객체지향 프로그래밍 언어를 구분 짓는 핵심적인 특징 중 하나다. 이것은 프로시저 호출에 대한 실행 코드를 컴파일 시간에 결정하는 절차적인 언어와 확연히 구분되는 특징이다.
* 메시지와 메서드의 분리는 객체의 협력에 참여하는 객체들 간의 자율성을 증진시킨다.
* 외부의 요청이 무엇인지를 표현하는 메시지와 요청을 처리하기 위한 구체적인 방법인 메서드를 분리하는 것은 객체의 자율성을 높이는 핵심 메커니즘이다. 이것을 **캡슐화(encapsulation)**라는 개념과도 관련돼 있다.
<hr>

## 객체지향의 본질
* 객체지향이란 시스템을 상호작용하는 **자율적인 객체들의 공동체**로 바라보고 객체를 이용해 시스템을 분할하는 방법이다.
* 자율적인 객체란 **상태**와 **행위**를 함께 지니며 스스로 자기 자신을 책임지는 객체를 의미한다.
* 객체는 시스템의 행위를 구현하기 위해 다른 객체와 **협력**한다. 각 객체는 협력 내에서 정해진 **역할**을 수행하며 역할은 관련된 **책임**의 집합이다.
* 객체는 다른 객체와 협력하기 위해 메시지를 전송하고, **메시지**를 수신한 객체는 메시지를 처리하는 데 적합한 **메서드**를 자율적으로 선택한다.

### 객체를 지향하라
* 코드를 담는 클래스의 관점에서 메시지를 주고받는 객체의 관점으로 사고의 중심을 전환하는 것이다.
* 클래스의 구조와 메서드가 아니라 객체의 역할, 책임, 협력에 집중하라.


참고 서적: http://www.yes24.com/Product/Goods/18249021?scode=032&OzSrank=1
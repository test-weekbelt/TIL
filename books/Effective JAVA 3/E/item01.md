# 생성자 대신 정적 팩터리 메서드를 고려하라
클래스는 클라이언트에 public 생성자 대신 (혹은 생성자와 함께) 정적 팩터리 메서드를 제공할 수 있다. 이 방식에는 장점과 단점이 모두 존재한다. 
장점
1.  이름을 가질 수 있다. 생성자에 넘기는 매개변수와 생성자 자체만으로는 반환될 객체의 특성을 제대로 설명하지 못한다. 반면 정적 팩터리는 이름만 잘 지으면 반환될 객체의 특성을 쉽게 묘사할 수 있다.
    ```java
    // 생성자 방식
    BigInteger(int, int, Random)

    // 팩터리 메서드 방식
    BigInteger.probablePrime
    ```
    생성자 방식보다 팩터리 메서드 방식이 '값이 소수인 BigInteger를 반환한다'는 의미를 더 잘 설명한다.
    <br>
    한 클래스에 시그니처가 같은 생성자가 여러 개 필요할 것 같으면, 생성자를 정적 팩터리 메서드로 바꾸고 각각의 차이를 잘 드러내는 이름을 지어주자.

2.  호출될 때마다 인스턴스를 새로 생성하지는 않아도 된다. 이 덕분에 불변 클래스는 인스턴스를 미리 만들어 놓거나 새로 생성한 인스턴스를 캐싱하여 재활용하는 식으로 불필요한 객체 생성을 피할 수 있다. 반복되는 요청에 같은 객체를 반환하는 식으로 정적 팩터리 방식의 클래스는 언제 어느 인스턴스를 살아 있게 할지를 철저히 통제할 수 있다.
<br><br>
인스턴스를 통제하면 클래스를 싱글턴으로 만들 수도, 인스턴스 불가로 만들수도 있다. 또한 불변 값 클래스에서 동치인 인스턴스가 단 하나뿐임을 보장할 수 있다(a == b일 때만 q.equals(b)가 성립).

3. 반환 타입의 하위 타입 객체를 반환할 수 있는 능력이 있다. 이 능력은 반환할 객체의 클래스를 자유롭게 선택할 수 있게 하는 '엄청난 유연성'을 선물한다.

    
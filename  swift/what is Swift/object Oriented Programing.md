# 객체지향
> 현대 프로그래밍 언어에서 대부분 차용하고 있는 객체지향 프로그래밍 패러다임에 대해 알아 보겠습니다.

<br>

**객체지향 프로그래밍 패러다임** 

[객체지향 프로그래밍 패러다임](https://ko.wikipedia.org/wiki/객체_지향_프로그래밍)은 컴퓨터 프로그래밍 패러다임의 한 종류로 객체지향 프로그래밍 ( Object Oriented Programing. OOP)이라고도 불립니다. 객체지향 프로그래밍은 컴퓨터 프로그램을 명령어의 목록으로 보는 기존의 명령형 프로그래밍 패러다임의 시각에서 벗어나 여러 개의 독립된 단위인 객체의 모임으로 파악하고자 하는 시각입니다. 각각의 객체는 서로 메시지를 주고 받고 데이터를 처리할 수 있습니다.

<br>

객체지향 프로그래밍은 프로그램을 유연하고 쉽게 변경할 수 있도록 작성할 수 있어 대규모 소프트웨어 개발에 많이 사용됩니다. 또한 객체만 잘 이해하면 프로그래밍을 더 쉽게 배울 수 있고, 소프트웨어 개발과 유지보수를 간편하게 할 수 있으며, 직관적으로 코드를 분석할 수 있다는 장점이 있습니다. 소프트웨어 공학의 관점에서 소프트웨어의 질을 향상하려면 강한 응집력(Strong Cohesion)과 약한 결합력(Weak Coupling)을 지향해야 합니다. 객체지향 프로그래밍은 클래스에 하나의 문제 해결을 위한 데이터와 메서드를 모아놓은 방식으로 응집력을 강화합니다. 또, 각 클래스는 독랍적이 되도록 디자인해 결합력을 약화합니다. 그러나 실제 세계의 모습을 프로그램안에 구현하고자 했던 객체지향 프로그래밍 패러다임이지만, 지나친 프로그램의 객체화 경향 때문에 오히려 실제 세계의 모습을 그대로 반영하기 어렵다는 비판을 받기도 합니다.

<br>

객체지향 프로그래밍의 주요 특징으로는 자료 추상화, 상속, 다형성, 동적 바인딩 등이 있으며 객체지향 프로그래밍 패러다임을 차용한 언어에는 스몰토크(smalltalk), Objective-C, C++, C#, 자바, 파이썬, 루비, 스위프트(swift)등이 있습니다.

**클래스와 객체**
>클래스와 객체의 관계를 살펴보기 전에 객체지향 프로그래밍에서 주요하게 다루는 용어를 먼저 알아보겠습니다.
- 클래스(Class): 같은 종류(또는 문제 해결을 위한)의 집단에 속하는 속성과 행위를 정의한 것입니다. 객체지향 프로그램의 기본 사용자 정의 데이터 타입이라고 할 수 있습니다. 클래스는 다른 클래스 또는 외부 요소와 독립적으로 디자인되어야 합니다.
- 객체(Object): 클래스의 인스턴스(실제로 메모리에 할당되어 동작하는 모양을 갖춘 것, instance)입니다. 객체는 자신 고유의 속성이 있으며 클래스에서 정의한 행위를 할 수 있습니다. 스위프트에서는 '객체'라는 용어보다는 '클래스의 인스턴스'라는 표현을 사용합니다.
- 메서드(Method)또는 메시지(Message): 객체가 클래스에 정의된 행위를 실질적으로 하는 함수입니다. 메서드(메시지)를 통해 객체에 명령을 전달할 수 있습니다. 객체 간에 명령 전달 또는 데이터 전달은 메서드(메시지)를 통해 이루어지며 명령을 전달하거나 데이터를 전달하는 행위를 '메서드를 호출한다'또는 '메시지를 전달한다'라고 표현합니다.
<br>

스위프트에서 작성한 객체지향 프로그래밍 패러다임을 차용하여 코드를 작성한 예입니다.
```swift
class SomeClass {
    var someProperty:Any = 1
    func someMethod(){
        //some task...
    }
}
let myInstance: SomeClass = SomeClass()
//SomeClass라는 이름의 클래스의 이니셜라이저를 호출하여
//myInstance라는 이름의 상수에 할당합니다.
//클래스의 이니셜라이저를 통해 메모리에 할당되고 초기화한 객체를 우리는 인스턴스라고 부릅니다.
myInstance.someProperty = 100 //인스턴스의 프로퍼티에 값을 할당할 수도 있고
print(myInstance.someProperty)//값을 가져올 수도 있습니다.

myInstance.someMethod() //인스턴스의 메서드를 호출하여 작업을 수행하도록 할 수 있습니다. 
```
>코드를 보면 알 수 있듯이 스위프트뿐만 아니라 객체지향 프로그래밍 패러다임을 차용한 언어는 필수로 명령형 프로그래밍 패러다임을 사용합니다. 프로퍼티, 변수 등에 해당하는 메모리 값의 변화(상태변화)가 있기 때문입니다.
<br>

>클래스는 객체가 만들어지기 위한 청사진으로 비유할 수 있습니다. 클래스는 실제 메모리에 객체를 할당해 인스턴스를 만들기 위한 일종의 설계코드입니다. 클래스에 구현된 코드대로 실제로 객체가 메모리에 올라가 활동하게 됩니다. 클래스에 정의된 모양대로 객체가 생성되고 객체 간의 메시지를 통해 프로그램의 각 명령이 실행됩니다. 
<br>

 >객체지향 프로그래밍에서 클래스와 객체는 매우 중요한 개념이므로 꼭 이해하고 넘어가야 합니다. 객체지향 프로그래밍을 처음 접하는 독자라면 '2부 객체지향 프로그래밍과 스위프트'까지 읽은 다음 '클래스와 객체'를 다시 읽어보기를 추천합니다.
# 8월 20일 CS
## 절차지향 프로그래밍과 객체지향 프로그래밍

- 절차지향 프로그래밍 : 순차적인 처리를 중요시 하며, 프로그램 전체가 유기적으로 연결되도록 하는 프로그램
   - 각 단계를 함수나 프로시저(Procedure)로 구분하여 실행하는 방식이다.
   - 여기서 프로시저에는 루틴, 서브루틴, 함수 등이 포함된다.
      - 서브루틴이란 main 문 밖에서 정의한 코드 블럭 중 return 값이 없는 것을 의미한다.
   - 장점 : 컴퓨터의 처리방식이랑 유사하여 실행 속도가 비교적 빠르다.
   - 단점 : 처리 과정이 유기적으로 연결되어 있어 유지보수에 어려움이 있다. 
- 객체지향 프로그래밍 : 프로그램을 명령어의 목록으로 보는 것이 아닌, 여러 개의 객체로 구성되어 있다고 파악하는 것
   - 각각의 객체는 메시지를 주고받고, 데이터를 처리할 수 있다.
   - 객체(Object) : 데이터와 기능을 묶어서 생각하는 형태
   - 장점 : 코드의 재사용성이 높아지며, 유지보수에 용이하다. 가독성이 높으며, 대형프로젝트에 적합하다.
   - 단점 : 절차지향 프로그래밍보다 속도가 느리다. 객체가 많아지면 용량이 커진다.


# 8월 24일 SOLID 원칙
## SOLID
- **SOLID** : 객체지향 프로그래밍에서의 다섯 가지 기본 원칙을 두문자어 기억술로 소개한 것.
   1. 단일 책임 원칙 SRP (Single Responsibility Principle)
   2. 개방-폐쇄 원칙 OCP (Open/Closed Principle)
   3. 리스코프 치환 원칙 LSP (Liskov Substitution Principle)
   4. 인터페이스 분리 원칙 ISP (Interface Segregation Principle)
   5. 의존관계 역전 원칙 DIP (Dependency Inversion Principle)

### 단일 책임 원칙 SRP
- 모든 클래스는 하나의 책임만 가지며, 클래스는 그 책임을 완전히 캡슐화해야한다.
- 클래스의 수정이 한 가지 책임에 집중되며, 클래스가 더욱 강화된다.
- **객체가 커지는 것을 막는다.**

### 개방-폐쇄 원칙 OCP
- 소프트웨어 개체(클래스, 모듈, 함수 등)는 확장에 대해 열려 있어야 하고, 수정에 대해 닫혀 있어야 한다.
   - 새로운 기능을 추가할 때 **기존 코드를 수정하지 않고 확장**할 수 있어야 한다.

### 리스코프 치환 원칙 LSP
- 자료형 S가 자료형 T의 서브타입이라면 필요한 프로그램의 속성의 변경 없이 자료형 T의 객체를 자료형 S로 치환할 수 있어야 한다.
   - 상위 타입이 하위 타위 타입으로 교체가 가능해야 한다. 
   - **부모 클래스를 상속한 자식 클래스가 부모 클래스의 모든 기능을 사용할 수 있어야 한다.**
- **다형성 구현**을 뒷받침하는 원칙이다.

### 인터페이스 분리 원칙 ISP
- 클라이언트(혹은 객체)는 자신이 이용하지 않은 메서드에 의존하지 않아야 한다.
- 통상적인 기능을 갖기 보다는, 여러 개의 세부적인 기능을 갖게!
- **객체가 커지는 것을 막는다.**

### 의존관계 역전 원칙 DIP
- 상위 모듈은 하위 모듈에 의존해서는 안되며, 둘 다 추상화에 의존해야 한다.
- 추상화는 세부 사항에 의존해서는 안된다. 그 반대가 되어야 한다.
- 여기서 세부사항은 변하기 쉬운 것, 추상화는 변하기 어려운 속성이다.
- **즉, 상위와 하위 객체 모두가 동일한 추상화에 의존해야 한다.**
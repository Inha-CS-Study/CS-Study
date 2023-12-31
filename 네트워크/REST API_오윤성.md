# RestAPI

API란 무엇일까요?

Application Programming Interface의 줄임말 입니다.

인터페이스는 두 애플리케이션 간 서비스 계약이라고 할 수 있습니다. 

### Interface란?

인터페이스는 서로 다른 두 개 이상의  컴포넌트가 서로 통신할 수 있게 하는 매개체 입니다.

예를 들어 사용자가 장치에 연결된 카메라를 사용하기 위해서는 운영체제를 통해 사용 허가를 받아야 합니다. 

운영체제는 카메라를 키는 시스템 콜을 호출할 수 있도록 아이콘을 제공합니다. 이 때 이 아이콘은 유저와 운영체제가 서로 통신할 수 있도록 도와주는 하나의 인터페이스 입니다. 

인터페이스를 한마디로 정리해보자면, 인터페이스는 서로 다른 컴포넌트가 서로 통신할 수 있게 도와주는 것입니다.

### API란?

> Application Programming Interface의 약자로 서로 다른 두 시스템이나 컴포넌트가 통신하고 상호 작용하기 위한 규약 또는 인터페이스를 제공하는 것입니다.
> 

예를 들어, A 웹페이지에서 제공하는 데이터를 B 앱에서 사용하고자 할 때, B 앱은 A가 정해둔 규칙에 따라 데이터를 요청해야 합니다. 따라서 API는 시스템 간 데이터 교환을 위한 규칙 또는 인터페이스입니다. 

한 프로그램에서 다른 프로그램으로 데이터를 주고받기 위한 방법

예를 들면, API란 식당 메뉴판이라고 생각하면 됩니다.

김치찌개 식당가서 주문할 때 김치찌개에 밥말아주세요가 아니라 메뉴판에 보고 거기에 적힌 메뉴들을 정확하게 주문합니다. 여기서 메뉴판이 API입니다. 식당 주인과 손님이 음식을 주고받기 위한 하나의 방법이라고 생각하면 됩니다. 

예를 들어 웹툰을 보여주는 프로그램을 만들었다고 하겠습니다. 이때 먼저 메뉴판을 만들어야합니다. 왜냐면 유저가 커스텀해서 날라다니는 자동차가 나오는 웹툰 보여줘 라고  커스텀 주문을 할 수 있습니다. 하지만 우리는 그런 웹툰이 없습니다. 그래서 메뉴판을 먼저 만들어야합니다.

나는 A웹툰, B웹툰, C웹툰을 보여줄 수 있습니다. 라고 메뉴판에 만들어 둬야 합니다. 

그래야 서비스가 가능합니다. 이처럼 식당하고 똑같습니다. 

실제 앱 서비스, 웹서비스에서 사용하는 API라는 용어는 그냥 유저와 서버가 데이터 주고받는 정확한 방법이라고 할 수 있습니다. 

서비스를 하기 위해서 만들어둔 하나의 메뉴판이라고도 할 수 있습니다. 

그러면 여기서 말하는 방법은 무엇일까요?

방법은 하나의 코드입니다.

웹툰을 보여주는 프로그램을 만들었을 때, 유저가 A 웹툰 보여줘 라는 요청을 어떻게 보낼까요?
해킹을 해서 만들어둔 코드를 실행하지 않는 이상 유저는 A웹툰을 볼 수 없습니다. 

그래서 이 프로그램을 실행시키는 방법을 

app.get(’/detail/:id’, …) 이 url로 get 요청을 하면 안에있는 코드를 실행해 주세요 라는 뜻인데 이 코드가 api라고 보면 됩니다.

### REST API란?

Representational State Transfer Application Programming Interface의 약자로

HTTP 프로토콜을 기반으로 클라이언트와 서버 간에 데이터를 주고받고, 서로 상호 작용하기 위한 규칙과 규격을 정의한 것입니다. REST API는 자원(리소스)을 나타내는 URL과 HTTP 메서드(GET, POST, PUT, DELETE 등)를 사용하여 데이터를 처리하고 관리합니다. 이를 통해 클라이언트와 서버 간의 효율적인 통신과 데이터 교환을 가능하게 합니다.

각 요청이 어떤 정보나 동작을 위한 것인지 그 모습 자체만으로도 추론이 가능하다는 것입니다. 

REST는 문서, 그림, 데이터 등의 자원을 이름으로 구분해서 해당 자원에 대한 상태, 정보를 주고 받는 것을 의미합니다. 

또한 HTTP 메서드를 활용해서 해당 자원에 대한 CRUD를 적용하는 것을 의미합니다. 

리뷰 데이터 전체 요청 GET /api/reviews

리뷰 상세 데이터 요청 POST /api/reviews/{id}

리뷰 상세 데이터 

누가봐도 각 요청이 어떤 동작이나 정보를 위한 것인지 그 요청의 모습 자체만으로 추론이 가능합니다.  REST의 가장 중요한 특성입니다. 

정리하면 REST API는 HTTP 요청을 할 때 어떤 URI에 어떤 메서드를 사용할지에 대한 개발자들 사이에서 널리 사용되어지는 약속입니다. 

### REST API의 특징

- 무상태성 : 서버가 각 클라이언트의 상태 정보를 저장하지 않는 것을 의미합니다.
- 각 요청을 독립적으로 처리하며, 이전 요청과 관련된 상태 정보를 서버에 저장하지 않습니다. 각 요청은 모든 필요한 정보를 포함하고 있어야 하며, 서버는 요청에 따라 즉시 응답합니다. 이는 서버의 부담을 줄이고 확장성을 높이는 데 도움이 됩니다.
    - 장점 : 대량의 트래픽에 강함
    - 단점 : 매번 요청할 때마다 모든 정보를 보내야 하니까 데이터가 많이 소모됨.
# 인터넷

## 인터넷 작동 원리

### Network에 대해

두 개의 컴퓨터가 통신이 필요할 때, 유선(이더넷 케이블)이나 무선(WiFi, Bluetooth)로 연결되어야한다.

![단순한 네트워크](https://mdn.mozillademos.org/files/8443/internet-schema-2.png)

그러나, 모든 컴퓨터끼리 연결할려고 한다면 다음과 같이 선들이 매우 복잡해진다.

이를 해결하기 위해서, **라우터** 라고 하는 **특수 소형 컴퓨터** 에 연결된다. 라우터가 하는 유일한 작업은 컴퓨터에게 보낸 메시지가 올바른 컴퓨터에 도착하는 지 확인하는 작업이다.

이러한 라우터는 라우터끼리 연결되며 다음과 같이 구성 된다.

![라우터가 있는 네트워크](https://mdn.mozillademos.org/files/8449/internet-schema-5.png)

그러나 라우터로는 아주 먼거리에 케이블을 연결할 수는 없습니다. 그래서 이미 연결되어 있는 전화선 기반의 시설을 사용합니다. 네트워크와 전화시설을 연결하기 위해서는 **모뎀** 을 사용합니다.

이렇게 네트워크가 전화 시설에 연결한 후, 우리의 네트워크에서 도달하려는 먼 네트워크로 메세지를 보내기 위해서는 네트워크를 **인터넷 서비스 제공 업체 (Internet Service Provider, ISP)** 에 연결합니다. 이러한 ISP는 모두 함께 연결되는 몇몇 특수한 라우터를 관리하고 다른 ISP의 라우터에도 액세스할 수 있는 회사입니다.

![ISP, 모뎀을 사용한 네트워크](https://mdn.mozillademos.org/files/8453/internet-schema-7.png)

인터넷은 이러한 전체 네트워크 인프라로 구성됩니다.

### 컴퓨터 찾기

- IP 주소 : 특정 컴퓨터의 고유한 주소. (프로토콜)
- 도메인 이름 : 사람이 읽을 수 있는 IP 주소의 이름 (ex. 173.194.121.32 -> google.com)

### 인터넷과 웹

- 인터넷 : 수십억 대의 컴퓨터를 모두 연결하는 기술 인프라
  - 컴퓨터 중 일부는 '웹 서버'로 웹 브라우저가 이해할 수 있는 서비스를 제공
- 웹 : 그 인프로 기반 위에 구축된 서비스
  - 그 외의 구축된 다른 서비스로는 이메일, IRC(릴레이챗) 등이 있다.


출처 : https://developer.mozilla.org/ko/docs/Learn/Common_questions/How_does_the_Internet_work

---

## 웹 작동 원리

### 클라이언트와 서버

![클라이언트와 서버](https://mdn.mozillademos.org/files/8973/Client-server.jpg)

- 클라이언트는 일반 웹 사용자의 인터넷이 연결된 장치에 연결되어 있고, 이러한 장치들에서 이용가능한 웹에 접근하는 소프트웨어
- 서버는 웹페이지, 사이트, 앱을 저장하는 컴퓨터. Client의 Device가 웹페이지에 접근하기 원할 때, 서버로부터 클라이언트의 장치로 사용자의 웹 브라우저에서 보여지기 위한 웹페이지의 사본이 다운된다.

### 도구 상자의 다른 부분들

간단한 그림으로는 다음과 같다.

> 클라이언트(집) --- 도로(웹) --- 서버(상점)

#### 용어에 대한 정의는 다음과 같다.

- 인터넷 연결 : 웹에서 데이터를 보내고 받을 수 있게 해줌. 도로와 같음.
- TCP/IP : Transmission Control Protocol(전송 제어 규약)과 Internet Protocol(인터넷 규약)은 데이터가 어떻게 웹을 지나는지 정의하는 통신 규약이다. 이는 주문을 하고 상점에 가고, 살 수 있게 해주는 운송 장치와도 같다.
- DNS : Domain Name System Servers (도메인 이름 시스템 서버)는 웹사이트를 위한 주소록과 같다. 브라우저에 웹 주소를 입력할 때, 브라우저는 그 웹사이트를 검색하기 전에 DNS를 살펴본다. 브라우저는 HTTP 메시지를 올바른 장소로 전송하기 위해 그 웹사이트가 있는 서버가 어떤 것인지를 찾아야한다. 이는 상점의 주소를 찾아보는 것과 비슷하다.
- HTTP : Hypertext Transfer Protocol(하이퍼텍스트 전송 규약)은 클라이언트와 서버가 서로 통신할 수 있게 하기 위한 언어를 정의하는 어플리케이션 규약이다. 이는 상품을 주문하기 위해 사용하는 양식(언어)과 같다.
- 컴포넌트 파일 : 한 웹사이트는 상점에서 다양한 종류의 상품들과 같이 많은 다른 파일들로 만들어진 것 처럼, 여러 파일로 구성된다.
  - 코드 파일 : HTML, CSS, JS
  - 자원 : 이미지, 음악, 비디오, 단어 문서, PDF 등등

### 브라우저에 웹 주소를 입력할 때, 발생하는 과정은?
> 상점으로 걸어가는 것과 유사함.

1. 브라우저는 DNS 서버로 가서 웹사이트가 있는 서버의 진짜 주소를 찾습니다. (여러분이 상점의 주소를 찾는다.)
2. 그 다음 브라우저는 서버에게 웹사이트의 사본을 클라이언트에게 보내달라는 HTTP 요청 메세지를 서버로 전송합니다. (상점으로 가서 상품을 주문한다.) 이 메세지, 그리고 클라이언트와 서버 사이에 전송된 모든 데이터는 TCP/IP 연결을 통해서 전송한다.
3. 이 메세지를 받은 서버는 클라이언트의 요청을 승인하고, "200 OK" 메세지를 클라이언트에게 전송합니다. "200 OK"는 성공이라는 의미다. 다음 서버는 웹사이트의 파일들은 데이터 패킷이라 불리는 작은 일련의 덩어리들을 브라우저에 전송하기 시작한다.
4. 브라우저는 작은 덩어리들은 완전한 웹 사이트로 조립하고, 보여준다.


### DNS (Domain Name System)

DNS는 브라우저에 입력하는 웹주소 (ex. google.com)을 웹사이트의 실제(IP) 주소에 맞춰주는 특별한 서버.

IP 확인하는 방법
- [IP Checker](https://ipinfo.info/html/ip_checker.php) 등을 통해서 도메인을 체크할 수 있다.
- Shell에서  `whois {DNS}` 입력해서 정보 받아오기.


### 패킷 설명

기본적으로, 데이터가 웹을 거쳐서 전송될 때, 수천개의 작은 덩어리들로 전송됩니다. 그래서 다양한 웹 사용자들은 동시에 같은 웹 사이트를 다운로드 할 수 있게 됩니다.

만약 웹 사이트가 하나의 큰 덩어리들로 전송된다면, 오직 한 번에 하나의 사용자만 다운로드 할 수 있을 것이다. 이는 웹을 매우 비효율적이고, 사용하기 불편하게 만든다.

출처 : https://developer.mozilla.org/ko/docs/Learn/Getting_started_with_the_web/%EC%9B%B9%EC%9D%98_%EB%8F%99%EC%9E%91_%EB%B0%A9%EC%8B%9D

---

## HTTP와 HTTPS

볼 자료.

- [HTTP - basic introduction](https://dev.opera.com/articles/http-basic-introduction/)
- [HTTP - Let's GET IT On!](https://dev.opera.com/articles/http-lets-get-it-on/)
- [HTTP - Response Codes](https://dev.opera.com/articles/http-response-codes/)



---

## 브라우저와 동작 원리

### 브라우저의 주요 기능

> 브라우저의 주요 기능은 사용자가 선택한 자원을 서버에 요청하고 브라우저에 표시하는 것이다. 자원은 보통 HTML 문서지만 PDF나 이미지 또는 다른 형태일 수 있다. 자원의 주소는 URI(Uniform Resource Identifier)에 의해 정해진다.

브라우저 W3C에 정해진 명세에 따라 HTML, CSS 작성한다. 대부분은 표준 명세를 따르며 다음과 같은 요소가 포함된다.
- URI를 입력할 수 있는 주소 표시줄
- 이전 버튼과 다음 버튼
- 북마크
- 새로 고침 버튼과 현재 문서의 로드를 중단할 수 있는 정지 버튼
- 홈 버튼

그러나 사용자 인터페이스는 표준 명세가 없습니다.

### 브라우저의 기본 구조

주요 구성 요소는 다음과 같습니다.
- 사용자 인터페이스 - 주소 표시줄, 이전/다음 버튼, 북마크 메뉴 등. 요청한 페이지를 보여주는 창을 제외한 나머지 모든 부분이다.
- 브라우저 엔진 - 사용자 인터페이스와 렌더링 엔진 사이의 동작을 제어.
- 렌더링 엔진 - 요청한 콘텐츠를 표시. 예를 들어 HTML을 요청하면 HTML과 CSS를 파싱하여 화면에 표시함.
- 통신 - HTTP 요청과 같은 네트워크 호출에 사용됨. 이것은 플랫폼 독립적인 인터페이스이고 각 플랫폼 하부에서 실행됨.
- UI 백엔드 - 콤보 박스와 창 같은 기본적인 장치를 그림. 플랫폼에서 명시하지 않은 일반적인 인터페이스로서, OS 사용자 인터페이스 체계를 사용.
- 자바스크립트 해석기 - 자바스크립트 코드를 해석하고 실행.
- 자료 저장소 - 이 부분은 자료를 저장하는 계층이다. 쿠키를 저장하는 것과 같이 모든 종류의 자원을 하드 디스크에 저장할 필요가 있다. HTML5 명세에는 브라우저가 지원하는 '웹 데이터 베이스'가 정의되어 있다.

![브라우저의 주요 구성요소](https://d2.naver.com/content/images/2015/06/helloworld-59361-1.png)


출처(좀 더 자세히) : https://d2.naver.com/helloworld/59361

---


## DNS의 작동원리

### Domain 구조

- 인터넷상에서 사용되는 도메인은 전 세계적으로 고유하게 존재하는 이름
- 정해진 규칙 및 체계에 따라야 하며, 임의로 변경되거나 생성될 수 없음.
- 인터넷상의 모든 도메인은 ".(dot)" 또는 루트(root)라 불리는 도메인 아래에 그림과 같이 나무를 거꾸로 위치시킨 역트리(Inverted tree)구조로 계층적으로 구성되어 있음
- 루트 도메인 바로 아래의 단계를 1단계 도메인 또는 최상위도메인(TLD, Top Level Doamin)이라고 부르며, 그 다음 단계를 2단계 도메인, 차상위도메인(SLD, Second Level Domailn)이라고 함
- 도메인은 일반최상위도메인(gTLD: Generic Top Level Domain)과 국가최상위도메인(ccTLD: Country Code Top Level Domain)로 구분할 수 있으며 여기서 일반최상위도메인은 다시 스폰서도메인(Sponsored TLD)과 언스폰서도메인(Unsponsored TLD)으로 구분됩니다.

![image](https://user-images.githubusercontent.com/42582516/95797353-4b6aa580-0d2a-11eb-9d14-ea3c4dd6abb9.png)


### DNS 서비스 유형

#### 신뢰할 수 있는 DNS
신뢰할 수 있는 DNS 서비스는 개발자가 퍼블릭 DNS 이름을 관리하는 데 사용하는 업데이트 메커니즘을 제공합니다. 이를 통해 DNS 쿼리에 응답하여 도메인 이름을 IP 주소로 변환합니다. 그러면 컴퓨터가 서로 통신할 수 있게 됩니다. 신뢰할 수 있는 DNS는 도메인에 대해 최종 권한이 있으며 재귀적 DNS 서버에 IP 주소 정보가 담긴 답을 제공할 책임이 있습니다.

#### 재귀적 DNS
대개 클라이언트는 신뢰할 수 있는 DNS 서비스에 직접 쿼리를 수행하지 않습니다. 대신에 해석기 또는 재귀적 DNS 서비스라고 알려진 다른 유형의 DNS 서비스에 연결하는 경우가 일반적입니다. 재귀적 DNS 서비스는 호텔 컨시어지와 같은 역할을 합니다. DNS 레코드를 소유하고 있지 않지만 사용자를 대신해서 DNS 정보를 가져올 수 있는 중간자의 역할을 합니다. 재귀적 DNS가 일정 기간 동안 캐시된 또는 저장된 DNS 레퍼런스를 가지고 있는 경우, 소스 또는 IP 정보를 제공하여 DNS 쿼리에 답을 합니다. 그렇지 않다면, 해당 정보를 찾기 위해 쿼리를 하나 이상의 신뢰할 수 있는 DNS 서버에 전달합니다.

### DNS 동작 원리

![DNS 동작 원리](https://user-images.githubusercontent.com/42582516/95796986-4822ea00-0d29-11eb-955d-07ffe6b426ee.png)

이 순서를 정리하려면 다음과 같다.

1. 웹 브라우저에 www.naver.com을 입력하면 먼저 Local DNS에게 "www.naver.com"이라는 hostname"에 대한 IP 주소를 질의하여  Local DNS에 없으면 다른 DNS name 서버 정보를 받음(Root DNS 정보 전달 받음)
2. Root DNS 서버에 "www.naver.com" 질의
3. Root DNS 서버로 부터 "com 도메인"을 관리하는 TLD (Top-Level Domain) 이름 서버 정보 전달 받음
4. TLD에 "www.naver.com" 질의
5. TLD에서 "name.com" 관리하는 DNS 정보 전달
6. "naver.com" 도메인을 관리하는 DNS 서버에 "www.naver.com" 호스트네임에 대한 IP 주소 질의
7. Local DNS 서버에게 "응! www.naver.com에 대한 IP 주소는 222.122.195.6 응답 
8. Local DNS는 www.naver.com에 대한 IP 주소를 캐싱을 하고 IP 주소 정보 전\

---


## 도메인 네임

---


## 호스팅

호스팅이란 정보의 집약체인 서버의 전체 혹은 일부를 이용할 수 있도록 임대해 주는 서비스를 말합니다.
서버를 관리하기 위해서는 24시간 내내 안정적으로 전기를 공급해야 하고, 빠르고 안정적인 인터넷 회선을 사용해야 하며, 철저한 보안 시스템을 갖추고 있어야 합니다. 따라서 개인이 서버를 관리하기보다 전문 업체의 호스팅 서비스를 사용하는 것이 일반적입니다.

호스팅 업체는 다음과 같이 있다.

> ex) GoDaddy, Google Cloud Platform, 1&1, AWS 등등

### 호스팅의 종류

#### 1. 웹 호스팅

웹 호스팅은 여러 고객이 하나의 서버를 함께 사용하는 형태입니다. 하나의 서버를 나누어 쓰기 때문에 저렴하게 이용할 수 있고, 호스팅 업체의 통합 관리를 받기에 편리합니다. 그러나 사용할 수 있는 하드웨어가 제한적이라는 단점도 있습니다.

#### 2. 서버 호스팅

서버 호스팅은 고객이 단독 서버를 사용하는 형태입니다. 넓은 하드웨어 공간을 사용할 수 있고, 서버 운영/관리에 대한 직접적인 권한을 가질 수 있습니다. 또한, 빠른 데이터 전송 속도도 누릴 수 있지요. 하지만 단독으로 서버를 이용하는만큼 비용이 높은 편 입니다. 대기업이나 대형 포탈 혹은 대형 오픈마켓과 같이 많은 데이터를 사용하는 기업들이 사용하기 좋습니다. 

#### 3. 클라우드 서버

서버 호스팅을 가상화한 것으로, 가상 서버를 단독으로 사용할 수 있는 형태입니다. 고객이 필요할 때마다 서버 자원을 늘리거나 축소하여 유연하게 서버를 이용할 수 있습니다. 하지만 하나의 가상 서버에 문제가 생기면 연결된 다른 가상 서버에도 문제가 생길 수 있다는 단점이 있지요.


---



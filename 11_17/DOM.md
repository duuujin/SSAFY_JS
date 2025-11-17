# DOM(The Document Objects Model)
- 웹 페이지(Document)를 구조화된 객체로 제공하여 프로그래밍 언어가 페이지 구조에 접근할 수 있는 방법을 제공

# DOM API
- 다른 프로그래밍 언어가 웹 페이지에 접근 및 조작 할 수 있도록, 페이지 요소들을 객체 형태로 제공하며 관련된 메서드(Method)도 함께 제공
- HTML 구조와 내용을 조작하는 명령어 모음

# document 객체
- 웹 페이지를 나타내는 DOM 트리의 최상위 객체
- HTML 문서의 모든 콘텐츠에 접근하고 조작할 수 있는 진입점
- DOM에서 모든 요소, 속성, 텍스트는 하나의 객체
- 모두 document 객체의 하위 객체로 구성됨

# DOM tree
- HTML 태그를 나타내는 elements의 node는 문서의 구조를 결정
- 이들은 다시 자식 node를 가질 수 있음

# DOM 핵심
- 문서의 요소들을 객체로 제공하여 다른 프로그래밍 언어에서 접근하고 조작할 수 있는 방법을 제공하는 API

# 선택 메서드
- document.querySelector(selector)
    - 요소 한 개 선택
    - 제공한 선택자(selector)와 일치하는 첫 번째 요소를 하나 선택
    - 제공한 선택자를 만족하는 첫 번째 element 객체를 변환 (없다면 null 반환)
- document.querySelectorAll(selector)
    - 요소 여러 개 선택
    - 제공한 선택자와 일치하는 여러 element를 선택
    - 제공한 선택자를 만족하는 NodeList를 반환

# DOM 조작
1. 속성(attribute)조작
    - 클래스 속성 조작
    - 일반 속성 조작
2. HTML 콘텐츠 조작
3. DOM 요소 조작
4. 스타일 조작

# 속성 조작
1. 클래스(Class) 속성 조작
    - 스타일링 및 상태 제어를 위한 클래스 목록을 동적으로 추가/제거
2. 일반 속성(Attribute) 조작
    - id, href등 요소의 모든 HTML 속성 값을 직접 설정/조회
- classList 메서드
    - element.classList.add()
        - 지정한 클래스 값을 추가
    - element.classList.remove()
        - 지정한 클래스 값을 제거
    - element.classList.toggle()
        - 클래스가 존재한다면 제거하고 false를 반환(존재하지 않으면 클래스를 추가하고 true를 반환)

- 일반 속성 조작 메서드
    - Element.getAttribute()
        - 해당 요소에 지정된 값을 반환(조회)
    - Element.setAttribute(name, value)
        - 지정된 요소의 속성 값을 설정
        - 속성이 이미 있으면 기존 값을 갱신(그렇지 않으면 지정된 이름과 값으로 새 속성이 추가)
    - Element.removeAttribute()
        - 요소에서 지정된 이름을 가진 속성 제거

# DOM 요소 조작 메서드
- document.createElement( tagName )
    - 작성한 tagName의 HTML 요소를 생성하여 반환
- Node.appendChild()
    - 한 Node를 특정 부모 Node의 자식 NodeList 중 마지막 자식으로 삽입
    - 추가된 Node 객체를 반환
- Node.removeChild()
    - DOM에서 자식 Node를 제거
    - 제거된 Node를 반환

# 세미콜론(semicolon)
- 자바스크립트는 문장 마지막 세미콜론(';')을 선택적으로 사용 가능
- 세미콜론이 없으면 ASI에 의해 자동으로 세미콜론이 삽입됨
    - ASI (Automatic Semicolon Insertion, 자동 세미콜론 삽입 규칙)
- JavaScript를 만든 Brendan Eich 또한 세미콜론이 선택적이어야 한다고 생각(세미콜론을 강제하지 않는 스타일을 선호)
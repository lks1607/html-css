# Html

## 기본정의

    HTML: Hypertext markup language의 준말 (content가 어떻게 구성되어있는지 설명)

    브라우저가 text파일을 이해해서 웹사이트가 됨 (브라우저는 text파일임)
    브라우저는 2가지에서 3가지 text로 이루어져있음 (HTML / CSS / JavaScript)
    tag가 있고 그안에 content가 있음
    html lang="" - lang은 language의 준말 검색엔진들에게 도움되기 위해 사용 사이트 주된 언어를 알려주기 위해 사용
    <body>는 사용자가 볼 수 있는 content를 보여줌

### [html태그](https://developer.mozilla.org/ko/docs/Web/HTML/Element)

| head         | 웹사이트의 환경을 설정 / head 안 태그들은 html에서 보이지 않음                                            |
| ------------ | --------------------------------------------------------------------------------------------------------- |
| meta         | 부가적인 정보 / 요소는 title,base,link,style,script를 사용 표현할수없는 다양한 종류의 메타데이터를 나타냄 |
| meta         | enrodml attribute를 가지고 있음 / content,name 구성                                                       |
| meta         | meta property="og:image" content="" - 공유될떄 보여지는 이미지                                            |
| meta charset | 한글이나 다른 특수문자가 있는언어를 위해 meta charset=utf-8 은 잊지말고 넣을것                            |
| link         | rel="" type="" sizes="" href=""로 골라서 사용                                                             |

### tag

| tag | 브라우저가 content를 구별하기 위해 사용 태그는 열면 항상 닫아야함 |
| --- | ----------------------------------------------------------------- |
| h1  | header number 1 title에 사용 h1~h6까지 존재                       |
| ol  | ordered list(순서가 중요한경우)                                   |
| ul  | unordered list(순서가 중요하지 않은경우)                          |
| li  | list item / ol,ul태그의 목록을 만들어줌                           |
| a   | anchor / 링크태그 /a href="링크" target="\_blank"content/a        |
| img | image태그 /self-closeing tag / img src="링크"                     |

| form  | action="" method="" 사용                                                                |
| ----- | --------------------------------------------------------------------------------------- |
| input | input type="" 사용 placeholder="text 설명" disable사용시 클릭x required 사용시 필수입력 |
| type  | text, textarea, password, button, radio, select                                         |

# CSS

## 기본정의

    CSS: Cascading Style Sheet의 준말 (Html이랑 같이 사용)

    브라우저가 어떻게 보여야하는지 알려주는 역할 (브라우저 디자인)

    css는 같은대상을 적용할때 아래있는 것이 최종 적용

    css사용방법
    - html파일에 css코드를 넣는 방법
    - css파일을 만들어서 head에 넣는 s방법

```html
<link href="경로" rel="stylesheet" />
```

### 사용시 편한 엘리먼트

    :root{} : 기본적으로 모든 document의 뿌리
    - 변수를 지정할때 dash(-)2개 다음에 dash 1개 그리고 변수 이름 빈공간이 있을경우 dash사용
    - 변수를 사용할때는 var(변수이름)

    ex)
    :root{ --main-color: #fcce00; } p{color: var(--main-color);}/ main-color를 정해서 컬러를 한번에 수정할때 사용하면 편함
    :root{ --default-border: 1px soild var(--main-color);} p{border: var(--default-border);}

### 모든요소를 이루는것은 box

    Display blcok은 옆에 요소가 못오지만
    inline은 옆에 요소가 올수있음 (span a image) 또한 높이와 넓이값을 가질수 없음
    inline은 padding은 사방으로 적용가능하지만 margin은 양옆으로만 적용
    margin : box가 가지고있는 속성 경계로 부터 바깥의 공간
    collapsing margins : 요소의 경계가 같은 때 일어나고 그 요소들이 하나의 margin이 됨(top,bottom만 됨)
    padding : box가 가지고있는 속성 경계로 부터 안쪽의 공간
    border : box의 경계

### flexbox는 3개의 규칙이있음

    자식 엘리먼트에는 아무것도 적지말고 부모만 적을것
    flex-direction : row, column에 따라 주축과 교차축이 바뀜
    justify-content : main-axis 메인축 (space-between, flex-start, flex-end)
    aline-items : cross-axis 교차축 (space-between, flex-start, flex-end)
    flexbox-wrap : default값은 nowrap으로 되어있음 wrap은 한줄에 들어가는만큼 최대한집어넣고 사이즈를 넘으면 다른줄로 넘어감

### position

    static: position 디폴트값 레이아웃 박스를 처음 위치하는 곳에 두는 것
    fixed : 레이어를 부수고 레이어 위에있을수 있음 (스크롤을 내려도 고정되어있음 ex: 넷플릭스 메인메뉴 )
    relative : 조금씩 오른쪽,왼쪽을 옮기고 싶을때 사용 (top left bottom right 사용가능 / 처음 위치에서 그 위치를 기준으로 옮김)
    absolute : 부모 박스 기준이 아니라 body기준으로 움직임 (absolute는 가장 가까운 relative부모 기준으로 이동시킴 부모 relative가없으면 body기준)

### pseudo selectors

    세부적으로 엘리먼트를 선택해주는 것 (css의 태그이름, ID의 # class의 .)
    ex) div:last-child / div:nth-child(적용할 숫자) / div:nth-child(even짝수/odd홀수)

    input::placeholder : placeholder를 스타일링 하고싶을때 사용
    p::selection : 드래그했을때 스타일링 하고 싶을때 사용
    p::first-letter : 문단 첫글자 스타일링 하고 싶을때 사용 / p::first-line : 문단 첫줄 스타일링

### combinator

    ex) p + span : p 다음에오는 span에게 적용 / p ~ span : p 다음에 오지않을때 span에게 적용
    p > span : 부모 바로 밑 자식의 관계
    input[조건] : 조건에 충족한 요소들을 변경 ex) input[type="password"], input:required

### state

    active(클릭되었을때), focus, focus-within(focus 상태인 자식을 가진 부모 엘리먼트에만 적용), hover, visited(링크를 클릭했을경우)
    ex) a:active

### color

    color 시스템

    16진수 color(hexadecimal color)
    ex) color:#fcce00;

    rgb방식 / rgba방식
    ex) color: rgb(red,green,blue); / color: rgba(red,green,blue,opacity);

## 구별하기

| 구별하기 | Id, Class로 지정하여 구별가능                         |
| -------- | ----------------------------------------------------- |
| ID       | 개체당 하나만 사용할수있음 (#Id값을 이용하여 사용)    |
| Class    | 여러가지 개체에서 사용가능 (.class값을 이용하여 사용) |

# Javascript

## 기본정의

    브라우저의 동적작용을 하는 역할

## 웹사이트 만들기

    웹사이트 만들때는 html / css 가 필요함

    1. 생성한 폴더 열기
    2. 폴더명은 소문자로 만들기 (대문자 x)
    3. 파일명도 폴더명과 같이 항상 소문자로 만들기
    4. 브라우저는 html파일에 오류가 있다고 알려주지 않음
    5. 현재 작업하고 있는 파일을 브라우저에 열어 놓을 것
    6. html은 tag는 text로 이루어져 있음
    7. html파일은 <!DOCTYPE html>로 시작해야함

```

```

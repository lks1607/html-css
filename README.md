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

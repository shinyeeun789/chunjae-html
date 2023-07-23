# HTML 학습하기
HTML5 학습을 위한 Repository 입니다.

## 📦 문서의 구조

html문서는 DTD를 선언하고, html 태그를 열고, 그 안에 head와 body로 구분하여 작성한다.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

### 1. 웹 문서의 유형을 지정하는 선언문
```html
<!DOCTYPE html>
```
- 문서 타입(DTD)
- 현재 문서가 HTML5 언어로 작성한 웹 문서라는 뜻을 가짐
<br>

### 2. 웹 문서의 시작을 알리는 `<html>`
```html
<html lang="en">
		...
</html>
```
- HTML 파일의 시작과 끝을 표시
- `lang` 속성으로 문서에서 사용할 언어를 지정 가능
    - 검색 사이트에서 특정 언어로 제한해 검색할 때 필요
  <span style='background-color: #f1f8ff'> ex) 검색 결과 중에서 ‘한국어로 된 문서’로 범위를 제한할 경우 <html lang=”ko”>인 문서를 우선 검색</span>
    - 화면 낭독기에서 웹 문서를 소리 내어 읽어 줄 때 해당 언어에 맞추어 발음이나 억양, 목소리 등을 다르게 할 수 있음
<br>

### 3. 웹 브라우저에 문서 정보를 알려주는 `<head>`
#### 3-1. title 태그
- 제목을 적어놓는 요소
#### 3-2. meta 태그
- 문서 관리를 위한 메타정보를 나타내는 요소
- 웹 브라우저에는 보이지 않지만 웹 문서와 관련된 정보를 지정할 때 사용
- 화면에 글자를 표시할 때 어떤 인코딩을 사용할지 지정하는 중요한 역할을 함
<br><br>

## 📦 HTML 태그
### 1. 문서 내용을 표현하는 태그
- 제목(Headline) `<h1> ~ <h6>`
- 단락(Paragraph) `<p>`
- 줄 바꿈(Link Break) `<br>`
- 가로줄(Horizontal Line) `<hr>`
- 작성된 형식 유지(Pre-formatted Text) `<pre>`
- 단락 인용(Block Quotation) `<blockquote>`
<br>

### 2. 다양한 텍스트 태그
- 텍스트 강조(Emphasis) `<em>`
- 강한 강조(Strong Emphasis) `<strong>`
- 작은 글자 `<small>`
- 하이라이트(Marked) 효과 `<mark>`
- 위 첨자(Superscript) `<sup>`
- 아래 첨자(Subscript) `<sub>`
> HTML5 문서 규약에서는 가급적 문서 출력 모양은 CSS를 사용하여 표현하는 것을 권장
<br>

### 3. 링크 태그
```html
<nav>
    <ul>     
        <li><a href="#ft"> 푸터로 이동 - 네임앵커 </a></li>
        <li><a href="mailto:tlsdpdms789@naver.com"> 이메일 보내기 </a></li>
        <li><a href="tel:010-1234-5678"> 전화걸기 </a></li>
        <li><a href="sms:010-1234-5678"> 문자 보내기 </a></li>
    </ul>
</nav>
```
- **하이퍼텍스트(HyperText)** : 서로 연관된 문서나 텍스트 조각들을 연결하여 원하는 정보를 찾아가도록 하는 것
- **하이퍼미디어(HyperMedia)** : 텍스트 뿐만 아니라 이미지, 그래픽, 비디오 등 멀티미디어 정보가 서로 연결되어 있는 것
- **노드** : HTML 문서나 멀티미디어 정보를 표현하는 기본 단위
- **앵커(anchor)** : 노드에 해당하는 HTML문서 내에서 링크의 출발점이나 도착점
<br>

### 4. 이미지 관련 태그
- **이미지 파일 종류** : 웹 브라우저에서 공통적으로 사용할 수 있는 이미지 파일은 `GIF, JPEG, PNG`가 있음
    - `GIF(Graphic Interchange Format)` : JPEG, PNG 보다 파일 크기가 작고, 자연스러운 장면을 표현하지 못함
    - `JPEG(Joint Photographic Experts Group)` : 복잡한 그림, 사진 등 색상을 많이 사용하는 이미지에 적합
    - `PNG(Portable Network Graphic)` : GIF와 JPEG 형식의 장점, 비압축 형식의 BMP 형식의 장점도 고려
    
    > 사진과 같이 색상의 개수가 많은 이미지를 다룰 때는 JPEG 형식이 적합하고, 색상의 개수가 적거나 간단한 도형으로 이루어진 이미지를 다룰 때는 GIF가 압축률이 높음
#### 4-1. `<img>`
```html
<img src="" alt="" title="">
```
- `alt` 속성은 무조건 넣어줘야 함
    - 웹 표준을 맞추기 위해서
    - 시각 장애인의 핸드폰에서 이미지에 대한 설명을 읽어줄 수 있도록 alt 속성은 넣어줘야 함
- `title` 속성은 마우스 포인터를 올리면 말풍선으로 보여줌

#### 4-2. `<figure>` `<figcaption>`
```html
<figure>
		<img src="intro.jpg" alt="책표지이미지">
		<figcaption> OO책의 표지 사진 </figcaption>
</figure>
```
- `<figure>` : 그림, 사진, 다이어그램과 텍스트 등의 콘텐츠를 함께 묶어 하나의 독립된 단위로 취급하고 싶을 때 사용
- `<figcaption>` : `<figure>` 요소를 위한 제목을 표현하는 요소로 `<figure>` 내에 위치하면 됨
<br>

### 5. 오디오 관련 태그
- HTML5는 외부객체로 표현하지 않고 별도의 플러그인 설치 없이 오디오와 비디오 재생 가능

#### 5-1. `controls`
- 화면에 컨트롤바 출력 (없으면 출력X)

#### 5-2. `autoplay`
- 파일을 로드하자마자 자동으로 재생한다는 의미
- `autoplay` 속성을 사용하려면 무조건 `muted`를 사용해야 함
    - youtube는 `iframe` 태그를 써서 `muted` 안 해도 자동 재생 가능
#### 5-3. `loop`
- 사운드를 반복 재생시킬 횟수 지정

#### 5-4. `width / height`
- 나중에 style 속성 써도 안 먹히기 때문에 사용하지 않음

#### 5-5. 오디오 타입을 지원하지 않을 경우 대비
```html
<audio controls autoplay muted>
		<source src="./sound/ditto.mp3" type="audio/mp3">
		<source src="./sound/ditto.ogg" type="audio/ogg">
		<source src="./sound/ditto.wav" type="audio/wav">
</audio>
```
- 브라우저에서 호환되는 MIME 타입이 다르기 때문에 위의 코드와 같이 사용
    - 브라우저에서 지원하는 첫 번째 타입만 실행되고, 나머지는 실행되지 않음 ⇒ 크로스 브라우징 처리
- `type` : 오디오 파일의 MIME 형식 지정
    - MIME 형식 : 멀티미디어 파일에 대한 형식을 종류별로 구분하도록 한 표기
    - ex) `audio/mp3` , `audio/ogg`

#### 5-6. `preload`

- `auto` : 웹 브라우저가 페이지를 로드하고 바로 오디오 파일 다운로드
- `metadata` : 사용자가 재생시키기 전까지는 메타데이터만 다운로드
- `none` : 사용자가 재생을 시작하기 전까지는 파일을 다운로드 하지 않음
<br>

### 6. 비디오 관련 태그
```html
<video poster="./img/img2.jpg" controls loop muted>
		<source src="./movie/ditto.mp4" type="video/mp4">
		<source src="./movie/ditto.ogv" type="video/ogg">
		<source src="./movie/ditto.webm" type="video.webm">
</video>
```
- src, controls, loop, autoplay 속성은 <audio> 요소의 속성들과 동일

#### 6-1. `width / height`
- 비디오 콘텐츠가 표시될 영역의 크기를 설정
- 비디오 자체의 크기와 일치하지 않을 경우 비디오 콘텐츠가 늘어나거나 잘릴 수 있음

#### 6-2. `videoWidth / videoHeight`
- 비디오 자체의 너비, 높이를 반환하는 속성

#### 6-3. `poster`
- 비디오가 로딩되고 있을 때 보여줄 이미지를 지정하는 속성

#### 6-4. `preload`
- audio 태그와 동일
- 브라우저가 미리 동영상을 로딩할지 지정하는 속성
- 속성이 metadata인 경우, 비디오의 첫 프레임이 나타남
<br>

### 7. 테이블 관련 태그
```html
<table class="tbl">
    <capion>
        <h2> 표에 대한 설명 </h2>
    </caption>
    <thead>
        <tr><th> 제목1 </th><th> 제목2 </th>
    </thead>
    <tbody>
        <tr><td> 내용1 </td><td> 내용2 </td></tr>
        <tr><td> 내용3 </td><td> 내용4 </td></tr>
        <tr><td> 내용5 </td><td> 내용6 </td></tr>
    </tbody>
    <tfoot>
        <tr><td colspan="2"> tfoot 부분입니다 </td></tr>
    </tfoot>
</table>
```
- 테이블에 선을 그리고 싶을 때 `<table border=”1”>` 사용하면 안됨 ⇒ 웹 표준 위배
<table>
    <tbody>
        <tr>
            <td> 선택 속성 </td>
            <td> 필수 속성 </td>
        </tr>
        <tr>
            <td> thead, caption, tfoot </td>
            <td> tbody </td>
        </tr>
    </tbody>
</table>

### 8. 폼 관련 태그
```html
<form action="">
</form>
```
- 전송방식 지정 안 하면 기본이 GET ⇒ 보안을 위해 POST 사용
#### 8-1 `<form>`
- 기본 사용자로부터 정보(아이디, 비밀번호 등)를 입력받을 때 사용하는 태그
- `action` : 폼에 입력된 정보를 받는 곳
- `method` : 폼에 입력된 정보를 전송하는 방식으로 get과 post가 있음

#### 8-2. 컨트롤 그룹 `<fieldset>` `<legend>`
```html
<fieldset>
		<legend></legend>
		<table></table>
</fieldset>
```
- 서로 관련성 있는 폼 컨트롤 요소를 묶어줄 수 있음
- 열고 닫는 태그 사이에 원하는 폼 컨트롤을 입력하면 됨
- legend는 컨트롤 그룹의 이름을 표시할 수 있음

#### 8-3. 문자(텍스트) 입력
```html
<input type="text">
```
- 사용자로부터 문자(=text)를 입력받는 태그
- `type` 속성을 생략하면 `text`가 됨
- `pattern` : <input> 요소의 값을 검사할 때 사용될 정규표현식을 명시
- `size` : `<input>` 요소의 너비를 문자수 단위로 명시

#### 8-4. 비밀번호 입력
```html
<input type="password">
```
- 사용자로부터 비밀번호를 입력받는 태그
- 사용자가 입력하는 정보가 외부로 노출되지 않음
- `pattern` : <input> 요소의 값을 검사할 때 사용될 정규표현식을 명시
- `size` : `<input>` 요소의 너비를 문자수 단위로 명시

#### 8-5. 숫자 입력
```html
<input type="number">
```
- 사용자로부터 비밀번호를 입력받는 태그
- `min`, `max`, `step` 속성을 지정할 수도 있음

#### 8-6. 날짜 입력
```html
<input type="date">
```
- 사용자로부터 날짜를 입력받거나 달력을 표시할 수 있는 태그

#### 8-7. 월 입력
```html
<input type="month">
```
- 사용자로부터 날짜를 입력받거나 달력을 표시할 수 있는 태그

#### 8-8. 주 입력
```html
<input type="week">
```
- 사용자로부터 날짜 중에서 몇 번째 주인지를 입력할 수 있는 태그

#### 8-9. 시간 입력
```html
<input type="time">
```
- 사용자로부터 시간을 입력할 수 있는 태그

#### 8-10. 이메일 입력
```html
<input type="email">
```
- 사용자로부터 이메일을 입력 받을 수 있는 태그
- `multiple` : `true | false`로, 여러 값을 허용할지 여부
- `size` : `<input>` 요소의 너비를 문자수 단위로 명시

#### 8-11. 전화번호 입력
```html
<input type="tel">
```
- 사용자로부터 전화번호를 입력 받을 수 있는 태그
- `pattern` : <input> 요소의 값을 검사할 때 사용될 정규표현식을 명시
- `size` : `<input>` 요소의 너비를 문자수 단위로 명시

#### 8-12. 검색어 입력
```html
<input type="search">
```
- 사용자로부터 검색어를 입력 받을 수 있는 태그

#### 8-13. 인터넷 주소 입력
```html
<input type="url">
```
- 사용자로부터 인터넷 주소인 URL을 입력 받는 태그

#### 8-14. 범위값 입력
```html
<input type="range">
```
- 사용자로부터 슬라이더를 활용하여 범위에 해당하는 값을 입력받을 수 있는 태그
- `min`, `max`, `step` 속성을 지정할 수도 있음

#### 8-15. 체크박스
```html
<input type="checkbox">
```
- 사용자가 ON/OFF의 형태의 선택사항으로 값을 받고자 할 경우 사용
- 사각형 모양으로 출력
- `checked` 속성을 지정할 수 있음

#### 8-16. 라디오 버튼
```html
<input tpye="radio">
```
- 사용자가 여러 가지 중에서 하나만 꼭 선택해야 하는 값을 받고자 할 경우 사용
- 둥근 모양으로 출력
- 여러 개의 라디오 버튼에서 하나만을 꼭 선택해야 하므로 반드시 name 속성이 같아야 함
- `checked` 속성을 지정할 수 있음

#### 8-17. 컬러 선택 버튼
```html
<input type="color">
```
- 사용자가 컬러 팔레트를 활용하여 원하는 색상의 값을 입력할 수 있는 태그

#### 8-18. 전송 버튼
```html
<input type="summit">
```
- 사용자가 폼에 입력한 정보를 action 속성에 입력한 곳으로 값을 전송할 수 있는 태그
- `formaction` : 양식 전송 시 `URL` 사용하기
- `formenctype` : 양식의 데이터 인코딩 유형이 양식 전송시 사용됨
- `formmethod` : 양식 전송 시 HTTP 방식을 사용
- `formnovalidate` : 양식 전송 시 양식 컨트롤 확인 무시
- `formtarget` : 양식 전송 시 서버로 제출된 후 받은 응답 데이터를 어디에 표시할 지 명시

#### 8-19. 취소 버튼
```html
<input type="reset">
```
- 사용자가 입력한 내용을 소거하여 초기화하는 태그

#### 8-20. 일반 버튼
```html
<input type="button">
```
- 사용자가 이 버튼을 눌렀을 경우 이벤트를 발생시키기 위한 태그

#### 8-21. 이미지 버튼
```html
<input type="image">
```
- 버튼에 이미지를 추가할 수 있는 태그
- `alt` : 이미지 유형에 대한 대체 속성으로, accessibility 측면에서 필요
- `src` : 이미지 출처의 주소에서 `src`와 같은 속성값
- `formaction` : 양식 전송 시 `URL` 사용하기
- `formenctype` : 양식의 데이터 인코딩 유형이 양식 전송시 사용됨
- `formmethod` : 양식 전송 시 HTTP 방식을 사용
- `formnovalidate` : 양식 전송 시 양식 컨트롤 확인 무시
- `formtarget` : 양식 전송 시 서버로 제출된 후 받은 응답 데이터를 어디에 표시할 지 명시
- `height` : 이미지의 height 속성과 같음
- `width` : 이미지의 width 속성과 같음

#### 8-22. 파일 첨부 버튼
```html
<input type="file">
```
- 파일을 첨부할 수 있도록 하는 태그
- `accept` 속성을 활용하여 특정 파일만 추가할 수 있도록 할 수 있음
- `multiple` : `true | false`로, 여러 값을 허용할지 여부

#### 8-23. 펼침 선택 상자
```html
<select name="control_name">
		<option value="val1"> val1 </option>
		<option> .... </option>
</select>
```
- 아래로 펼쳐져 늘어지는 목록 상자가 표시되어 그 중에서 사용자가 값을 선택할 수 있도록 해주는 태그
- 부속요소로 `option` 요소를 활용해야 함
- 처음부터 특정 값을 선택되게 하려면 해당 `option` 요소에 `selected` 속성을 추가함

#### 8-24. 메모 상자
```html
<textarea name="contro_name" rows="행수" cols="한 줄당 글자수">
</textarea>
```
- 여러 줄로 많은 내용의 텍스트를 입력받을 수 있는 태그

#### 8-25. 여러 가지 속성
- `autocomplete` : 모든 컨트롤에 지정 가능하며, 양식 자동 생성 기능 암시
- `autofocus` : 모든 컨트롤에 지정 가능하며, 페이지가 로딩될 때 양식 제어에 오토포커스되므로 하나의 컨트롤에만 지정해야 함
- `disabled` : 모든 컨트롤에 지정 가능하며, 양식 컨트롤이 비활성화되었는지의 여부를 지정하고, 지정된 컨트롤은 값을 전송할 수 없음
- `maxlength` : `password`, `search`, `tel`, `text`, `url` 컨트롤에 지정 가능하며, `value`의 최대 길이 (문자수)
- `minlengh` : `password`, `search`, `tel`, `text`, `url` 컨트롤에 지정 가능하며, `value`의 최소 길이 (문자수)
- `name` : input 양식 컨트롤의 이름으로, 이름/값 짝`(name/value pair)`의 일부로서 양식과 함께 전송됨
- `readonly` : 문자나 숫자로 입력하는 것은 모두 가능하며, 이 값은 수정이 불가능
- `required` : 입력 또는 선택하는 컨트롤은 모두 가능하며, 양식이 전송되기 위해서 반드시 입력하거나 확인이 필요한 값
- `value` : 이름/값 짝(name/value pair)의 일부로서 양식과 함께 전송됨

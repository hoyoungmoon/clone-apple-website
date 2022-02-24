# Apple website clone

HTML, CSS, JS로 애플 웹사이트 만들기

## 목표

- HTML, CSS
- 인터랙션, 애니메이션
- 스크롤 키프레임과 요소 컨트롤
- 고해상도 이미지 처리 위한 캔버스 활용

## HTML

- div, span : non-semantic element
- header, nav, section : semantic element

semantic element는 검색엔진이 웹사이트 정보를 수집 & 인덱싱할 때 수집하는 의미를 가진 HTML 태그이다.
브라우저, 검색엔진, 개발자 모두에게 해당 콘텐츠의 명확한 의미를 전달해줄 수 있는 역할을 한다.

- ul (unordered list)
- ol (ordered list)

- href 어트리뷰트를 "#{element_class}"로 정의하여 클릭시 해당 요소로 이동할 수 있다.

## CSS

### 셀렉터

- \*: HTML 문서 내의 모든 요소를 선택하는 전체 셀렉터
- 태그명, id(#), class(.)으로 셀렉팅
- a[href] : a 요소 중에 href 어트리뷰트 가지는 요소만 셀렉팅
- 후손(ex: ul li), 자식(>), 인접형제(+), 일반형제(~),
- **가상 클래스 셀렉터**: 요소의 특정 상태에 따라 스타일 정의할 때 사용하며 이미 정의된 CSS 표준 클래스 이름이 존재한다.

  - link, active, hover, visited, focus, checked, enabled, disabled, first-child, last-child, nth-child, nth-last-child, first-of-type, last-of-type, nth-of-type)

- **가상 요소 셀렉터**: 요소의 특정 부분에 스타일 정의할 때 사용
  - before, after, first-letter, first-line, selection

### 프로퍼티 단위

- px: 화소 단위 (브라우저 대부분 1px = 1/96inch로 인식)
- %: 요소의 디폴트 사이즈, 상속 사이즈에 상대적으로 사이즈 결정
- em: 요소의 디폴트, 상속 사이즈의 배수
- rem: em은 상속의 영향을 받아 요소의 깊이에 따라 예상치 못한 결과 발생할 수 있다. rem은 최상위 요소(html)의 값을 기준으로 결정한다.
- viewport: 반응형 웹디자인을 위해 크기가 동적으로 변할 때를 대응하기 위해 웹페이지의 가시영역(viewport)를 기준으로 상대적인 사이즈를 결정한다.
  - vh, vw, vmin, vmax
  - % 또한 em과 마찬가지로 상속에 의해 예상치 못한 결과 발생할 수 있음

### display

- block
  - 항상 새로운 라인에 시작한다.
  - width 100%이며 내부에 inline 레벨 요소 포함할 수 있다.
  - div, p, ol, ul, li, hr, table, form
- inline
  - 줄을 바꾸지 않고 한 행에 위치한다.
  - content 너비 만큼 width를 차지한다.
  - width, height, margin-top, margin-bottom 프로퍼티를 지정할 수 없다.
  - span, a, strong, img, br, button, input, select, textarea
- inline-block
  - inline 레벨 요소와 같이 한 줄에 표현되면서 width, height, margin 프로퍼티를 모두 지정할 수 있다.

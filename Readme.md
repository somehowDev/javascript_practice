# 개인 취미 웹 페이지 프로젝트 - JS편

<div style="text-align:center;">
<img src="./2.png" width="85%" height="50%" title="dev"/></div> <br />

이 프로젝트는 HTML, CSS 기초에 이어 Javascript를 기초적인 내용을 다루며, 이전에 배웠던 웹 페이지의 스타일과 레이아웃을 개선에 이어서 간단한 기능(javascript)를 활용하여 개인의 취미와 관심사를 돋보이게 표현하는 웹 사이트를 만드는 기술을 습득합니다.
<br />

## 프로젝트 목표

**JavaScript 기초 학습:** JavaScript의 기본 문법과 DOM 조작 방법을 배웁니다.
**상호작용성 추가:** 사용자가 웹 페이지와 상호작용할 수 있도록 버튼 클릭, 텍스트 입력, 이미지 슬라이드 등의 기능을 구현합니다.
**동적 UI 구현:** 페이지의 다양한 요소들(예: 섹션의 표시 및 숨김)을 동적으로 제어할 수 있는 기능을 추가합니다.
<br />

## 핵심 기능 구현 및 설명

**섹션 토글:** 각 섹션의 제목 옆에 있는 토글 버튼을 클릭하면 해당 섹션의 내용이 표시되거나 숨겨집니다. 이 기능은 사용자가 원하는 정보를 쉽게 찾을 수 있도록 도와줍니다.

```javascript
// 각 섹션에 대한 토글 기능을 설정합니다.
setupToggle("toggleTravel", "travelJournal");
setupToggle("toggleMusic", "musicPlaylist");
setupToggle("toggleGame", "gameReview");
setupToggle("toggleFashion", "fashionContent");
setupToggle("toggleBooks", "booksContent");
setupToggle("toggleMovie", "movieContent");
```

**이벤트 리스너 활용:** JavaScript의 이벤트 리스너를 활용하여 사용자의 클릭에 반응하는 로직을 구현합니다.

```javascript
// getElementById를 사용하여 DOM에서 토글 버튼 요소를 가져옵니다.
document
  .getElementById(toggleButtonId)
  .addEventListener("click", function () {
    ...
  });
```

**DOM 조작:** 문서의 요소를 선택하고, 스타일을 변경하며, 내용을 동적으로 수정합니다.

```javascript
// content 변수를 사용하여 섹션의 내용을 DOM에서 가져옵니다.
const content = document.getElementById(contentId);
// 버튼 자체에 대한 참조를 this 키워드를 사용하여 가져옵니다.
const button = this;

// 내용이 현재 숨겨져 있는지 (display가 'none')를 확인합니다.
if (content.style.display === "none") {
  // 내용을 보이도록 설정합니다 (display를 'block'으로 변경).
  content.style.display = "block";
  // 토글 버튼의 텍스트를 '➖'로 변경하여 내용이 펼쳐졌음을 나타냅니다.
  button.innerHTML = "➖";
} else {
  // 내용을 숨깁니다 (display를 'none'으로 변경).
  content.style.display = "none";
  // 토글 버튼의 텍스트를 '➕'로 변경하여 내용이 접혔음을 나타냅니다.
  button.innerHTML = "➕";
}
```

<br />

## 배운점

#### 함수의 정의와 사용

setupToggle 함수는 특정 엘리먼트의 표시 상태를 토글하는 기능을 가진 함수입니다. 이 함수는 JavaScript에서 함수를 정의하고 사용하는 방법을 잘 보여줍니다.

#### DOM 요소 접근

document.getElementById 메소드를 사용하여 HTML 문서에서 특정 ID를 가진 요소에 접근합니다. 이를 통해 웹 페이지의 구조적 요소를 프로그래밍적으로 조작할 수 있습니다.

#### 이벤트 리스너 추가

addEventListener 메소드를 사용하여 특정 요소에 클릭 이벤트 리스너를 추가합니다. 이를 통해 사용자의 클릭 동작에 반응하여 함수를 실행할 수 있습니다.

#### 조건문을 통한 동적 상호작용 처리

클릭 이벤트가 발생했을 때, 조건문 (if-else)을 사용하여 요소의 현재 상태(표시되거나 숨겨짐)를 체크하고, 이에 따라 요소의 display 속성을 조정합니다. 이는 조건에 따라 다른 동작을 수행하게 하는 기본적인 프로그래밍 구조입니다.

#### DOM 속성 수정

요소의 스타일 속성인 display를 수정하여 요소를 보이거나 숨기는 동작을 합니다. 이를 통해 JavaScript가 HTML 요소의 스타일을 직접 조작할 수 있음을 보여줍니다.

#### 텍스트 컨텐츠의 동적 변경

innerHTML 속성을 사용하여 요소의 내부 HTML(여기서는 ➕ 또는 ➖ 기호)을 동적으로 변경합니다. 이는 웹 페이지의 내용을 프로그래밍적으로 갱신하는 방법을 보여줍니다.
<br />

## 결론

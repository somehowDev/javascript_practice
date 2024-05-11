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

이 프로젝트를 통해 참가자들은 JavaScript의 기초를 배우고, 웹 페이지에 동적 기능을 추가하는 실용적인 경험을 했습니다. 이 경험은 기술적 자신감을 높이고, 복잡한 문제를 해결하는 능력을 향상시켰습니다. 참가자들은 자신의 취미를 웹사이트로 표현하며 창의력을 발휘하고, 웹 개발에 대한 열정을 더욱 고취시켰습니다. 이 프로젝트는 웹 개발에 필요한 기술적 기초를 다지는 데 중요한 역할을 했으며, 참가자들에게 지속적인 학습과 성장을 위한 발판을 마련했습니다. <br />

여러분이 배운 지식과 기술을 바탕으로 앞으로도 더 자신있고 재미있게 성장하길 바랍니다. 여기서 제가 다시 한번 강조하고 싶은 부분은 html, css, javascript의 기술을 말하는 것이 아닙니다. 우리는 꼭 혁신적인 기술이 필요한게 아닙니다. 이런 기초를 배우더라도 빠르게 도전해보고 실행 했다는게 더 중요한 포인트 입니다.
앞으로 계속 해서 도전해보며 즐기다 보면 그런 과정들이 결국 우리한테 좋은 결과로 돌아 올 것을 꼭 명심하길 바랍니다.

감사합니다, 그리고 다음 시간에 뵙겠습니다. 😃😃

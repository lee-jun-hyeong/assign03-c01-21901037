# Assignment 03 - Multi-Page CRUD Frontend UI

**학번:** 21901037  
**이름:** 이준형 (Junhyung Lee)

캠퍼스 중고교재 게시판을 HTML / CSS / JavaScript / Bootstrap으로 만든 과제입니다.  
서버(DB)는 연결하지 않고, 화면과 입력 검사, 반응형 레이아웃을 중심으로 작성했습니다.

## 페이지 설명

| 페이지 | 파일 | 설명 |
|--------|------|------|
| 목록 | [index.html](./index.html) | 중고교재 표(Table) + 등록 버튼 |
| 등록 | [add.html](./add.html) | 새 교재 입력 폼 + Validation |
| 상세 | [view.html](./view.html) | 1번 교재의 모든 Field 표시 |
| 수정 | [edit.html](./edit.html) | 기존 값이 채워진 수정 폼 |
| Bootstrap 예제 | [example.html](./example.html) | 공식 Album 예제와 같은 구조로 따라 만든 페이지 |
| 공통 CSS | [my.css](./my.css) | 모든 페이지에서 같이 쓰는 디자인 |

페이지 이동:

```
index.html  --[등록]-->  add.html
index.html  --[교재명]--> view.html
view.html   --[수정]-->  edit.html
view.html   --[삭제]-->  confirm() 확인창
모든 페이지 --[Home/목록]--> index.html
```

## URL

### GitHub Repository

https://github.com/lee-jun-hyeong/assign03-c01-21901037

### Vercel Deploy URL

> GitHub와 Vercel을 연결한 뒤, 실제 배포 주소로 바꿔 적습니다.

- https://assign03-c01-21901037.vercel.app/
- https://assign03-c01-21901037.vercel.app/index.html
- https://assign03-c01-21901037.vercel.app/add.html
- https://assign03-c01-21901037.vercel.app/view.html
- https://assign03-c01-21901037.vercel.app/edit.html
- https://assign03-c01-21901037.vercel.app/example.html

---

## Weekly Review – Week 3

### Service Topic

**캠퍼스 중고교재 관리**  
한동대 학생들이 전공 교재를 사고 팔 수 있는 게시판 화면입니다.

### Data Fields

6개보다 많은 8개 Field를 사용했습니다.

| Field | 설명 | 입력 방식 |
|-------|------|-----------|
| 교재명 | 책 이름 | 텍스트 |
| 저자 | 책을 쓴 사람 | 텍스트 |
| 과목명 | 이 책을 쓰는 수업 이름 | 텍스트 |
| 가격 | 판매 가격(원) | 숫자 |
| 책 상태 | 최상 / 상 / 중 / 하 | 선택(select) |
| 판매 상태 | 판매중 / 예약중 / 판매완료 | 선택(select) |
| 판매자 이메일 | 연락할 이메일 | 텍스트 |
| 등록일 | 글을 올린 날짜 | 날짜 |

### List Page

`index.html` 표에는 아래 5개 Field를 보여줍니다.

1. 번호
2. 교재명 (클릭하면 `view.html`로 이동)
3. 과목명
4. 가격
5. 판매상태

### Validation

`js/check.js` 파일에 검사를 모아 두었고, `add.html` / `edit.html`에서 같이 불러 씁니다. (4개 이상)

1. **필수값** — 교재명, 저자, 과목명이 비어 있으면 안 됨
2. **문자열 길이** — 교재명은 2자 이상 50자 이하
3. **숫자 범위** — 가격은 1,000원 ~ 200,000원
4. **이메일 형식** — `@`와 `.`이 들어 있어야 함
5. **날짜 입력 여부** — 등록일을 꼭 선택
6. **Select 선택 여부** — 책 상태, 판매 상태를 꼭 선택

추가 버튼은 `confirm("게시물이 추가됩니다.")`  
수정 버튼은 `confirm("게시물을 수정할까요?")`  
삭제 버튼은 `confirm("이 게시물을 삭제할까요?")` 를 사용합니다.

### RWD

Desktop / Mobile 두 환경을 같이 맞췄습니다.

- HTML에 `viewport` 메타 태그를 넣었습니다.
- Bootstrap Grid (`row`, `col-md-6`)로 폼을 넓은 화면에서는 2열, 휴대폰에서는 1열로 배치했습니다.
- 표는 `table-responsive`로 감싸서 휴대폰에서 좌우 스크롤이 됩니다.
- 메뉴는 `navbar-expand-md` + `navbar-toggler`로 휴대폰에서 접힙니다.
- `my.css`의 `@media (max-width: 767px)`에서 제목 크기, 버튼 폭, 상세보기 한 줄 배치를 따로 조정했습니다.

확인 포인트:

- 글이나 표가 화면 밖으로 넘치지 않는가
- 폼 폭이 너무 넓거나 좁지 않은가
- 버튼을 손가락으로 누를 수 있는가
- 메뉴가 열리고 닫히는가

### Bootstrap

사용한 주요 클래스 / 컴포넌트:

- `container`, `row`, `col`, `col-md-6`
- `navbar`, `navbar-toggler`, `collapse`
- `table`, `table-responsive`, `table-hover`
- `form-control`, `form-select`, `form-label`
- `btn`, `card`, `badge`, `album` 카드 그리드 (`example.html`)

`example.html`은 [Bootstrap Album 예제](https://getbootstrap.com/docs/5.3/examples/album/)를 최대한 비슷하게 따라 만들었습니다. (카메라 아이콘, Thumbnail 카드 9개, View/Edit, Light/Dark 버튼) 과제 Step6에 맞춰 `my.css`도 연결했습니다.

### Problem & Solution

**문제 1:** 처음에는 CSS를 각 HTML 파일 안에 따로 써서, 메뉴 색깔을 바꾸려면 파일을 4번 고쳐야 했습니다.

**해결:** 공통 디자인을 `my.css`로 분리하고, 모든 페이지에서 `<link rel="stylesheet" href="my.css">`로 연결했습니다.

**문제 2:** 휴대폰에서 표가 화면보다 넓어 글자가 잘렸습니다.

**해결:** 표를 `<div class="table-responsive">`로 감싸고, `my.css`에 모바일용 글자 크기와 버튼 폭을 추가했습니다.

### Reflection

- Bootstrap은 미리 만들어진 클래스 이름만 붙이면 버튼, 표, 반응형 배치가 나와서 편했습니다.
- `col-md-6`처럼 화면 크기 이름이 들어간 클래스가 Media Query를 대신해 준다는 점이 흥미로웠습니다.
- Validation은 `if`문과 `alert()`만으로도 충분히 만들 수 있었습니다. 아직 서버가 없어서 데이터가 저장되지는 않습니다. 다음에는 입력한 내용이 목록에 실제로 남는 방법을 공부하고 싶습니다.

### AI Usage

- Cursor로 HTML 뼈대, Bootstrap Album 따라하기, Validation 초안을 만들고 코드를 쉽게 고쳤습니다.
- 어려운 문법은 쓰지 않고 `var`, `function`, `if`, `alert`, `confirm` 위주로 직접 읽고 이해했습니다.

---

## Weekly Question (Google Form 제출용)

수업 핵심을 확인하는 문제 2개입니다. Google Form에 옮겨 제출하면 됩니다.  
https://forms.gle/QoxoyWP8ZiJTyJu67

### 문제 1 (객관식)

반응형 웹에서 휴대폰 화면 크기에 맞게 보이도록 HTML `<head>`에 넣는 태그는 무엇인가?

1. `<meta charset="UTF-8">`
2. `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
3. `<link rel="stylesheet" href="my.css">`
4. `<title>목록</title>`

**정답:** 2번  
**해설:** viewport 메타 태그가 있어야 모바일 브라우저가 화면 너비에 맞춰 페이지를 확대/축소합니다. charset은 한글 깨짐 방지, link는 CSS 연결, title은 탭 제목입니다.

### 문제 2 (OX)

Bootstrap의 `col-md-6` 클래스는 화면이 중간(md) 크기 이상일 때 한 줄의 절반(12칸 중 6칸)을 사용한다는 뜻이다.

**정답:** O  
**해설:** Bootstrap Grid는 한 줄을 12칸으로 나눕니다. `col-md-6`은 md 이상에서 6칸, 그보다 좁은 화면에서는 기본적으로 한 줄 전체를 차지합니다.

---

## LMS 제출 체크

- GitHub Repository URL
- Vercel Deploy URL
- Google Form 문제 2개 제출

# Assignment 03 과제 명세

과제 목표  
이전 과제에서 학습한 CRUD 개념을 기반으로 실제 서비스와 유사한 Multi-Page CRUD Frontend UI를 제작합니다. Bootstrap 또는 CSS Media Query를 이용하여 Desktop과 Mobile 환경에 대응하는 Responsive Web Design을 적용합니다.

## Practice Flow

CRUD Planning → List / Add / View / Edit → Validation → RWD → Bootstrap → Deploy

## 제출 전 준비

이번 과제는 새로운 프로젝트로 진행합니다.

- 새로운 GitHub Repository 생성
- Vercel에서 새로운 Site 생성
- GitHub Repository와 Vercel Site 연결
- Deploy 후 생성된 URL 확인

## Study – Responsive Web Design

Responsive Web Design과 Bootstrap Framework의 기본 사용법을 학습합니다.

참고 링크

- https://www.w3schools.com/bootstrap5/index.php
- https://www.w3schools.com/css/tryit.asp?filename=tryresponsive_video3
- https://www.w3schools.com/bootstrap/bootstrap_templates.asp
- https://getbootstrap.com/docs/5.3/examples/

주요 학습 내용

- Responsive Web Design
- Viewport
- Media Query
- Bootstrap Grid
- Container
- Row / Column
- Responsive Table
- Responsive Form
- Desktop / Mobile Layout

## 수행내용

### STEP 0. Bootstrap Example 따라하기

bootstrap 시작하기: https://getbootstrap.com/docs/5.3/getting-started/introduction/

다음 Bootstrap Example 페이지에서 1개를 선택합니다.

https://getbootstrap.com/docs/5.3/examples/

예) Sticky footer 제외한 그외 예제

- Album
- Pricing
- Heroes
- Carousel
- Sign-in
- Dashboard

선택한 페이지와 최대한 유사하도록 HTML/CSS 및 Bootstrap을 이용하여 제작합니다.

- 파일명: `example.html`
- Bootstrap CDN 사용 가능
- 예제의 텍스트, 이미지 등은 자유롭게 변경 가능

### Step1. CRUD Frontend Service 기획

제작하고 싶은 CRUD Frontend Service의 주제를 하나 선정합니다.

데이터는 6개 이상의 Field로 구성합니다.

예)

- 도서관리 : 도서명/저자/출판사/출판년도/ISBN/카테고리
- 친구관리 : 이름/관계/전화번호/이메일/주소/생일
- 상품관리 : 품목/품명/가격/수량/구매일/재고/상태

### Step2. List Page (파일명: index.html)

- CRUD Service의 메인 목록 페이지를 제작합니다.
- 임의의 Sample Data를 작성하여 Table 또는 List 형태로 표시합니다.
- 전체 데이터 Field 중 4개 이상을 목록에 표시합니다.
- 예) 번호 / 제목 / 작성자 / 조회수 / 생성일자

필수 기능

- [Add] 버튼
- 각 데이터의 상세보기 링크
- [Add] 클릭 시 `add.html`로 이동
- 특정 데이터 클릭 시 `view.html`로 이동
- Vercel 의 기본 배포 URL에 접속하면 `index.html`이 바로 표시되어야 합니다.

### Step3. Add Page (파일명: add.html)

새로운 데이터를 입력하는 Form 페이지를 제작합니다.

필수 조건

- 6개 이상의 입력 Field
- 적절한 Form Element 사용
- 필수 입력 항목 지정
- JavaScript Validation 4개 이상 적용

Validation 예)

- 필수값 입력 여부
- 문자열 길이
- 숫자 범위
- 이메일 형식
- 날짜 입력 여부
- Select 선택 여부

[추가] 버튼 클릭 시 메시지를 표시합니다.

예) "게시물이 추가됩니다."

`alert()` 또는 `confirm()`을 이용할 수 있습니다.

### Step4. View Page (파일명: view.html)

`index.html`의 목록에서 특정 데이터를 선택했을 때 표시되는 상세 페이지입니다.  
임의로 정한 하나의 Record에 대해 데이터의 모든 Field를 표시합니다.

필수 기능

- 모든 데이터 Field 표시
- [Edit] 버튼클릭 → `edit.html`로 이동
- [Delete] 버튼클릭 → `confirm()`을 이용하여 메시지 표시

### Step5. Edit Page (파일명: edit.html)

임의의 Record 데이터를 수정할 수 있는 Form 페이지를 제작합니다.

필수 조건

- 기존 Record 값을 Form에 표시
- 전체 데이터 Field를 수정할 수 있도록 구성
- 필수 항목 Validation 적용
- Validation 4개 이상 적용
- [수정] 버튼 클릭 시 `confirm()`을 이용합니다.

예) "게시물을 수정할까요?"

### Step6. 공통 Style 적용 (CSS 파일명: my.css)

모든 페이지에 공통 CSS를 적용합니다. HTML 내부에 모든 CSS를 작성하지 않고, 별도의 `my.css` 파일을 만들어 사용합니다.

다음 요소에 공통 Style을 적용합니다.

- Page Layout
- Navigation
- Form
- Input
- Select
- Button
- Table / List
- Card
- Header / Footer

### Step7. Responsive Web Design 적용

제작한 모든 페이지에 Desktop / Phone 2개 이상의 Device 환경을 위한 RWD를 적용합니다.

다음 방법을 활용할 수 있습니다.

- CSS Media Query
- Bootstrap Grid
- Bootstrap Responsive Utility

Desktop과 Mobile에서 다음 내용을 확인합니다.

- 콘텐츠가 화면 밖으로 넘어가지 않는가?
- Form의 폭이 적절한가?
- Table 또는 List를 확인할 수 있는가?
- Button을 정상적으로 사용할 수 있는가?
- Navigation이 정상적으로 동작하는가?

### Step8. Bootstrap 활용

Bootstrap Framework를 자유롭게 활용할 수 있습니다. Bootstrap Example 또는 Template을 참고하여 적용할 수 있습니다.

활용 예)

- container
- row
- col
- table
- form-control
- btn
- navbar
- card
- alert

### Step9. Page Navigation

4개의 페이지 사이에 자연스럽게 이동할 수 있도록 하이퍼링크를 연결합니다. 각 페이지에서 List 또는 Home으로 돌아갈 수 있는 링크를 제공합니다.

기본 흐름

- `index.html` → [Add] → `add.html`
- `index.html` → 데이터 선택 → `view.html`
- `view.html` → [Edit] → `edit.html`
- `view.html` → [Delete] → Confirm

참고 : 최종 Repository

Repository에는 최소 다음 파일이 포함되어 있어야 합니다.

- `index.html`
- `add.html`
- `view.html`
- `edit.html`
- `my.css`
- `README.md`

필요한 경우 다음과 같은 폴더를 추가할 수 있습니다.

- `images/`
- `js/`

### Step10. 배포 확인

Vercel Deploy URL에 접속했을 때 `index.html` 목록 페이지가 바로 표시되어야 합니다.

다음 페이지가 모두 정상적으로 접근되어야 합니다. Desktop과 Mobile 화면에서 각각 정상적으로 표시되는지 확인합니다.

- `example.html`
- `index.html`
- `add.html`
- `view.html`
- `edit.html`

## README.md – Weekly Review

README.md에 다음 내용을 작성합니다.

- Service Topic : 제작한 CRUD Frontend Service 주제
- Data Fields : 6개 이상의 데이터 Field와 각 항목 설명
- List Page : index.html에서 표시한 Field 4개 이상
- Validation : add.html과 edit.html에 적용한 Validation 조건 4개 이상
- RWD : Desktop과 Mobile 환경을 어떻게 구성했는지 설명
- Bootstrap : 사용한 Bootstrap Component 또는 Class
- Problem & Solution : 개발 중 발생한 문제와 해결 방법
- Reflection : 새롭게 알게 된 점 또는 궁금한 점

## Weekly Question

이번 주 수업 및 실습 내용을 바탕으로 퀴즈 2문제를 출제하여 Google Form으로 제출합니다.  
문제 출제 방법은 직접 출제 / AI 활용 후 수정 / AI 생성하면 됩니다.

https://forms.gle/QoxoyWP8ZiJTyJu67

- 문제 유형: 객관식 / OX / 단답형 / 주관식
- 직접 출제 또는 AI 도구 활용 가능
- 각 문제에 정답과 간단한 해설 포함
- 이번 주의 핵심 내용을 이해했는지 확인할 수 있는 문제로 출제
- 제출된 문제는 수업의 Weekly Quiz에 활용될 수 있습니다.

## 제출내용

LMS에 다음 내용을 제출합니다.

- GitHub Repository URL
- Vercel Deploy URL
- Google form : 문제 제출

## 6. Self-Check

1. 새로운 GitHub Repository를 생성했는가?
2. 새로운 Vercel Site를 생성했는가?
3. GitHub Repository와 Vercel을 연결했는가?
4. CRUD Frontend Service의 주제를 선정했는가?
5. 데이터 Field를 6개 이상 구성했는가?
6. Bootstrap sample page `example.html`를 만들었는가?
7. `index.html` 목록 페이지를 작성했는가?
8. 목록 페이지에 4개 이상의 Field를 표시했는가?
9. `add.html`을 작성했는가?
10. `add.html`에 6개 이상의 입력 항목을 사용했는가?
11. `add.html`에 Validation을 4개 이상 적용했는가?
12. 추가 시 메시지가 표시되는가?
13. `view.html`을 작성했는가?
14. 상세 페이지에 전체 데이터 Field를 표시하는가?
15. Edit 버튼이 `edit.html`로 연결되는가?
16. Delete 버튼에서 Confirm 창이 표시되는가?
17. `edit.html`을 작성했는가?
18. 기존 데이터를 Form 형태로 표시했는가?
19. `edit.html`에 Validation을 4개 이상 적용했는가?
20. 수정 시 Confirm 창이 표시되는가?
21. `my.css` 파일을 별도로 작성했는가?
22. 모든 페이지에 공통 Style을 적용했는가?
23. Desktop / Mobile 2개 이상의 환경에 RWD를 적용했는가?
24. Bootstrap 또는 Media Query를 활용했는가?
25. 4개 페이지 사이의 Navigation이 정상적으로 연결되는가?
26. Vercel에서 전체 페이지가 정상적으로 동작하는가? (명세 Self-Check에는 Netlify로 적혀 있으나, 본 과제는 Vercel 배포)
27. README.md에 Weekly Review를 작성했는가?
28. Weekly Question 2문제를 제출했는가?

---

## 점검 결과 (2026-09-17)

페이지/코드는 과제 필수 조건을 충족합니다. 아직 안 한 것은 배포와 Google Form 제출입니다.

| # | Self-Check | 결과 | 확인 |
|---|------------|------|------|
| 1 | 새 GitHub Repository | 부분 | remote는 `https://github.com/2026-2-OSS/assign03-c01-21901037.git` 있음. **아직 commit/push 안 함** |
| 2 | 새 Vercel Site | 미완료 | 프로젝트 생성/연결 전 |
| 3 | GitHub-Vercel 연결 | 미완료 | 위와 같음 |
| 4 | 주제 선정 | 완료 | 캠퍼스 중고교재 관리 |
| 5 | Field 6개 이상 | 완료 | 8개 (교재명/저자/과목명/가격/책상태/판매상태/이메일/등록일) |
| 6 | example.html | 완료 | Bootstrap Album 예제 따라함, CDN 사용 |
| 7 | index.html 목록 | 완료 | 샘플 5행 테이블 |
| 8 | 목록 Field 4개 이상 | 완료 | 번호, 교재명, 과목명, 가격, 판매상태 (5개) |
| 9 | add.html | 완료 | |
| 10 | 입력 항목 6개 이상 | 완료 | 8개 (text/number/select/date) |
| 11 | add Validation 4개 이상 | 완료 | `js/check.js`에 6개 |
| 12 | 추가 시 메시지 | 완료 | `confirm("게시물이 추가됩니다.")` |
| 13 | view.html | 완료 | |
| 14 | 전체 Field 표시 | 완료 | 번호 + 데이터 8개 |
| 15 | Edit → edit.html | 완료 | |
| 16 | Delete confirm | 완료 | `confirm("이 게시물을 삭제할까요?")` |
| 17 | edit.html | 완료 | |
| 18 | 기존 값 Form 표시 | 완료 | `value` / `selected` |
| 19 | edit Validation 4개 이상 | 완료 | add와 같은 `checkBookForm()` 6개 |
| 20 | 수정 시 confirm | 완료 | `confirm("게시물을 수정할까요?")` |
| 21 | my.css 별도 파일 | 완료 | |
| 22 | 모든 페이지 공통 Style | 완료 | index/add/view/edit/example 모두 `my.css` 연결 |
| 23 | Desktop/Mobile RWD | 완료 | viewport + Grid + `table-responsive` + `@media` |
| 24 | Bootstrap 또는 Media Query | 완료 | 둘 다 사용 |
| 25 | 4페이지 Navigation | 완료 | Add, 상세 링크, Edit, Home/목록 |
| 26 | Vercel 전체 페이지 | 미완료 | 로컬에서는 동작 확인. 배포 전 |
| 27 | README Weekly Review | 완료 | Topic/Fields/List/Validation/RWD/Bootstrap/Problem/Reflection |
| 28 | Weekly Question 2문제 | 부분 | README에 문제+정답+해설 작성됨. **Google Form 제출은 직접 해야 함** |

필수 파일: `index.html`, `add.html`, `view.html`, `edit.html`, `my.css`, `README.md`, `example.html`, `js/check.js` 있음.


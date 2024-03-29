# 👨‍👨‍👦‍👦 대학생의 바다
---

## 💬 프로젝트 주제

대학생들을 위한 커뮤니티.

정보의 바다라는 이름에서 착안하여 대학생의 바다라고 프로젝트명을 지었습니다.

어플 '에브리타임'을 모티브로 제작하였고 JSP 모델2 방식을 사용하여 개발하였습니다.

각종 대외활동, 구직정보 등을 얻을 수 있으며 대학생끼리 정보를 공유할 수 있는 커뮤니티입니다.
<br><br><br>

## 🕒 개발 기간

2022.05.02 ~ 2022.05.31
<br><br><br>

## 🔨 개발 환경
- 운영체제 : Windows10
- 사용 언어, 기술 : Java JDK1.8, HTML, CSS, JQuery, Ajax, JavaScript, JSP&Servlet
- 서버 : Tomcat 8.5, MySQL Workbench
- IDE : Eclipse
<br><br><br>

## 💬 ER 다이어그램
<img src="https://user-images.githubusercontent.com/103329327/178713950-ecbed6ad-c7f0-470c-a7ee-5da17b82d24e.png" width="80%" height="700px">

## 🎞 주요 기능

1. 메인페이지
- 인기글
- <b>ajax</b> 활용. 실시간 전국 날씨 출력(기온, 강수 등등)<br>


![메인](https://user-images.githubusercontent.com/103329327/179348279-4f9a2fb7-3bac-44c9-a0f2-359d7b2289ca.PNG)


- <b>구글 메일 API</b>를 이용하여 관리자에게 문의 기능 구현

![메일문의](https://user-images.githubusercontent.com/103329327/179348920-bd6c00b4-20f3-4d93-8a14-e03c0d602fa0.png)
![메일확인](https://user-images.githubusercontent.com/103329327/179348927-c46e3ce6-90f0-41a8-890e-9f8030779659.PNG)

<br><br>

----------


2. 회원

- 회원가입
- <b>key up 이벤트를 이용해</b> 아이디 및 비밀번호 중복, 유효성 체크. 모든 조건을 만족해야 회원 가입 가능.
- <b>다음 주소 API를 이용해</b> 회원 주소 입력.
<br>


<img src="https://user-images.githubusercontent.com/103329327/179349001-1046e34f-41a7-47e6-9f3f-37ea4c1f4674.PNG" height="500px">
<br><br>

- 회원정보 수정(최신 정보로 변경) 및 비밀 번호 수정 시 <b>비밀번호 체크</b> 후 동작 실행
- 마찬가지로 유효성 체크 후 수정 기능 동작
- 회원 탈퇴 시 비밀번호 체크 후 탈퇴 기능 동작
<br>

비밀번호 재확인

<img src="https://user-images.githubusercontent.com/103329327/179349267-f2a0eb60-34b2-4879-bfb5-1b2d95d59a71.PNG" height="500px">

회원 수정 페이지 - 회원 탈퇴하기 클릭 시 비밀번호 재확인

<img src="https://user-images.githubusercontent.com/103329327/179349369-52a0b101-3ec1-40dc-a73b-928d23608c3b.PNG" height="500px">

---

3. 게시판
3-1. 자유게시판(자유의바다)
- 첨부 파일 유무에 따라 <b>파일 이미지</b> 표시

<img src="https://user-images.githubusercontent.com/103329327/179349457-b4e31ba5-00fc-4efd-b2eb-cd3d34c8234f.PNG" height="500px">

- 검색 키워드를 받아 글제목 컬럼으로 글검색 수행
<img src="https://user-images.githubusercontent.com/103329327/179349887-9bddae46-e1c4-4ae0-91de-fe14a3634354.PNG" height="500px">

- 글쓰기 유효성 체크 후 글쓰기 동작 수행
- 글쓴이만 수정/삭제 버튼 보이게 함
- (첨부파일 존재시) 파일 클릭 시 다운 가능

<img src="https://user-images.githubusercontent.com/103329327/179349514-e08badfa-5395-451b-86c2-82cee506ceba.PNG" height="500px">


- 글 클릭 시, <b>session 영역에 저장된 id를 비교.</b> 좋아요 유무 체크. 비회원일시 좋아요, 댓글기능 제한
- 좋아요 클릭시 db에서 id값과 게시판 번호를 비교하여 데이터 존재 시 좋아요 취소. 없을시 좋아요 동작
<img src="https://user-images.githubusercontent.com/103329327/179349604-6c38dc41-5c28-4a5d-bae9-bed9b38c36c5.PNG" height="500px">


- 좋아요 후
<img src="https://user-images.githubusercontent.com/103329327/179349606-db407ca2-2da0-4ab0-85cc-5cb929763ec0.PNG" height="500px">

- 댓글 작성자일시 수정/삭제 버튼 보이게 함
- 수정 버튼 클릭 시 index 번호를 매개변수로 보내 해당 클래스의 댓글 박스 display 속성을 block으로 변경
<img src="https://user-images.githubusercontent.com/103329327/179349711-116b4a7e-4936-401c-85e5-847dda78da24.PNG" height="500px">

---

3-2. 중고거래게시판(중고바다)

- 책 검색란에 책제목 입력시 <b>다음 책검색 api</b>를 통해 출판사와 가격정보를 받아올 수 있음. 검색 결과는 최대 20개까지 표시함

<img src="https://user-images.githubusercontent.com/103329327/179349995-8424c1e4-edd5-4c53-a86b-38dd5eae4e6e.PNG" height="500px">

- 글 수정을 통해 판매중/판매완료를 지정할 수 있음
- 판매완료 시 이미지 다르게 표시
<img src="https://user-images.githubusercontent.com/103329327/179350001-6effaba0-6aba-43d0-bb1e-95715a3e2ab1.PNG" height="500px">
<img src="https://user-images.githubusercontent.com/103329327/179350827-00d2f308-1993-43f3-9da0-fa6a3e7deb64.PNG" height="500px">



- 책 거래는 <b>쪽지 기능</b>을 통해 이루어짐
<img src="https://user-images.githubusercontent.com/103329327/179350132-0acf4ff4-e408-47ae-9654-394da3c64ea8.PNG" height="500px">

- receiver, sender 컬럼을 통해 받은쪽지, 보낸쪽지 구별
<img src="https://user-images.githubusercontent.com/103329327/179350135-4c3c8080-034b-41dd-85a7-1e036e615c14.PNG" height="500px">

---

4. 관리자 페이지(사이트관리)
- admin 계정(관리자)으로 로그인 시 사이트 관리 탭이 보이며 회원 관리란에서 검색/수정/탈퇴 기능
- 회원 id 또는 이름 카테고리로 검색

<img src="https://user-images.githubusercontent.com/103329327/179350246-0522790b-e109-42c5-b268-e5ac18947ae7.PNG" height="500px">


- 게시판 관리에서 실시간 인기글 지정 기능 / 글 정렬 기능

<img src="https://user-images.githubusercontent.com/103329327/179350477-99189449-20eb-4ef0-9279-65b76f6ab219.PNG" height="500px">

- 인기글 적용 후 -> <b>메인에서 실시간으로 바뀜</b>

<img src="https://user-images.githubusercontent.com/103329327/179350710-c96fa61f-5888-457c-a5b4-f7b924abb729.PNG" height="500px">


---

## 💎 프로젝트 후 느낀점 & 보완점
1. 프로젝트 초기 단계에서 이름 작성 규칙, DB 설계 등을 좀 더 구체적으로 정해야겠다.
2. 중고거래 게시판은 포토게시판이라 이미지가 노출되게 되어있는데 글 수정시 이미지 파일을 따로 첨부하지 않고 올리면 엑박이 발생하는 문제가 있었다.
이미지가 아닌 텍스트는 수정하는 view로 정보를 끌어올 수 있지만 input 타입으로 파일을 첨부하다보니 이를 실행하는것이 불가능했다. 
다음에 이미지 게시판을 만든다면 이를 보완하고 싶다.
3. 쪽지 기능에서 그 전에 쪽지를 주고받은 기록이 있으면 그대로 쪽지함에 기록이 남아있기 때문에 사용자 입장에선 처음 쪽지를 보내는 것이지만 과거의 이력이 남아있어 익명성을 보장하기가 어려운 점이 있다. 또 새 쪽지에 대한 알람 기능을 추가하면 더 좋을 것 같다.
4. 패스워드를 암호화 하여 DB에 저장해야겠다. (보안성 보완)
5. 대댓글이나 댓글을 수정하는 경우에도 글자수 유효성 체크 가능하게 하기




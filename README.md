# django-instagram
django로 인스타그램 따라 만들기(like-lion 실습)

## 기존 코드를 가져오면서 발생했던 이슈 및 주요 변경사항
1. 로그인 url 접속 시 무한루프 문제 -> 로그인 함수에 걸린 어노테이션을 로그아웃 함수로 변경
2. 슈퍼유저 계정을 알 수 없어, 기존 코드 내부에 있던 커스텀 유저 패키지에 함수를 사용해 create superuser
3. 기존에 생성된 admin계정이 있어 staff를 true로 주었지만, 권한이 없어 superuser생성으로 해결.
4. image가 없으면 예외가 발생하는 문제를 if문으로 예외처리
5. settings.py에 리다이렉션을 위한 로그인, 로그아웃 url 추가.
6. logout 함수 작동을 위해 urls.py에 로그아웃 url 추가.

## 주요 기능 스크린샷

### 1. 로그인 및 회원가입 (+관리자)
<img width="1040" alt="스크린샷 2023-06-18 오전 12 38 59" src="https://github.com/castlehyeon/django-instagram/assets/53210680/11a30d5b-6b45-4cf6-a3c7-bb3ceec35766">
<img width="1046" alt="스크린샷 2023-06-17 오후 11 44 39" src="https://github.com/castlehyeon/django-instagram/assets/53210680/f81e5e18-dec7-46eb-94e5-f0a915f34243">
<img width="589" alt="스크린샷 2023-06-17 오후 2 00 44" src="https://github.com/castlehyeon/django-instagram/assets/53210680/79e15214-917a-46e9-a43e-4c822e4bba92">

### 2.관리자는 유저 그룹별 관리와 게시글 관리 기능, model 설계에 따라 게시글 옵션 정보 확인 기능
<img width="1420" alt="스크린샷 2023-06-18 오전 12 33 52" src="https://github.com/castlehyeon/django-instagram/assets/53210680/8bdd577f-60e7-43ec-b797-a398942f9f25">
<img width="1420" alt="스크린샷 2023-06-18 오전 12 34 12" src="https://github.com/castlehyeon/django-instagram/assets/53210680/63fc40a9-bfe1-45f7-b6a7-5f256076e766">
<img width="1420" alt="스크린샷 2023-06-18 오전 12 34 43" src="https://github.com/castlehyeon/django-instagram/assets/53210680/5c46d081-9b2a-473f-abfc-9b5028919668">
<img width="1420" alt="스크린샷 2023-06-18 오전 12 34 50" src="https://github.com/castlehyeon/django-instagram/assets/53210680/a3ea7088-51f0-4ac1-b94e-72ba50c5ff31">



### 3. 생성된 게시글과 답글은 메인페이지 확인 가능
<img width="1040" alt="스크린샷 2023-06-18 오전 12 41 45" src="https://github.com/castlehyeon/django-instagram/assets/53210680/41af6f49-2520-45b9-90e8-3e505ae9aa1e">

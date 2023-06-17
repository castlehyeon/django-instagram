# django-instagram
django로 인스타그램 따라 만들기(like-lion 실습)

## 기존 코드를 가져오면서 발생했던 이슈 및 주요 변경사항
1. 로그인 url 접속 시 무한루프 문제 -> 로그인 함수에 걸린 어노테이션을 로그아웃 함수로 변경
2. 슈퍼유저 계정을 알 수 없어, 기존 코드 내부에 있던 커스텀 유저 패키지에 함수를 사용해 create superuser
3. 기존에 생성된 admin계정이 있어 staff를 true로 주었지만, 권한이 없어 superuser생성으로 해결.
4. image가 없으면 예외가 발생하는 문제를 if문으로 예외처리
5. settings.py에 리다이렉션을 위한 로그인, 로그아웃 url 추가.
6. logout 함수 작동을 위해 urls.py에 로그아웃 url 추가.

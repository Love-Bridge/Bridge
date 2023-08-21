# Bridge
멋사 11th 중앙해커톤 Bridge 연동코드

## 배포 URL
[Bridge 홈페이지 방문하기](http://3.35.4.22:3000/)
<br/>
(요금 부과 문제로 현재는 닫힌 상태입니다.)


## 로컬 실행방법
1. git clone 받기
2. secrets.json 파일 생성
   
   **(목적)** 로그인을 위한 파일
   
   **(초기 세팅)** [Kakao Developers](https://developers.kakao.com/), [NAVER Developers](https://developers.naver.com/main/), [Google Cloud Console](https://console.cloud.google.com/) 에 접속하여 만들 앱에 대한 각각의 키를 발급받기

   **(파일 경로)** ***Bridge/bridge/secrets.json***

   **(파일 내용)**
   * "SECRET_KEY"는 장고 secret_key로 settings.py에서 확인 가능
   * 따옴표 부분을 발급받은 내용으로 채우기
   * redirect uri는 각 소셜의 Developers에서 설정한 redirect uri를 **동일**하게 설정해야 함 (사이트에 들어가서 아래와 같이 설정할 것)
   <br/>
  
   ```json
   {
     
      "SECRET_KEY": "django-insecure-",

      "KAKAO_REST_API_KEY": "",
      "KAKAO_REDIRECT_URI": "http://127.0.0.1:8000/accounts/login/kakao/user/callback/",
      "KAKAO_SECRET_KEY": "",
      
      "NAVER_CLIENT_ID": "",
      "NAVER_REDIRECT_URI": "http://127.0.0.1:8000/accounts/login/naver/user/callback/",
      "NAVER_CLIENT_SECRET": "",
  
      "GOOGLE_CLIENT_ID": "",
      "GOOGLE_REDIRECT_URI": "http://127.0.0.1:8000/accounts/login/google/user/callback/",
      "GOOGLE_CLIENT_SECRET": ""
    }
   ```
   
4. Bridge 폴더 안에서 터미널 실행 후 가상환경 만들고 켜기 (윈도우는 git bash 실행)
   
   ```bash
   # 가상환경 만들기
   python -m venv myvenv
   ```
   ```bash
   # 가상환경 실행
   ## 윈도우
   source myvenv/Scripts/activate
   ## 맥
   source myvenv/bin/activate
   ```
   
5. 장고 서버 실행

   ```bash
   python manage.py runserver
   ```
   
6. 리액트 실행
   Bridge/Bridge-Client 폴더 안에서 새로운 터미널 실행 (윈도우는 git bash 실행)
   ```bash
   # yarn 설치
   ## 윈도우
   sudo npm install -g yarn
   ## 맥
   brew install yarn
   ```
   
   ```bash
   # react-scripts 추가
   sudo yarn add react-scripts
   ```
   
   ```bash
   # 리액트 실행
   yarn start
   ```
   

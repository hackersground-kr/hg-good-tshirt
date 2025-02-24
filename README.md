# `이번 해커톤 옷 나쁘지않네` - `sodam`

해커그라운드 해커톤에 참여하는 `이번 해커톤 옷 나쁘지않네` 팀의 `sodam`입니다.

## 참고 문서

> 아래 두 링크는 해커톤에서 앱을 개발하면서 참고할 만한 문서들입니다. 이 문서들에서 언급한 서비스 이외에도 더 많은 서비스들이 PaaS, SaaS, 서버리스 형태로 제공되니 참고하세요.

- [순한맛](./REFERENCES_BASIC.md)
- [매운맛](./REFERENCES_ADVANCED.md)

## 제품/서비스 소개

<!-- 아래 링크는 지우지 마세요 -->
[제품/서비스 소개 보기](TOPIC.md)
<!-- 위 링크는 지우지 마세요 -->

## 오픈 소스 라이센스

<!-- 아래 링크는 지우지 마세요 -->
[오픈소스 라이센스 보기](./LICENSE)
<!-- 위 링크는 지우지 마세요 -->

## 설치 방법
# Azure 배포 - Azure Container Apps

Java와 SpringBoot를 통해 개발한 애플리케이션을 [Azure Developer CLI](https://learn.microsoft.com/ko-kr/azure/developer/azure-developer-cli/overview?WT.mc_id=dotnet-121695-juyoo)를 이용해 [Azure Container Apps](https://learn.microsoft.com/ko-kr/azure/container-apps/overview?WT.mc_id=dotnet-121695-juyoo)로 배포해 보겠습니다.

> [IntelliJ IDEA](https://www.jetbrains.com/ko-kr/idea/) 환경과 Mac m2에서 작업하는 것을 기준으로 합니다.

## 사전준비
1. [IntelliJ IDEA](https://www.jetbrains.com/ko-kr/idea/)설치하기(설치되지 않으셨다면 아래를 참고해주세요)
![image](https://github.com/user-attachments/assets/1ca7b9ec-01e5-498e-8a89-a4427238bdc8)
IntelliJ 사이트에 들어가주세요.
![image](https://github.com/user-attachments/assets/699838f8-616d-4803-a25f-cc5e3da88569)
저신의 운영체제에 맞는 파일을 설치해주세요
![image](https://github.com/user-attachments/assets/9c9c443e-5a26-4042-89d0-4e08c06739c9)
계속해서 다음을 눌러주세요
![image](https://github.com/user-attachments/assets/ba6395b1-cbf5-4167-9734-9c96ffcce9e0)
위 사진의 화면이 나오면 path를 추가해주신 이후 다음을 눌러주세요
![image](https://github.com/user-attachments/assets/ca3a3619-b87e-4076-b084-f8b20ba1f535)
설치를 눌러주세요
![image](https://github.com/user-attachments/assets/2c474700-8940-4a5e-827a-cb7c82ebf90e)
지금 재부팅을 선택해주시고 마침을 눌러주세요

2. 자바 [이것](https://www.java.com/ko/download/ie_manual.jsp?locale=ko) 설지하기(맥북은 다음 코드로 들어가주세요: https://www.java.com/ko/download/apple.jsp )
![image](https://github.com/user-attachments/assets/ce1d9330-d646-4141-9847-279a4d982a34)
자바 다운로드를 클릭해주세요
![image](https://github.com/user-attachments/assets/753cc2ec-99eb-4ac5-be70-a8ffa6f0ce4d)
설치를 클릭해주세요

3. Docker [이것](https://www.docker.com/) 설치하기
![image](https://github.com/user-attachments/assets/1741a4bd-77a6-4e9a-b1d2-13a2f92bd167)
자신의 운영체제에 맞는 도커를 설치해주세요
![image](https://github.com/user-attachments/assets/1d57f23b-1d15-4c9d-a3af-42cdcf3e830c)
둘 다 체크하고 ok를 눌러주세요
![image](https://github.com/user-attachments/assets/31224e11-8187-42da-80a7-e3bc35339f4d)
설치가 완료되면 close 해주세요

4. 회원가입 및 로그인이 필요하다면 로그인과 회원가입을 해 주세요.(독커실행도 무조건 하셔야 합니다!)




## 따라하기
   1. 빈 폴더를 배경화면에 생성해 주세요

      <img width="115" alt="스크린샷 2024-08-26 오후 3 50 58" src="https://github.com/user-attachments/assets/4dfe23b5-2628-460f-9f81-0fcfcf179ab0">

   2. 우클릭을하여 제일 및 서비스를 클릭하여 새로운 터미널을 열어주세요(iTerm이 없다면 새로운 터미널 열기를 해 주세요)

      <img width="491" alt="스크린샷 2024-08-26 오후 3 51 35" src="https://github.com/user-attachments/assets/0c4a8305-fa67-47a3-98de-470bf41e6b53">

   3. 터미널에 아래의 코드를 작성해 주세요

      ```git clone https://github.com/hackersground-kr/hg-good-tshirt.git ```
   4. 폴더 안에 생성이 된 것을 확인하세요
      
      <img width="195" alt="스크린샷 2024-08-26 오후 3 52 32" src="https://github.com/user-attachments/assets/d66efaa2-8790-4f43-a95c-1fa42aeffd9f">
   5. intelliJ를 키세요

      <img width="821" alt="스크린샷 2024-08-26 오후 3 59 37" src="https://github.com/user-attachments/assets/3123a64e-5ad1-4ef9-acf8-59d75a0b4830">
   6. Open을 클릭하고 방금 클론한 파일을 열어주세요

      <img width="806" alt="스크린샷 2024-08-26 오후 3 55 00" src="https://github.com/user-attachments/assets/afb6fea3-6a57-45c3-977e-b2aac8f9563c">

   7. 이 창이 뜬다면 파란색 버튼을 클릭하세요

       ![스크린샷 2024-08-26 오후 3 55 14](https://github.com/user-attachments/assets/425681c9-0006-444a-b07a-d51df9c1de4b)

   8. 좌측 하단에 있는 터미널창을 열어주세요
      
      <img width="182" alt="스크린샷 2024-08-26 오후 4 20 41" src="https://github.com/user-attachments/assets/140c56a1-2d2f-4bd4-bc08-2634fb9b62e0">
   10. 상단에 있는 열기를 클릭

       <img width="376" alt="스크린샷 2024-08-27 오전 5 18 21" src="https://github.com/user-attachments/assets/2a18d4ee-1cef-4030-8fe5-6da8a9c79325">
   10-1. 원하는 프로젝트를 쭉 타고 들어가 build.gradle을 클릭
   
   <img width="820" alt="스크린샷 2024-08-27 오전 5 19 10" src="https://github.com/user-attachments/assets/09dcc788-205b-4714-b20c-c6d515e94abc">
   10-2. 파란색 버튼 클릭 및 새로운창에서 열기 클릭
   
   <img width="475" alt="스크린샷 2024-08-27 오전 5 20 08" src="https://github.com/user-attachments/assets/502555f2-2e0a-421e-a41d-8f202fef015d">

11. 브랜치를 변경합니다 (아래코드를 실행해 주세요)

      ```git switch master```
   ```./gradlew build```
root.build.libs 안에 jar파일이 생성되었는지 확인한다.(SNAPSHOT.jar가 아님!!)
만약 없다면 코드를 재실행하거나 ```./gradlew clean build``를 입력하며 생성될때까지 한댜

오늘쪽의 코끼리 모양을 누르고 Task -> build 로 이동 후 clean과 build를 각각 실행시켜보는것도 시도해 본다.
<img width="267" alt="스크린샷 2024-08-27 오전 7 01 34" src="https://github.com/user-attachments/assets/356bc1f2-5d3f-4b85-b003-116bc60e5209">

   13. 윈도우인 경우
       ```winget install microsoft.azd```
       맥북인 경우
       ```curl -fsSL https://aka.ms/install-azd.sh | bash```
       password창엔 컴퓨터 비밀번호 눌러주세요
   14. ```azd auth login``` 명령어 실행하여 Azure로그인해 주세요
   
   15. 아래의 코드를 따라합니다

       ```azd init -e good-tshirt```
   16. 이런 문구가 뜬다면 엔터를 누르세요

       <img width="731" alt="스크린샷 2024-08-26 오후 4 24 38" src="https://github.com/user-attachments/assets/c16596c1-33ac-4ac5-8e3d-0327df5f1f4c">
   17. 그 다음 y를 작성후 엔터를 눌러 주세요

       <img width="646" alt="스크린샷 2024-08-26 오후 4 25 34" src="https://github.com/user-attachments/assets/78c82030-9e71-4c1e-9776-3989c470cb58">
   18. 방향키를 통해 JAVA로 이동하여 엔터를 눌러주세요

       <img width="623" alt="스크린샷 2024-08-26 오후 5 36 10" src="https://github.com/user-attachments/assets/9e40ade2-0849-434f-b459-497449d18019">
   19. 이런 문구가 뜨면 tab을 눌러주세요

       <img width="614" alt="스크린샷 2024-08-26 오후 5 36 42" src="https://github.com/user-attachments/assets/08b082f4-05c7-47c4-b5a1-4d150a620a0b">
   20. 이동하지 않고 엔터

       <img width="530" alt="스크린샷 2024-08-26 오후 6 38 27" src="https://github.com/user-attachments/assets/2cdb1308-937a-4106-b526-fe9fc84ab9ba">

   21. 이런게 뜨면 그냥 엔터쳐 주세요
      
       <img width="750" alt="스크린샷 2024-08-26 오후 4 35 10" src="https://github.com/user-attachments/assets/de32601b-bb4d-496a-90dd-78c88ba34e8c">
   22. 또 엔터쳐 주세요
      
       <img width="688" alt="스크린샷 2024-08-26 오후 4 36 06" src="https://github.com/user-attachments/assets/3e4b52a0-6146-49dc-9bc8-6a4306264eed">
   23. SUCCESS: Your app is ready for the cloud! 가 뜨면 성공!
      
       <img width="1027" alt="스크린샷 2024-08-26 오후 4 36 29" src="https://github.com/user-attachments/assets/1669019d-fd79-496d-9a57-e9ee1c277210">
        
24. ```azd up``` 명령어 실행
25. 엔터 누르기
   
    <img width="635" alt="스크린샷 2024-08-26 오후 5 42 23" src="https://github.com/user-attachments/assets/40fd826e-bd60-4e9f-99dc-e516484fcfa6">

26. 또 엔터 누르기

    <img width="587" alt="스크린샷 2024-08-26 오후 5 42 56" src="https://github.com/user-attachments/assets/b2ee1c3b-87b6-455d-b4a7-c3793adaffcd">
27. 터미널창에 아래 코드를 입력합니다.

    ```git init```
    ```git add .```
    ```git commit -m "Initial commit```

28. 개인 깃허브 프로필에 들어가 레포지토리 클릭 후 new를 클릭합니다.

    <img width="497" alt="스크린샷 2024-08-26 오후 6 02 34" src="https://github.com/user-attachments/assets/6cf1f244-becb-42b6-9a21-e70c02b0c156">
29. 이름을 sodam으로 지정 후 아래로 스크롤하여 레포지토리 생성버튼을 클릭합니다.

    <img width="753" alt="스크린샷 2024-08-26 오후 6 03 43" src="https://github.com/user-attachments/assets/93e2ab8c-bfdc-4aa5-a5d4-9cd661aad877">
    <img width="775" alt="스크린샷 2024-08-26 오후 6 03 55" src="https://github.com/user-attachments/assets/c4bdc3be-2d92-4bbc-a492-ae9c1253b2c9">

30. 그림에 https://github.com/GayeongKimm/sodam.git 로 해당하는 부분을 복사해 주세요(앞의 링크가 아닌 사진에 위치한 여러분의 링크를 복사하란 뜻 입니다.)

    <img width="1470" alt="스크린샷 2024-08-26 오후 6 42 33" src="https://github.com/user-attachments/assets/0b4d3e77-9ebf-404a-89ae-4cb52e12c3ca">
31. 아래코드를 차례대로 입력해 주세요
```git remote remove origin``` 
```git remote add origin {아까 복사한 주소}```
```git push origin main```

32. 푸시가 될때까지 잠깐기다리세요 
33. azure로 돌아와 azure SQL에 접속하여 만들기를 클릭합니다.

    <img width="1470" alt="스크린샷 2024-08-26 오후 6 48 52" src="https://github.com/user-attachments/assets/fd4a8f0a-035c-4eeb-acd2-31e8f5933e4d">
34. <img width="1470" alt="스크린샷 2024-08-26 오후 6 50 21" src="https://github.com/user-attachments/assets/40c1776e-a360-459e-8195-8aa05c59cbc4">

리소스 그룹에서 rd-good-tshirt를 선택후 이름과 위치를 사진과 같이 합니다.

<img width="1470" alt="스크린샷 2024-08-26 오후 6 50 53" src="https://github.com/user-attachments/assets/200fd449-1128-4bba-9515-9addb1104e90">

아래로 스크롤하여 사진과 같이 설정 후 비밀번호는 원하는걸로 설정한다(꼭 기억하기!)
<img width="825" alt="스크린샷 2024-08-26 오후 6 52 46" src="https://github.com/user-attachments/assets/a5d30a26-3982-4ca5-8463-6421fc658cb8">

만들기를 한다.
<img width="555" alt="스크린샷 2024-08-26 오후 6 53 49" src="https://github.com/user-attachments/assets/d97cab7e-e279-44c8-b65d-b025b228e470">

리소스로 이동을 하여 연결 문자열을 선택한다.
<img width="270" alt="스크린샷 2024-08-26 오후 7 01 47" src="https://github.com/user-attachments/assets/526e4d5c-96dd-46bf-a21f-ff7f43ae7d94">

JDBC로 이동하여 빨간 부분을 복사한다.
<img width="1152" alt="스크린샷 2024-08-26 오후 7 03 05" src="https://github.com/user-attachments/assets/dc3b6540-6838-4334-a683-47bda0de55b6">

아까전 생성한 github 레포지토리로 이동하여 settings로 이동한다.
<img width="1289" alt="스크린샷 2024-08-26 오후 7 05 10" src="https://github.com/user-attachments/assets/c4611711-5a2a-4aee-a01d-590cd195a5d8">

아래로 스크롤하여 Secrets and variables부분을 클릭하시고 actions를 클릭해주세요.
<img width="319" alt="스크린샷 2024-08-26 오후 7 06 33" src="https://github.com/user-attachments/assets/6fcfb45d-e8fe-4fee-b53a-e269d5983808">

초록버튼 클릭 
<img width="1470" alt="스크린샷 2024-08-26 오후 7 07 52" src="https://github.com/user-attachments/assets/6efb8923-c64d-45ff-9221-2898a1b41ff5">

아까 설정한 정보들을 아래와 같이 넣는다. 비밀번호는 설정한 비밀번호로 넣어줘야 한다.
<img width="807" alt="스크린샷 2024-08-26 오후 7 08 38" src="https://github.com/user-attachments/assets/cbcd6d57-7802-4f1e-b2df-2e16b83f094b">
<img width="788" alt="스크린샷 2024-08-26 오후 7 09 06" src="https://github.com/user-attachments/assets/e66e066a-a463-4fb5-82a4-909cb1e3ee30">
<img width="829" alt="스크린샷 2024-08-26 오후 7 09 35" src="https://github.com/user-attachments/assets/3cbd75e3-c325-422e-8f56-539194a29b07">

intelliJ로 돌아와 아래코드를 실행한다.
```azd pipeline config```

이제 마지막이다.
Actions 클릭후 제일 최근의 workflow를 클릭한다
<img width="1468" alt="스크린샷 2024-08-26 오후 7 11 25" src="https://github.com/user-attachments/assets/c9a60085-80bc-4a42-a2c5-437f6f96ad46">

re-run-allJobs를 클릭한다.
<img width="1470" alt="스크린샷 2024-08-26 오후 7 12 45" src="https://github.com/user-attachments/assets/608d47bf-bc0a-4247-aba1-4c2d8d8c3942">

기다리시다 초록불이 뜨면 액션성공이다.








1.	깃허브에 로그인한 이후 https://github.com/ahapwhs0414/SODAM_WEB_V1 을 Fork해주세요

2.	에져 ( https://portal.azure.com/#home )에 들어가신 후 백엔드가 배포되어있는 리포지터리(https://portal.azure.com/#@hackersground.kr/resource/subscriptions/bfa39d86-1058-4824-8074-e9d283d6c321/resourceGroups/rg-good-tshirt/overview)에 들어가주세요
   ![image](https://github.com/user-attachments/assets/80ae99e9-ee72-4eb2-a7b7-a7385a67ba38)

3.	  리포지터리에서 만들기를 눌러주세요
   ![image](https://github.com/user-attachments/assets/2bf51de8-4147-4e75-aa4b-e29d9c5b54d7)

4.	  마켓 플레이스에서 정적 웹앱을 눌러주세요
   ![image](https://github.com/user-attachments/assets/11a30f05-8bbb-4fa9-9fca-3238a58dc85f)

5.	 만들기를 눌러주세요
   ![image](https://github.com/user-attachments/assets/8810160f-7d02-46d1-8062-4790d8e0b3b7)
 
6.	구독과 리소스 그룹은 건드리지 않고 이름을 sodamf로 입력해주세요

7.	Github 계정을 자신의 깃허브 계정으로 로그인해주세요
![image](https://github.com/user-attachments/assets/4f30a922-9568-4c52-9f2d-adf0992b7a57)
 
8.	1번에서 Fork한 조직을 선택하신 이후 리포지토리에서 SODAM_WEB_V1을 선택해주세요

9.	검토 + 만들기를 눌러주세요.

10.	만들기를 눌러주세요
 ![image](https://github.com/user-attachments/assets/83298d21-0a89-4458-bb56-7d74f29b38ad)

11.	배포가 완료되면 sodamf 리소스로 이동해주세요
 ![image](https://github.com/user-attachments/assets/3f4e936a-c24c-4ba5-80dc-e8f6e45a4711)

12.	리소스에서 Github 작업 실행을 눌러주세요.

13.	액션이 완료되었다면 프론트엔드 배포 끝입니다!


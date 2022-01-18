---
## github.io에 FLUTTER 적용하기
---
#### 1. Prerequsites
* STEP1. [Flutter 설치](https://docs.flutter.dev/get-started/install)
* STEP2. Flutter web support 추가
    * cmd 실행
    ```markdown
    $ flutter channel
    ```
    ```markdown
    $ flutter channel beta
    $ flutter upgrade
    $ flutter config --enable-web
    ```
    * Web support가 추가된 경우, device목록에 chrome이 있음
     ```markdown
    $ flutter devices
    ```
* (Optional) beta채널에서 stable채널로 변경
    ```markdown
    $ flutter channel stable
    ```
* (Optional) flutter 버전 최신화
    ```markdown
    $ flutter upgrade
    ```
---
#### 2. Develop & Test
```markdown
$ flutter run -d chrome
```
---
#### 3. Deploy
* STEP1. Build
```markdown
$ flutter build web
```
* STEP2. Replace
    - github.io 를 호스팅하는데 이용되는 repository(=vegart.github.io) 소스를 build web 명령 실행을 통해 생성된 build/web 하위의 소스로 replace해야함
    - 해당 repo를 clone한 이후, flutter 의 build/web 소스로 덮어쓰고 다시 remote로 올려주기
---
#### 4. Appendix
* 4-1. 출처 
    * [https://kim66s.medium.com/beginners-guide-to-flutter-web-set-up-to-deployment-39c967d7dfae](https://kim66s.medium.com/beginners-guide-to-flutter-web-set-up-to-deployment-39c967d7dfae) 
* 4-2. github.io 접근 시, 바로 index.html 이동하는 법
  * REPO -> Settings -> Pages 이동
  * Build 의 루트 경로를 Branch 의 /root 에서 /doc 으로 변경
* 4-3. [Flutter 샘플화면](https://flutter.github.io/samples/#?platform=web)

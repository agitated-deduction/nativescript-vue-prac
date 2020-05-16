참고 사이트<br>
https://nativescript-vue.org/ko/docs/getting-started/installation/ <br>
https://docs.nativescript.org/start/ns-setup-win <br>
https://kr.vuejs.org/v2/guide/index.html <br>
https://ux.stories.pe.kr/185 <br>

# window에서 nativescript -vue 설치하기

* windows용 패키지 관리 툴인 chocolatey 설치
```
@powershell -NoProfile -ExecutionPolicy unrestricted -Command "iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1'))" && SET PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin
```

* 앱 디버깅 위해 chrome 설치
```
choco install googlechrome -y
```

* node.js LTS 설치
```
choco install nodejs-lts -y
```
* jdk 설치
```
choco install adoptopenjdk --version 8.192
```

* android sdk 설치
```
choco install android-sdk -y
```

* sdk의 패키지 설치
```
"%ANDROID_HOME%\tools\bin\sdkmanager" "emulator" "platform-tools" "platforms;android-28" "build-tools;28.0.3" "extras;android;m2repository" "extras;google;m2repository"
```

### vue.js와 nativeScript 설치

* vue cli 설치

@vue/cli 명령창에서 vue에게 명령 실행시키는 명령어 모음<br>
@vue/cli-init 기초 template을 설치해주는 기능을 제공
```
npm install -g @vue/cli @vue/cli-init
```

* vue를 모바일앱으로 변환해주는 nativeScript cli 설치
```
npm install -g nativescript
```



* 설치 및 설정 확인하기
```
tns doctor
```
No issues were detected. 라는 메세지가 나오면 정상적으로 설치 완료.



# 프로젝트 생성 및 실행
생성
```
$ vue init nativescript-vue/vue-cli-template <project-name>
$ cd <project-name>
$ npm install
```
스마트폰 설정<br>
1. usb 드라이버 설치<br>
2. 디버깅 모드로 전환<br>
  설정 > 휴대전화 정보 > 소프트웨어 정보 > 빌드번호 (연타) > 설정 (설정화면으로 돌아가기) > 개발자 옵션 > usb디버깅모드 활성화
  
  
실행
```
$ tns run
```

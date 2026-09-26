카테고리 메모장 PWA

구성:
- index.html
- manifest.webmanifest
- sw.js
- icons/icon-192.png
- icons/icon-512.png

중요:
PWA의 '홈 화면에 추가' 기능은 Android/Chrome 보안 정책상 일반적인 file:// 파일을 직접 열어서는 설치할 수 없습니다.
최초 설치할 때는 HTTPS 웹사이트 또는 localhost에서 이 폴더를 제공해야 합니다.

컴퓨터에서 테스트:
1. 이 폴더에서 터미널을 엽니다.
2. Python이 있다면:
   python -m http.server 8080
3. 브라우저에서 http://localhost:8080 접속
4. 브라우저 메뉴의 '홈 화면에 추가' 또는 '설치'를 선택합니다.

실제 휴대폰 설치:
이 폴더를 HTTPS가 적용된 웹 호스팅에 업로드한 뒤 Android Chrome에서 접속하고 '홈 화면에 추가/앱 설치'를 선택하면 됩니다.

설치 후에는 Service Worker가 파일을 캐시하므로 인터넷 없이도 앱을 사용할 수 있습니다.

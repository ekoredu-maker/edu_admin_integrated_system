# 교육행정업무 통합 관리 시스템 v6.2 PWA

단일 HTML 시제품을 GitHub Pages 배포에 맞게 `index.html`, `css`, `js`, `assets`, `manifest`, `sw.js` 구조로 분리한 버전입니다.

## 폴더 구조

```text
edu_admin_integrated_system_pwa_v6_2/
├─ index.html
├─ manifest.webmanifest
├─ sw.js
├─ css/
│  └─ style.css
├─ js/
│  └─ app.js
├─ assets/
│  ├─ logo.svg
│  └─ icons/
│     ├─ icon-192.png
│     └─ icon-512.png
└─ .nojekyll
```

## GitHub Pages 배포 방법

1. 새 GitHub 저장소를 만듭니다.
2. 이 폴더 안의 파일들을 저장소 루트에 업로드합니다. `index.html`이 루트에 있어야 합니다.
3. 저장소의 `Settings` → `Pages`로 이동합니다.
4. `Build and deployment`에서 `Deploy from a branch`를 선택합니다.
5. Branch는 `main`, Folder는 `/root`를 선택하고 저장합니다.
6. 생성된 GitHub Pages 주소로 접속합니다.

## 초기 계정

- ID: `admin`
- PW: `edu2026!`

현재 로그인은 서버 인증이 아니라 로컬 화면 잠금 방식입니다. 실제 업무 운영용으로 개인정보·민감자료를 다루려면 서버 인증, 사용자별 권한, 암호화 저장 구조가 필요합니다.

## 이번 분리판에서 반영한 것

- CSS를 `css/style.css`로 분리
- JavaScript를 `js/app.js`로 분리
- PWA용 `manifest.webmanifest` 추가
- `sw.js` 서비스워커 추가
- GitHub Pages용 상대경로 적용
- 아이콘 및 로고 자산 추가
- RTF 다운로드 함수 중복 선언 문제 정리
- v5/v6/v6.1 혼재 문구를 v6.2 PWA 방향으로 정리

## 캐시 주의

브라우저 캐시 때문에 이전 버전이 보이면 강력 새로고침을 하거나 개발자도구 Application 탭에서 기존 Service Worker와 Cache Storage를 삭제하세요.

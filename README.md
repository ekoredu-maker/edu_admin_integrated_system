# 교육행정업무 통합 관리 시스템 v6.2.4 PWA

단일 HTML 시제품을 GitHub Pages 배포에 맞게 `index.html`, `css`, `js`, `assets`, `manifest`, `sw.js` 구조로 분리한 버전입니다.

## 폴더 구조

```text
edu_admin_integrated_system_pwa_v6_2_4_full/
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
│     ├─ icon.svg
│     ├─ icon-192.png
│     └─ icon-512.png
└─ .nojekyll
```

## 초기 계정

- ID: `admin`
- PW: `1234`

현재 로그인은 서버 인증이 아니라 로컬 화면 잠금 방식입니다. 실제 업무 운영용으로 개인정보·민감자료를 다루려면 서버 인증, 사용자별 권한, 암호화 저장 구조가 필요합니다.

## v6.2.4 주요 변경

- 문서 자동 생성에서 `겉공문`과 `붙임 파일`의 역할을 분리했습니다.
- `겉공문 생성` 버튼은 케이에듀파인 본문에 붙여넣기 좋은 공문 본문을 생성합니다.
- `붙임 계획서 생성` 버튼은 표지와 목차형 계획서를 갖춘 별도 첨부문서를 생성합니다.
- `공문+붙임 각각 다운로드` 버튼으로 겉공문 RTF와 붙임 계획서 RTF를 연속 다운로드합니다.
- 신규 사업 생성 화면에 붙임 계획서용 입력값을 추가했습니다.
  - 추진 배경
  - 실태 분석
  - 세부 추진 내용
  - 기대 효과
- 붙임 계획서 구조를 다음 순서로 구성했습니다.
  - 표지
  - Ⅰ. 운영 근거
  - Ⅱ. 추진 배경
  - Ⅲ. 추진 목적
  - Ⅳ. 실태 분석
  - Ⅴ. 추진 방향
  - Ⅵ. 추진 개요
  - Ⅶ. 추진 체계
  - Ⅷ. 세부 추진 계획
  - Ⅸ. 예산 운영 계획
  - Ⅹ. 기대 효과
  - Ⅺ. 결재 및 붙임
- Service Worker 캐시명을 `edu-admin-integrated-v6-2-4-attachment`로 변경했습니다.

## GitHub Pages 배포 방법

1. 새 GitHub 저장소를 만듭니다.
2. 이 폴더 안의 파일들을 저장소 루트에 업로드합니다. `index.html`이 루트에 있어야 합니다.
3. 저장소의 `Settings` → `Pages`로 이동합니다.
4. `Build and deployment`에서 `Deploy from a branch`를 선택합니다.
5. Branch는 `main`, Folder는 `/root`를 선택하고 저장합니다.
6. 생성된 GitHub Pages 주소로 접속합니다.

## 캐시 주의

브라우저 캐시 때문에 이전 버전이 보이면 강력 새로고침을 하거나 개발자도구 Application 탭에서 기존 Service Worker와 Cache Storage를 삭제하세요.

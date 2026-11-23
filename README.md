# IMMUNE RUSH

**인체 속 면역 레이싱 · 공개 테스트 빌드 0.1.0**

IMMUNE RUSH는 미래형 인체 터널을 질주하며 **빨간 좀비세포만 직접 골라 공격하는** 브라우저 아케이드 게임입니다.

## 지금 플레이하기

GitHub Pages 배포가 완료되면 아래 주소에서 설치 없이 플레이할 수 있습니다.

**https://utokyomedlee-lab.github.io/immune-rush/**

## 30초 시작 안내

1. 위 플레이 링크를 엽니다.
2. 화면 하단의 **슬라이드 출발** 버튼을 누릅니다.
3. 마우스 또는 손가락으로 빨간 좀비세포를 터치해 공격합니다.
4. 초록 정상세포는 공격하지 않습니다.
5. 좀비세포 15마리를 제거하면 구역 방어에 성공합니다.

## 조작법

| 조작 | 기능 |
|---|---|
| 마우스 이동 / 손가락 드래그 | 면역세포의 슬라이드 위치 조정 |
| 빨간 세포 클릭 / 탭 | 선택 공격 |
| ← / → 또는 A / D | 좌우 이동 |
| Space | 시작 / 일시정지 |
| 하단 다시 시작 버튼 | 새 게임 |

## 게임 특징

- 네온 스타일의 인체 내부 터널과 워터슬라이드 질주
- 빨간 좀비세포를 직접 겨냥하는 선택 공격
- 정상세포 보호와 연속 명중 콤보
- 면역 방어력, 점수, 처치 수 HUD
- PC와 모바일 브라우저용 터치·마우스 조작

## 기술 구성 및 개인정보

- 단일 `index.html`로 실행되는 HTML5 Canvas, CSS, Vanilla JavaScript 게임
- 설치, 별도 빌드 도구, 외부 게임 라이브러리 불필요
- 현재 게임 코드에는 계정 생성, 광고 SDK, 분석 스크립트, 외부 API 호출 기능이 포함되어 있지 않습니다.
- 호스팅 사업자는 자체 서비스 운영 및 보안 목적으로 접속 관련 기술 정보를 처리할 수 있습니다. 자세한 내용은 [개인정보 안내](PRIVACY-KO.md)를 확인하세요.

## 개발 및 배포

GitHub Pages는 GitHub Actions로 배포하도록 구성되어 있습니다.

1. 저장소의 **Settings → Pages**로 이동합니다.
2. **Build and deployment → Source**에서 **GitHub Actions**를 선택합니다.
3. `main` 브랜치에 변경사항이 올라오면 `.github/workflows/pages.yml`이 사이트를 자동 배포합니다.
4. 배포 결과는 **Actions** 탭에서 확인할 수 있습니다.

GitHub Pages 안내: https://docs.github.com/en/pages

## 문서

- [게임 안내 및 면책](DISCLAIMER-KO.md)
- [개인정보 안내](PRIVACY-KO.md)
- [공개 전 체크리스트](PUBLICATION-CHECKLIST-KO.md)

## 이용 및 재사용

현재 저장소에는 별도 오픈소스 라이선스를 부여하지 않았습니다. 공개 저장소에서 코드를 열람할 수 있다는 사실만으로 복제·수정·재배포·상업적 이용 권한이 생기는 것은 아닙니다. 이용 허락이나 라이선스 관련 문의는 저작권자에게 확인해 주세요.

## 버전

- 공개 테스트 빌드: `0.1.0`
- 게임 진입 파일: `index.html`

## GitHub → itch.io 게시

GitHub의 최신 게임을 itch.io에 업데이트하려면 [ITCHIO-PUBLISHING-KO.md](ITCHIO-PUBLISHING-KO.md)를 따라 `BUTLER_API_KEY` Secret을 등록하고 Actions에서 게시 워크플로를 실행하세요.

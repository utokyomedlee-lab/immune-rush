# GitHub → itch.io 게시 안내

이 저장소의 `main/index.html`을 기존 itch.io 프로젝트에 HTML5 웹 빌드로 올리는 방법입니다.

## 1. itch.io API key를 GitHub Secret으로 등록

1. itch.io 계정에서 **Account Settings → API Keys**를 엽니다.
2. Butler/Wharf 업로드에 사용할 API key를 생성하거나 확인합니다.
3. GitHub 저장소의 **Settings → Secrets and variables → Actions**로 이동합니다.
4. **New repository secret**을 누릅니다.
5. 이름을 정확히 `BUTLER_API_KEY`로 입력하고 itch.io API key를 값에 붙여넣어 저장합니다.

**중요:** API key를 코드, README, 공개 이슈, 채팅에 붙여넣지 마세요. GitHub Secret에만 저장해야 합니다.

## 2. itch.io 업로드 실행

1. 저장소의 **Actions** 탭을 엽니다.
2. **Publish IMMUNE RUSH to itch.io** 워크플로를 선택합니다.
3. **Run workflow**를 누릅니다.
4. Project slug에는 itch.io 게임 주소에서 도메인 뒤의 경로를 입력합니다. 예: `https://utokyomedlee-lab.itch.io/immune-rush`라면 `immune-rush`입니다.
5. Version은 `0.1.0`을 사용하고 실행합니다.

이 작업은 GitHub 저장소의 최상위 `index.html`만 업로드합니다. 다른 저장소 문서나 워크플로 파일은 게임 빌드에 포함하지 않습니다.

## 3. itch.io 프로젝트 페이지 설정

업로드가 성공한 후 itch.io에서 **Edit game**을 열고 다음을 확인합니다.

- Kind of Game: **HTML**
- 업로드된 `html5` 채널: **HTML5 / Playable in browser**로 표시
- Embed options: 필요에 따라 **Embed in page** 또는 **Click to launch in fullscreen** 선택
- 변경사항 저장 후 공개 페이지에서 플레이 테스트

itch.io는 HTML5 게임 ZIP에 루트의 `index.html`을 요구하며, 프로젝트를 HTML 유형으로 설정해야 브라우저에서 실행할 수 있습니다. [공식 HTML5 안내](https://itch.io/docs/creators/html5)

## 4. 자동 업데이트

현재 워크플로는 보안을 위해 수동 실행(`workflow_dispatch`)입니다. GitHub의 게임 코드를 변경한 뒤 Actions에서 다시 실행하면 동일한 itch.io 프로젝트의 `html5` 채널이 업데이트됩니다.

## 주의

- Butler는 기존 itch.io 프로젝트에 빌드를 올립니다. 프로젝트 페이지를 새로 생성하지 않습니다.
- Project slug가 기존 게임 URL과 정확히 일치해야 합니다.
- itch.io 계정의 API key가 GitHub Actions Secret에 등록되어 있어야 합니다.

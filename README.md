# 그릇그릇 가득가득

Netlify에 바로 배포할 수 있는 정적 웹사이트입니다. 별도의 빌드나 서버 설정 없이 `index.html`, `style.css`, `app.js`, `public/images/`를 함께 게시하면 됩니다.

## 기능

- 도자기 이미지 17종 선택 (목록용 투명 썸네일로 빠르게 표시)
- 그릇 유약 색과 장식 색 편집
- 투명 배경의 그릇 실루엣 미리보기
- Windows용 `.ico` 다운로드
- Mac Finder에서 파일·폴더 아이콘으로 사용할 1024×1024 PNG 한 장이 담긴 `.zip` 다운로드
- IndexedDB에 작품과 유약·장식 색 조합(내 스타일) 저장
- 여러 그릇을 골라 한 번에 작품으로 저장
- 장식 자동 인식 미리보기, 직접 칠하기 실행 취소
- 작품 그룹 이름 변경 및 삭제 (삭제한 그룹 작품은 그룹 없음으로 이동)
- 내 작품 창에서 사용자 그룹을 만들고 그릇을 그룹별로 정리

## Netlify 배포

1. Netlify에서 새 사이트를 만들고 수동 배포(Deploy manually)를 선택합니다.
2. `index.html`, `style.css`, `app.js`, `netlify.toml`, `public/`가 들어 있는 폴더 또는 ZIP을 올립니다.
3. 빌드 명령은 비워 두고 게시 디렉터리는 프로젝트 최상위(`.`)로 둡니다. `netlify.toml`이 게시 디렉터리를 지정합니다.

## 로컬 미리보기

프로젝트 폴더에서 `python3 -m http.server 8000`을 실행하고 `http://localhost:8000`을 엽니다.

## GitHub Pages 배포

저장소의 `main` 브랜치에 변경 사항을 올리면 GitHub Actions가 사이트를 자동 배포합니다.

1. GitHub에서 새 저장소를 만듭니다. 공개 사이트로 배포하려면 저장소 공개 설정을 선택하세요.
2. 이 프로젝트 폴더를 그 저장소에 `main` 브랜치로 올립니다.
3. GitHub 저장소의 **Settings → Pages → Build and deployment → Source**에서 **GitHub Actions**를 선택합니다.
4. **Actions** 탭에서 `Deploy website to GitHub Pages` 작업이 끝나면 공개된 주소가 표시됩니다. 보통 `https://계정이름.github.io/저장소이름/` 형식입니다.

이후 `main`에 새 커밋을 올릴 때마다 자동으로 다시 배포됩니다. 사이트 데이터와 저장한 스타일·작품 그룹은 방문자 각자의 브라우저에 저장됩니다.

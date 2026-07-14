# October Sky 회사 사이트 — GitHub Pages 배포 가이드

## 1. 로컬에서 git 초기화

```bash
cd octobersky-site
git init
git add .
git commit -m "Initial commit: October Sky landing page"
```

## 2. GitHub에 새 리포지토리 생성

GitHub 웹에서 새 저장소를 만듭니다. 두 가지 선택지가 있습니다.

- **`october-sky.github.io` 형태의 이름으로 만들면** → 별도 설정 없이 `https://<계정명>.github.io` 로 바로 접속 가능
- **`octobersky-site` 처럼 일반 이름으로 만들면** → `https://<계정명>.github.io/octobersky-site/` 경로로 접속 (아래 3번에서 Pages를 켜야 함)

## 3. 원격 저장소 연결 후 푸시

```bash
git remote add origin https://github.com/<계정명>/<저장소명>.git
git branch -M main
git push -u origin main
```

## 4. GitHub Pages 활성화

1. 리포지토리 → **Settings** → **Pages**
2. **Source**를 `Deploy from a branch`로 설정
3. Branch를 `main`, 폴더는 `/ (root)` 선택 후 저장
4. 1~2분 후 상단에 뜨는 URL로 접속 확인

## 5. (선택) 커스텀 도메인 연결

`octobersky.com` 같은 도메인을 이미 갖고 계시다면:
- 리포지토리 루트에 `CNAME` 파일 하나 추가 (내용: `octobersky.com`)
- 도메인 등록업체 DNS에 GitHub Pages IP로 A 레코드 4개(또는 CNAME) 추가
- Settings → Pages → Custom domain에 도메인 입력

## 파일 구성

```
octobersky-site/
├── index.html   ← 페이지 전체 (HTML/CSS/JS 한 파일에 포함)
└── README.md
```

## 수정하고 싶을 때

`index.html` 상단 `:root` 안의 CSS 변수(`--gold`, `--ew`, `--stetho`, `--wolf` 등)로 색상을,
`Apps` 섹션의 `<article class="app-card ...">` 블록으로 앱 소개 문구·링크·상태 배지를 바로 수정할 수 있습니다.
Stetho 심사 통과, WOLF 출시 확정되면 `app-status` 텍스트와 `Coming soon` 링크를 실제 스토어 링크로 바꿔주시면 됩니다.
# octobersky
# octobersky

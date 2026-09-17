# Design After AI : How AI Is Changing the Design Process

**AI 시대의 서비스 디자인** — 강의 슬라이드 138장 (HTML, 1920×1080)
Soomin Kim · smsoominkim@gmail.com

> 라이브 : https://soominkim.github.io/design-after-ai/

## 보는 법

| 동작 | 키 / 제스처 |
|---|---|
| 다음 · 이전 | `→` `←` , `↓` `↑` , `Space` , `PageDown` `PageUp` , 마우스 휠, 모바일 스와이프 |
| 처음 · 끝 | `Home` · `End` |
| 특정 장으로 바로 가기 | 주소 뒤에 `#번호` (예 `…/#37`) |
| 편집 모드 (로컬에서만, 내 브라우저에 저장) | `E` 또는 좌상단 모서리 클릭 |

화면 크기에 맞춰 자동으로 축소·확대됩니다. 처음 열 때 138장의 이미지(약 18 MB)를 한 번에 불러오므로 첫 로딩에 몇 초 걸릴 수 있습니다.

## GitHub Pages에 올리기

1. GitHub에서 새 저장소를 만듭니다 (Public).
2. 이 폴더의 내용을 저장소 루트에 올립니다. 터미널에서:

   ```bash
   cd design-after-ai
   git init
   git add .
   git commit -m "Design After AI slides"
   git branch -M main
   git remote add origin https://github.com/<아이디>/<저장소>.git
   git push -u origin main
   ```

   (또는 GitHub 웹에서 *Add file → Upload files* 로 끌어다 놓아도 됩니다. 단, 웹 업로드는 한 번에 100개 파일까지라 `images/`(120장)는 두 번에 나눠 올려야 합니다. 숨김 파일 `.nojekyll`도 잊지 마세요.)
3. 저장소 **Settings → Pages → Build and deployment**
   - Source : **Deploy from a branch**
   - Branch : **main** / **/(root)** → Save
4. 1~2분 뒤 `https://<아이디>.github.io/<저장소>/` 에서 열립니다.

## 폴더 구성

```
design-after-ai/
├── index.html      # 슬라이드 본문 (CSS·JS 포함, 단일 파일)
├── images/         # 슬라이드에서 실제로 쓰는 이미지 120장 (상대 경로 images/…)
├── .nojekyll       # GitHub Pages의 Jekyll 처리 비활성화
├── .gitignore      # .DS_Store 제외
└── README.md
```

- 경로는 모두 상대 경로라서 저장소 이름이 무엇이든, 하위 폴더에 두어도 그대로 동작합니다.
- 웹폰트(Pretendard, JetBrains Mono)는 CDN(jsDelivr, Google Fonts)에서 불러옵니다. 오프라인에서는 시스템 폰트로 대체됩니다.
- 이미지는 웹용으로 최적화했습니다 (긴 변 최대 2200px, 스크린샷 PNG → JPEG 품질 88). 원본은 `AI+Design/slide/images/`에 그대로 있습니다.
- 슬라이드 내용을 고칠 때는 `index.html`의 `<!-- 001 -->` … `<!-- 138 -->` 주석으로 장표를 찾으면 됩니다.

## 링크 공유 미리보기 (선택)

SNS·메신저에서 미리보기 이미지를 띄우려면 표지 캡처(예 `cover.png`, 1200×630 권장)를 저장소에 넣고 `index.html` `<head>`의 OG 메타 아래에 한 줄을 추가하세요. og:image는 절대 URL이어야 합니다.

```html
<meta property="og:image" content="https://<아이디>.github.io/<저장소>/cover.png">
```

## 저작권

슬라이드 구성과 글 © Soomin Kim. 인용된 그림·스크린샷·기사 이미지는 각 저작권자의 것이며 교육 목적으로 출처를 표기해 인용했습니다.

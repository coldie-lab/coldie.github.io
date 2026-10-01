# 김해찬 개인 홈페이지

GitHub Pages에서 별도 빌드 없이 동작하는 정적 개인 홈페이지입니다.

## 로컬에서 확인하기

```bash
python3 -m http.server 8000
```

브라우저에서 `http://localhost:8000`을 엽니다. `file://`로 직접 열면 Markdown 문서를 불러올 수 없습니다.

## 개인정보 교체

- 이름과 소개: `index.html`, `about/index.html`
- 프로필 사진: `assets/profile-placeholder.svg`를 본인 사진으로 교체하거나 HTML의 이미지 경로를 수정
- CV: `about/index.html`
- GitHub·이메일 링크: 각 HTML의 푸터

## 문서 추가

1. `content/` 아래에 Markdown 파일을 만듭니다.
2. 파일 맨 위에 메타데이터를 작성합니다.

```md
---
title: 문서 제목
category: 개발/웹
date: 2026-10-01
tags: [JavaScript, 기록]
summary: 목록에 표시할 한 줄 설명
---

# 문서 제목

본문을 작성합니다.
```

3. `content/manifest.json`의 `documents` 배열에 경로를 추가합니다.

카테고리에 `/`를 사용하면 나무위키 분류처럼 계층적으로 표시됩니다. 예: `개발/웹`, `개발/데이터`.

## GitHub Pages 배포

1. 이 폴더의 파일을 `username.github.io` 저장소의 기본 브랜치 루트에 올립니다.
2. 저장소의 **Settings → Pages**에서 **Deploy from a branch**를 선택합니다.
3. 기본 브랜치와 `/ (root)`를 선택해 저장합니다.

배포 후 주소는 `https://username.github.io`입니다.


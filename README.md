# seiwoonghong.com — 배포 & 관리 가이드

## 파일
```
index.html      About (사진, 한 줄 연구 소개, job market, 연락처, References)
research.html   JMP / Working Paper / Work in Progress
cv.html         CV PDF 임베드 + 다운로드
teaching.html   Corporate Finance (BUSFIN 4211)
style.css       디자인 (흰 배경, 네이비 포인트 --accent)
CNAME           seiwoonghong.com
sitemap.xml, robots.txt   구글 검색용
assets/
  profile.jpg           ← 직접 넣기 (지금 없음)
  CV_SeiwoongHong.pdf
  Hong_JMP.pdf          ← 새 버전 나오면 같은 이름으로 덮어쓰기
  Hong_RareDisease.pdf
```
PDF는 **항상 같은 파일명으로 덮어쓰기** → 논문 안의 "Link to the Most Recent Version" 링크가 언제나 최신본을 가리킴.

## 1. GitHub Pages 올리기
1. github.com에서 새 repo: `<아이디>.github.io` (Public)
2. 이 폴더 안 파일 전부 업로드 (Add file → Upload files, `assets` 폴더째 드래그)
3. Settings → Pages → Branch `main` / `(root)` → Save

## 2. 도메인 연결
1. `seiwoonghong.com` 구매 (Cloudflare / Porkbun / Namecheap, 연 $10~15)
2. DNS에 추가:
   - A `@` → 185.199.108.153 / 185.199.109.153 / 185.199.110.153 / 185.199.111.153 (4개)
   - CNAME `www` → `<아이디>.github.io`
3. Settings → Pages → Custom domain에 `seiwoonghong.com` → 반영 후 **Enforce HTTPS** 체크

## 3. 구글에서 이름 검색 시 1등 만들기
1. **Google Search Console** (search.google.com/search-console) → 도메인 추가 → DNS TXT로 소유 확인
   → Sitemaps에 `sitemap.xml` 제출 → URL 검사에서 홈페이지 "색인 생성 요청"
2. **옛 Google Sites 정리**: 홈 화면을 "My website has moved to seiwoonghong.com" 한 줄 + 링크만 남기고,
   일주일쯤 뒤 unpublish. (두 사이트가 같이 있으면 검색 순위가 나뉨)
3. **링크 걸기** (구글 순위에 제일 효과 큼): OSU Fisher PhD student 프로필, SSRN author page,
   Google Scholar, LinkedIn, CV, Research Statement, 논문 첫 페이지 → 전부 `https://seiwoonghong.com`
4. 보통 1~2주 안에 이름 검색 1위로 올라옴.

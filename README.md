# Sooyoung Ryu

개인 홈페이지: <https://sooyoung-ryu.github.io/>

[Jon Barron의 공식 소스](https://github.com/jonbarron/jonbarron.github.io)를 바탕으로 만든 단일 HTML 홈페이지입니다. 원본 `stylesheet.css`는 수정하지 않았으며, 800px 표 기반 배치·글꼴·색상·논문 목록 형식을 유지합니다. 별도 메뉴나 블로그 탭은 없습니다.

## 내용 수정

- 소개·연락처·논문 목록: `index.html`
- 프로필 사진: `images/sooyoung-ryu.jpeg`
- Q-Drift 그림과 BibTeX: `images/q-drift.jpg`, `data/q-drift.bib`

## 블로그 글을 프로젝트 페이지로 추가

1. `_templates/project-page.html`을 `projects/<slug>/index.html`로 복사합니다.
2. 제목·날짜·본문의 대문자 자리표시자를 실제 내용으로 교체합니다. 그림도 같은 폴더에 둡니다.
3. 홈페이지 `index.html`의 Publications 표에서 Q-Drift의 `<tr>...</tr>` 한 줄을 복사하여 새 글을 추가합니다.
4. 제목과 `blog post` 링크는 `projects/<slug>/`로 연결합니다. 논문 학회명 대신 `<em>Blog post</em>, YEAR`를 표시하여 논문과 글을 구분합니다. 해당하지 않는 arXiv·code·bibtex 링크는 제거합니다.

논문과 글은 같은 목록에 최신 항목부터 배치합니다. `_templates`는 작성용이며 배포하지 않습니다. 실제 블로그 글이나 빈 프로젝트 페이지는 아직 게시하지 않았습니다.

## 배포와 미리보기

GitHub Settings → Pages → Source를 **GitHub Actions**로 설정합니다. `main`에 저장하면 정적 파일을 그대로 배포합니다. Ruby, Jekyll, Node.js 빌드가 필요하지 않습니다.

로컬 확인: `python3 -m http.server 4000` 실행 후 <http://127.0.0.1:4000/>에 접속합니다.

## 원본 및 자료

- 템플릿 기준: `jonbarron/jonbarron.github.io`, commit `25905bd773bd778585e66725780a7bc589269af1`.
- 원본 README: “This is the source code to Jon Barron's public academic website: https://jonbarron.info/. Feel free to clone this code for your own personal use.”
- 원본은 개인 사용을 허용하며, 별도의 MIT 라이선스를 명시하지 않습니다. 홈페이지 하단에 출처를 표시했습니다.
- 소개·사진: Sooyoung Ryu 제공. Chelsea Finn 교수님과의 협업은 원격 연구로 명시합니다.
- 논문: <https://arxiv.org/abs/2603.18095>. 학회 게재가 아닌 arXiv preprint로 표시합니다.
- 그림: 본인의 [Q-Drift 저장소](https://github.com/sooyoung-ryu/Q-Drift/blob/0674c2ba9131f5a9339ad059d76c977305cc174c/assets/teaser.jpg)에서 수정 없이 가져왔습니다.

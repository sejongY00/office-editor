# office-editor

[ranuts/document](https://github.com/ranuts/document)(ONLYOFFICE 편집기 + x2t WebAssembly, AGPL-3.0)를
고정 버전으로 빌드해 GitHub Pages에 올리는 저장소. 소스는 담지 않고 워크플로만 둔다.

- 사이트: https://editor.sejong.dev/ (Cloudflare CNAME → `sejongy00.github.io`). **도메인 루트 필수** — ranuts가 `/sdkjs/…` 루트 절대 경로를 써서 `github.io/office-editor/` 하위 경로에선 x2t 워커가 404
- 쓰는 곳: [sejong-office](https://github.com/sejongY00/sejong-office)가 새 탭(`/editor?new=docx` 등)으로 연다. iframe 임베드([embed API](https://github.com/ranuts/document/blob/main/docs/embed-api.md))는 COOP/COEP 헤더가 필요해 GitHub Pages에선 불가
- 업데이트: `.github/workflows/pages.yml`의 `RANUTS_REF`를 새 태그로 바꿔 push
- 파일은 브라우저 안에서만 처리된다. 서버는 정적 파일만 준다

라이선스: 빌드 결과물은 ranuts/document의 AGPL-3.0을 따른다. 소스는 위 저장소의 해당 태그.

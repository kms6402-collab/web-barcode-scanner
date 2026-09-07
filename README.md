# web-barcode-scanner

카메라 전환 없이 후면 카메라 하나로 바코드를 스캔하고, 화면 중앙 스캔 라인 위에 판독값을 즉시 표시하는 모바일 웹 바코드 리더입니다.

## 사용 방법

GitHub Pages로 이 저장소를 배포하면 `https://kms6402-collab.github.io/web-barcode-scanner/` 에서 바로 열 수 있습니다.

1. 저장소 **Settings → Pages**
2. Source: **Deploy from a branch**, Branch: **main** / **(root)** 선택 → Save
3. 몇 분 후 생성되는 링크를 휴대폰 브라우저로 열고 카메라 권한을 허용

카메라 접근에는 HTTPS(또는 localhost)가 필요하므로, GitHub Pages처럼 실제 HTTPS 주소로 열어야 정상 동작합니다.

## 주요 기능

- 후면 카메라 고정 사용 (카메라 전환 UI 없음)
- 화면 중앙 스캔 라인 위에 판독값 실시간 표시
- 브라우저 네이티브 `BarcodeDetector` API 우선 사용 (미지원 브라우저는 QuaggaJS로 자동 폴백)
- 바코드 값 직접 검색 시 부분 문자열로 유사/동일 항목 탐색 및 후보 목록 제공
- 등록된 바코드 태그 ↔ 시리얼(S/N) 매핑 데이터 137건 내장 (`index.html`의 `barcodeDatabase`)

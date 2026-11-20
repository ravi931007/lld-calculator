# 소아 하지부동(LLD) 성장 계산기 (PWA)

외부 CDN 없이 오프라인 및 병원 내부망에서도 동작하는 소아 정형외과 하지부동 성장 계산기 PWA 패키지입니다.

## 포함된 파일
- `index.html`: 앱 본체 (Multiplier, White-Menelaus, Moseley 직선 그래프, 다회계측 회귀분석, EMR 요약표, 오프라인 순수 Canvas 차트 내장)
- `manifest.json`: 스마트폰 홈 화면 앱 설치용 웹 매니페스트 (상대 경로 `./` 기반)
- `sw.js`: 오프라인 캐싱용 서비스 워커
- `icons/icon-192.png`, `icons/icon-512.png`: iOS/Android 앱 아이콘

## 빠른 배포
- **Vercel**: GitHub 저장소에 이 폴더 내부 파일들을 그대로 올린 뒤 Vercel에서 Import → Deploy 클릭
- **GitHub Pages**: 저장소 Settings → Pages → Source: `Deploy from a branch` → `main` / `(root)` 선택 후 저장

## 버전 업데이트 시 주의사항
코드를 수정하여 다시 배포할 때는 `sw.js` 1행의 `CACHE_NAME` 버전(예: `v1.0.0` → `v1.0.1`)을 반드시 올려야 사용자 기기의 구버전 캐시가 교체됩니다.

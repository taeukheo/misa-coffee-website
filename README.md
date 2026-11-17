# 미사커피공방학원 홈페이지

Cloudflare Workers 정적 자산(Static Assets) 배포용 저장소입니다.

## 포함 파일
- `public/`: 홈페이지 정적 파일 (index.html, logo.png, 네이버 사이트 소유확인 파일)
- `src/index.js`: 정적 자산을 반환하는 Worker 엔트리
- `wrangler.jsonc`: 기존 Cloudflare Worker 이름 `nameless-lab-8884`에 맞춘 배포 설정

## Cloudflare Workers Builds 연결 설정
- Git branch: `main`
- Root directory: `/` (저장소 루트)
- Build command: 비워 둠
- Deploy command: `npx wrangler deploy`
- Preview command: 기본값 사용 또는 비워 둠

주의: Cloudflare 대시보드에서 기존 Worker의 Settings > Builds > Connect로 Git 저장소를 연결한 뒤에만 자동 배포가 시작됩니다. 이 저장소를 연결하기 전에는 기존 운영 사이트가 변경되지 않습니다.

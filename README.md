# 왕가네 헬로

배포 플랫폼 시연용 작은 Node 서버입니다. 설치할 의존성이 없습니다.

| 경로 | 응답 |
| --- | --- |
| `GET /` | 소개 화면 (서버 시각 · 켜진 시간 · 방문 수 · 비밀값 설정 여부) |
| `GET /api/health` | `200 {"ok":true}` |
| `GET /api/info` | `{ time, uptimeSeconds, visits, hasApiKey }` |

## 배포 설정

- Dockerfile: `Dockerfile` (루트)
- 실행 방식: 서버(server), 포트 `8080`
- 공개 경로: `/`
- 동작 확인: http `/api/health`
- 비밀값: `DEMO_API_KEY` (아무 값이나. 화면에는 들어 있는지만 보이고 값은 보이지 않습니다)

## 로컬 실행

```bash
node server.js            # http://localhost:8080
DEMO_API_KEY=x node server.js
```

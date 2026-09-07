# CATSMARKET Web

냥코 대전쟁 아이템 · 웹 자판기

## 로컬 실행
```bash
npm install
npm start
```

기본 주소: `http://localhost:3000`

## Render 배포
Render에서 **Web Service**로 이 프로젝트를 연결하면 됩니다.
- Build Command: `npm install`
- Start Command: `npm start`
- Health Check Path: `/health`

`render.yaml`도 포함되어 있어 Blueprint 배포에도 사용할 수 있습니다.

## 중요 환경변수
Discord 로그인과 관리자 기능을 사용하려면 Render의 Environment에 기존 `.env` 값을 등록하세요.

```text
DISCORD_CLIENT_ID=
DISCORD_CLIENT_SECRET=
DISCORD_REDIRECT_URI=https://<렌더주소>/auth/discord/callback
ADMIN_DISCORD_IDS=
SESSION_SECRET=
CATSMARKET_WEB_SECRET=
BASE_URL=https://<렌더주소>
```

은행/충전/VIP/Discord 채널 관련 환경변수는 기존 운영 설정을 그대로 등록하면 됩니다.

## 페이지
- `/` : 고객용 CATSMARKET
- `/admin` : 관리자 패널
- `/health` : Render 상태 확인용

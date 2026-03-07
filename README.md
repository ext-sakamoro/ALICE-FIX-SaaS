# ALICE-FIX SaaS

FIX protocol 4.4/5.0 message processing API

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum, ALICE-FIX |

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST /api/v1/parse` | FIXメッセージパース |
| `POST /api/v1/build` | FIXメッセージ構築 |
| `POST /api/v1/session` | FIXセッション管理 |
| `GET`  | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto

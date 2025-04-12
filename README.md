# Next.js + FastAPI + PostgreSQL Template

このプロジェクトは、Next.js、FastAPI、PostgreSQL を使用したフルスタックアプリケーションのテンプレートです。

## 開発環境

- Frontend: Next.js
- Backend: FastAPI
- Database: PostgreSQL
- コンテナ環境: Docker, Docker Compose

## 環境構築手順

1. リポジトリのクローン

```bash
git clone https://github.com/otaki0413/next-fastapi-postgres-template.git
cd next-fastapi-postgres-template
```

2. Docker コンテナの起動

```bash
docker compose up -d
```

3. アプリケーションへのアクセス

- フロントエンド: http://localhost:3000
- バックエンド: http://localhost:8000
- データベース: localhost:5432
  - User: postgres
  - Password: password
  - Database: test_db

## プロジェクト構成

```
.
├── frontend/         # Next.jsアプリケーション
├── backend/         # FastAPIアプリケーション
│   ├── app/        # APIソースコード
│   ├── Dockerfile  # バックエンド用Dockerfile
│   └── requirements.txt
├── compose.yml     # Docker Compose設定
└── README.md
```

## 開発用コマンド

### Docker 関連

```bash
# イメージ作成 + コンテナの起動
docker compose up -d --build

# コンテナの停止
docker compose down

# ログの確認
docker compose logs frontend  # フロントエンド
docker compose logs backend   # バックエンド
docker compose logs db       # データベース

# イメージ削除 & コンテナ削除
docker compose down --rmi all

# PostgreSQLへの接続
docker exec -it postgres psql -U postgres -d test_db
```

# Next.js + FastAPI Sample Project

このプロジェクトは、Next.js と FastAPI を使用したフルスタックアプリケーションのサンプルです。

## 開発環境

- Frontend: Next.js
- Backend: FastAPI
- コンテナ環境: Docker, Docker Compose

## 環境構築手順

1. リポジトリのクローン

```bash
git clone https://github.com/otaki0413/next-fastapi-sample.git
cd next-fastapi-sample
```

2. Docker コンテナの起動

```bash
docker compose up -d
```

3. アプリケーションへのアクセス

- フロントエンド: http://localhost:3000
- バックエンド: http://localhost:8000

## プロジェクト構成

```
.
├── frontend/          # Next.jsアプリケーション
├── backend/          # FastAPIアプリケーション
│   ├── app/         # APIソースコード
│   ├── Dockerfile   # バックエンド用Dockerfile
│   └── requirements.txt
├── compose.yml      # Docker Compose設定
└── README.md
```

## 開発用コマンド

- コンテナの起動

```bash
docker compose up -d
```

- コンテナの停止

```bash
docker compose down
```

- ログの確認

```bash
# フロントエンド
docker compose logs frontend

# バックエンド
docker compose logs backend
```

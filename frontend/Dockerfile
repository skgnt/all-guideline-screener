# ベースイメージ
FROM node:20-alpine

# 作業ディレクトリの設定
WORKDIR /app

# ホストのpackage.jsonとpackage-lock.jsonをコンテナにコピー
COPY package*.json ./

# 依存関係のインストール
RUN npm install
# Gitのインストール
RUN apk add --no-cache git

# ソースコードをコンテナにコピー
COPY . .

# 開発サーバーの起動
CMD ["npm", "run", "dev", "--", "--host"]

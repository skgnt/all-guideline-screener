# ベースイメージ
FROM python:3.10-slim-buster

# 作業ディレクトリの設定
WORKDIR /app

# ホストのrequirements.txtをコンテナにコピー
COPY requirements.txt ./

# 依存関係のインストール
RUN pip install --no-cache-dir -r requirements.txt
# Gitのインストール
RUN apt-get update && apt-get install -y git

# ソースコードをコンテナにコピー
COPY . .

# FastAPIアプリケーションの起動
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000", "--reload"]

# 手順メモ

TODO: この手順について

## 事前準備

- git
- Node.js v18.18.2
- Docker v23.0.3
- docker-compose v2.17.2

TODO: 事前準備の手順

## AWS CLI のインストール

### AWS CLI とは?

(TODO)

### セットアップ

```bash
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
```

確認

```bash
aws --version
```

構成設定

```bash
aws configure --profile=localstack
# AWS Access Key ID [None]: hogehoge
# AWS Secret Access Key [None]: fugafuga
# Default region name [None]: ap-northeast-1
# Default output format [None]: json
```

## localstack 立ち上げ

### localstack とは?

(TODO)

### 立ち上げ

```bash
docker compose up -d
# docker-compose v1の場合は "docker-compose up -d"
```

コマンド実行してみる

```bash
aws s3 mb s3://localstack-bucket --endpoint-url=http://localhost:4566 --profile localstack
```

...

## CDK を使ってみる

### AWS CDK とは?

(TODO)

### セットアップ

```bash
npm install -g aws-cdk-local aws-cdk
mkdir work
cd work
cdklocal init --language typescript
```

## コードを書く

(TODO)

## デプロイしてみる

```bash
cdklocal bootstrap
cdklocal deploy
```

## 動作確認

(TODO)

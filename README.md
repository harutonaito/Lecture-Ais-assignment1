# Lecture-Ais--assignment1
講義課題用のレポジトリ

## 概要
IaCでサーバ構築を行うために作成したyamlフォルダを公開する
2層構造のDBが構築できる

![サーバ構成図](architecture.png)


## Cloud9上での操作

以下のコマンドをCLoud9のターミナルで実行することで，Cloud Formationでサーバの構築ができる

```deployコマンド
aws cloudformation deploy \
    --template-file DB-app.yaml \
    --stack-name DB-app2Stack \
    --capabilities CAPABILITY_IAM \
    --parameter-overrides \
        DBPassword='(ここでパスワードを設定)' \
        DBInstanceType='db.t3.micro' \
        InstanceType='t3.micro'
```

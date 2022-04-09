# Serverless Framework
## ■概要
AWS オープンソースの、サーバレスアーキテクチャデプロイ用のフレームワーク。
AWS関連のリソースは本フレームワークで生成・管理する。

## ■Install
```sh
npm install serverless
npx serverless --version
  > Framework Core: 3.12.0 (local)
  > Plugin: 6.2.1
  > SDK: 4.3.2 
```

## ■Invoke / Deploy
* Invoke
```sh
npx sls invoke local --function helloWorld
```
* Deploy
```sh
# aws configure設定を事前に通しておく
npx sls deploy --verbose --region ap-northeast-1
```

## ■Delete
```sh
# S3のバケットの中身、DynamoDBのデータなど、あらかじめ削除しておく。
npx serverless remove --verbose --region ap-northeast-1
```

## ■その他Tips
* CloudFormationスタック名はserverless.ymlのserviceによる。
* 


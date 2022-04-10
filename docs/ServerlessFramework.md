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

## ■Project作成
* serverless-plugin-typescriptを利用
  * 参考
    https://team-6.hatenablog.jp/entry/2021/02/14/210839




* 下記は利用しない。
  * middy/sourceMapへの依存があり、利用しにくい。
  * serverless.ymlがtsファイルに置き換わっており、可読性が低い
```sh
npx serverless create --template aws-nodejs-typescript --path ci-api
cd ci-api
npm install
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

## ■Local開発
[Serverless Frmamework](https://www.serverless.com/plugins/serverless-offline)
> This Serverless plugin emulates AWS λ and API Gateway on your local machine to speed up your development cycles. To do so, it starts an HTTP server that handles the request's lifecycle like APIG does and invokes your handlers.
```sh
npm install -D serverless-offline
```

## ■その他Tips
* CloudFormationスタック名はserverless.ymlのserviceによる。
* 


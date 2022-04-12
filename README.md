# gcp-web-backend

Cloud Run + Cloud SQL(MySQL)でDjangoを動かすサンプル。

Cloud Buildでデプロイを実行する。

https://cloud.google.com/python/django/run?hl=jaを参考


## secret managerに以下を追加

| 名前 | 値 |
----|---- 
| django_settings | DATABASE_URL=mysql://${ユーザー名}:${dbパスワード}@//cloudsql${プロジェクトID}:${リージョン}:${dbインスタンス名}/${テーブル名}<br>GS_BUCKET_NAME=${mediaファイル用GCSバケット名}<br>SECRET_KEY=${作成したSECRET_KEY}|
|　superuser_password | Djangoの管理者パスワード |
| serviceurl | Cloud RunのURL (カスタムドメイン利用時は任意のカスタムドメインでのURL) |
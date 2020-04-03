# wmap_infrastructure_wordpress

## 環境
* OS: CentOS7
* Docker: 19.03.7
* Docker Compose: 1.22.0

## 追加でやりたいこと
* DB設定の調整 - とりあえずmy.cnfを追加済み
* セキュリティ面の確認

## 課題
* dockerとfirewalldの競合問題に対処する必要がある。要調査。

## envファイル
このdocker-composeファイルを利用する場合、以下のファイルが必要になります。  
docker-compose.ymlファイルと同階層に設置してください。  

.env

```
# ローカル環境サンプル(.env.sample.local)
DB_NAME=wordpress
DB_USER=wp_user
DB_USER_PASS=wp_passwd
DB_ROOT_PASS=root_passwd
HOST_DOMAIN=localhost
PRODUCTION_STAGE=local
```
```
# ステージング環境サンプル
DB_NAME=wordpress(.env.sample.staging)
DB_USER=wp_user
DB_USER_PASS=wp_passwd
DB_ROOT_PASS=root_passwd
HOST_DOMAIN=st-www.sample-wmapst.net
PRODUCTION_STAGE=staging
```
```
# 本番環境サンプル(.env.sample.production)
DB_NAME=wordpress
DB_USER=wp_user
DB_USER_PASS=wp_passwd
DB_ROOT_PASS=root_passwd
HOST_DOMAIN=www.sample-wmapst.net
PRODUCTION_STAGE=production
```

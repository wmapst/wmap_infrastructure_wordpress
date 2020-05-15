# wmap_infrastructure_wordpress
Dockerを使ったWordPress本番環境運用も見越したDockerComposeです。  
nginxとmysqlの設定ファイルを仮で設置済みです。

## Blog
docker composeでSSL-WordPress 本番環境を構築  
https://www.wmapst.net/programming/20200403-docker-compose-ssl-wordpress-production-env/  
  
https-portalでwww無しからwww有りへのドメインリダイレクト設定[Docker-Compose]  
https://www.wmapst.net/programming/20200429-https-portal-redirect-setting/  

## 使い方
```
git clone https://github.com/wmapst/wmap_infrastructure_wordpress.git
cd ./docker-compose
vi .env # .env.sample.xxxxx を参考にしてください。
docker-compose up -d
```

## 環境
* OS: CentOS7
* Docker: 19.03.7
* Docker Compose: 1.22.0

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
# ステージング環境サンプル(.env.sample.staging)
DB_NAME=wordpress
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

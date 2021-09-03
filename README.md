# Operation

## Run

```shell
touch ./data/env
# productionのredashから環境設定を読み込む
mkdir ./data/postgres-data

cd data
# docker-compose.ymlで、envファイルの参照箇所を変えている

docker-compose run --rm server create_db
docker-compose up -d
```
## Reset Postgres and redis

```
cd data
docker-compose down -v
rm -rf ./postgres-data
mkdir ./postgres-data
docker-compose run --rm server create_db
docker-compose up -d
```

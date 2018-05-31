# superset-test

git clone https://github.com/codeyu/superset-test.git

cd superset-test

docker pull amancevice/superset

mkdir -p data/sqlite

docker run -d  -p 8088:8088 -v $(pwd)/data/sqlite:/var/lib/superset --name superset-new amancevice/superset


docker exec -it superset-new superset-demo


http://localhost:8088

docker stop superset-new


ref：https://github.com/amancevice/superset

bash demo.sh mysql|postgres|sqlite|celery
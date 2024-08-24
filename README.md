# Infra 환경 설정

### MySQL
```bash
# mac
$ docker run --rm -p 3306:3306 -e MYSQL_ROOT_PASSWORD=root1234! -v ./ddl.sql:/docker-entrypoint-initdb.d/init.sql mysql:8.0

# windows (powershell)
$ docker run --rm -p 3306:3306 -e MYSQL_ROOT_PASSWORD=root1234! -v ${PWD}/ddl.sql:/docker-entrypoint-initdb.d/init.sql mysql:8.0

# windows (command) - C:\path\to\worksapce 부분을 ddl 파일이 위치한 디렉토리로 변경
$ docker run --rm -p 3306:3306 -e MYSQL_ROOT_PASSWORD=root1234! -v C:\path\to\workspace\ddl.sql:/docker-entrypoint-initdb.d/init.sql mysql:8.0
```

### Kafka
```bash
docker run -p 9092:9092 apache/kafka:3.8.0
```

### Redis
```bash
docker run -p 6379:6379 redis:7.4.0
```

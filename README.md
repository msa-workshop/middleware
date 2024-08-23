# Infra 환경 설정

### MySQL
```bash
docker run --rm -p 3306:3306 \
  --name mysql-container \
  -e MYSQL_ROOT_PASSWORD=root1234! \
  -v ./ddl.sql:/docker-entrypoint-initdb.d/init.sql \
  mysql:8.0
```

### Kafka
```bash
docker run -p 9092:9092 apache/kafka:3.8.0
```

### Redis
```bash
docker run --name redis-container -p 6379:6379 redis:7.4.0
```
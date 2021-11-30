# Пример среды docker, в которой php может писать и читать из kafka.

## Требования

На вашей собственной машине вы должны иметь:

- docker
- docker-compose

## Запустите демонстрационную версию

```
docker-compose up -d
```

Отправьте свое сообщение в строке запроса, посетив `http://localhost?hello`.

```
docker-compose exec php php /usr/share/nginx/www/public/consumer_high.php
```

## Документация

- Docker images for [kafka](https://hub.docker.com/r/wurstmeister/kafka/) and [zookeeper](https://hub.docker.com/r/wurstmeister/zookeeper/)
- [librdkafka](https://github.com/edenhill/librdkafka), a C implementation of the kafka protocol
- [php-rdkafka](https://github.com/arnaud-lb/php-rdkafka), a kafka client for php

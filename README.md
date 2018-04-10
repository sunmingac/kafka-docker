docker-compose exec kafka-1 bash

kafka-topics --create --zookeeper zookeeper-1:2181 --replication-factor 3 --partitions 3 --topic demo

kafka-topics --zookeeper zookeeper-1:2181 --list

kafka-topics --zookeeper zookeeper-1:2181 --describe --topic demo





kafka-console-producer --broker-list kafka-1:9092 --topic demo

kafka-console-consumer --bootstrap-server kafka-1:9092 --from-beginning --topic demo

kafka-console-consumer --bootstrap-server kafka-1:9092 --from-beginning --group my-group --topic demo




kafka-consumer-groups --new-consumer --bootstrap-server kafka-1:9092 --list


kafka-consumer-groups --new-consumer --bootstrap-server kafka-1:9092 --describe --group my-group

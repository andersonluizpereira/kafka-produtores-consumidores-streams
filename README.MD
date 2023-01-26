**Suba o docker**
Na pasta raiz
`docker-compose up -d`

**Kafka -basics **
1-)Criando topico - Todas as mensagens aqui não ficam em ordem devido que ela vão para partições diferentes
`kafka-topics --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 3 --topic  ECOMMERCE_NEW_ORDER`

2-)Listar os tópicos
`kafka-topics --list --bootstrap-server localhost:9092`

Depois rode o "FraudDetectorService" no main mesmo raiz.
Depois rode o "NewOrderMain" no main mesmo raiz.
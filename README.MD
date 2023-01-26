**Suba o docker**
Na pasta raiz
`docker-compose up -d`

**Kafka -basics **
1-)Criando topico - Todas as mensagens aqui não ficam em ordem devido que ela vão para partições diferentes
`kafka-topics --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic  ECOMMERCE_NEW_ORDER`

2-)Listar os tópicos
`kafka-topics --list --bootstrap-server localhost:9092`

Nesse exercicío
Rode todos os programas
E utilize o comando

Serve para ver como o grupo está distruindo os dados nas particoes todos os grupos
`kafka-consumer-groups --bootstrap-server=localhost:9092  --describe --all-groups`

Aumente agora o numero de partiçoes para distribuir a carga
`kafka-topics --bootstrap-server localhost:9092 --alter --topic ECOMMERCE_NEW_ORDER --partitions 3`

Feche todos os progrmas e rode novamente
Espere fazer o rebalanceamento
Rode o comando do describe


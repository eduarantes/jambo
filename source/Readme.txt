

============

docker run --name some-mongo -d -p 27017:27017 mongo

docker stop some-mongo
docker rm some-mongo

docker start some-mongo


============

docker run -p 2181:2181 -p 9092:9092 --env ADVERTISED_HOST=10.0.75.1 --env ADVERTISED_PORT=9092 spotify/kafka

docker run -p 2181:2181 -p 9092:9092 \
    --env ADVERTISED_HOST=10.0.75.1 \
    --env ADVERTISED_PORT=9092 \
    --env CONSUMER_THREADS=1 \
    --env TOPICS=my-topic,some-other-topic \
    --env ZK_CONNECT=kafka7zookeeper:2181/root/path \
    --env GROUP_ID=mymirror \
    spotify/kafkaproxy


winpty docker run --rm -it -p 8000:8000 \
               -e "KAFKA_REST_PROXY_URL=http://localhost:2181" \
               -e "PROXY=true" \
               landoop/kafka-topics-ui


docker run --rm -p 2181:2181 -p 3030:3030 -p 8081-8083:8081-8083 \
           -p 9581-9585:9581-9585 -p 9092:9092 -e ADV_HOST=10.0.75.1 \
           landoop/fast-data-dev:latest

http://10.0.75.1:3030 


docker run --rm -p 2181:2181 -p 3030:3030 -p 8081-8083:8081-8083 \
           -p 9581-9585:9581-9585 -p 9092:9092 -e ADV_HOST=10.0.75.1 \
           landoop/fast-data-dev:latest




Demonstrating high cpu-usage in `KafkaStreamsMetrics` for micrometer 1.7.4

Needs kafka running on localhost:9092 (https://docs.confluent.io/platform/current/quickstart/ce-docker-quickstart.html)

Start application: `./mvnw spring-boot:run`

App should run using minimal cpu.

Call prometheus in loop: `./call_prometheus.sh`

This should increase the CPU usage significantly: `jconsole {pid}`

On micrometer 1.7.3 the CPU increase shouldn't be noticeable.
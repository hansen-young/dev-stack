# dev-stack
A simple repository consisting of stacks used across my other projects.


## How to Use

1. Create the `dev-network`. This will be the default communication channel across services unless specified otherwise.
   ```bash
   ./create_network.sh
   ```

2. Start service
   ```bash
   cd [service_name] && docker compose up
   ```


## Available Services

- **Port:** The port exposed internally by the container
- **Forward:** The port used in the host machine if forwarded


|     Service    | Port  | Forwarded |  Containers   |
|----------------|-------|-----------|---------------|
| Postgres       | 5432  |    5432   | `postgres`    |
| Kafka          | 9092  |     -     | `kafka`       |
| Kafka UI       | 8080  |    7500   | `kafka-ui`    |
| Redis          | 6379  |    6379   | `redis-1` `redis-2` |
| Redis Sentinel | 26379 |     -     | `redis-sentinel` |
| ScyllaDB       | 9042  |    9042   | `scylla_haproxy` `scylla1` `scylla2` |
|                |       |           |               |
|                |       |           |               |
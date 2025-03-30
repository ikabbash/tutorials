# Collecting Data from Azure Event Hub with Fluentd
This repo sets up Fluentd to consume data from Azure Event Hub using the Kafka Fluentd [plugin](https://github.com/fluent/fluent-plugin-kafka).

[![Hashnode](https://img.shields.io/badge/Read%20on-Hashnode-2962FF?style=flat&logo=hashnode)](https://ikabbash.hashnode.dev/configuring-fluentd-to-collect-data-from-azure-event-hub)
[![Medium](https://img.shields.io/badge/Read%20on-Medium-000000?style=flat&logo=medium)](https://medium.com/@ikabbash/configuring-fluentd-to-collect-data-from-azure-event-hub-ae2603602f03)
[![Dev.to](https://img.shields.io/badge/Read%20on-Dev.to-0A0A0A?style=flat&logo=devdotto)](https://dev.to/ikabbash/configuring-fluentd-to-collect-data-from-azure-event-hub-41g7)


## Setup Steps
1. Create an Azure Event Hub:
    - Create a namespace (Standard tier).
    - Create an Event Hub inside the namespace.
    - Add a **Shared Access Policy** with **listen** permissions.
    - Copy the **connection string**.

2. Clone & Configure
    ```
    git clone <repo-url>
    cd <repo-folder>
    ```

3. Update `fluentd.conf` with your Event Hub namespace, name, and connection string

4. Run Fluentd
    ```
    mkdir logs && sudo chown 999:999 logs
    docker compose up --build
    ```

# Data Platform

![GitHub Workflow Status (with event)](https://img.shields.io/github/actions/workflow/status/xuwenyihust/Data-Platform/ci-cd.yml)


## Overview
A big data platform for data processing and machine learning based on Kubernetes and Spark.

## Setup
### Prerequisites
- GCP account
- gcloud SDK
- kubectl
- helm
- docker
- python3

### Configuration
```bash
cp bin/env_template.yaml bin/env.yaml
```

Update the configuration in `bin/env.yaml` accordingly.

### Create a Kubernetes cluster on GCP
```bash
source bin/setup.sh
```

### Deploy Spark Application on Kubernetes
```bash
source bin/submit_spark_app.sh --image APP_IMAGE --name APP_NAME --main MAIN_CLASS --jar JAR_FILE --args APP_ARGS
```

## License
This project is licensed under the terms of the MIT license.

## Reference
- [Running Apache Spark on Kubernetes](https://medium.com/empathyco/running-apache-spark-on-kubernetes-2e64c73d0bb2)
- [spark-docker](https://github.com/apache/spark-docker)
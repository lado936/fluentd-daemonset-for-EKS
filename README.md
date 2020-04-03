# fluentd-daemonset-for-EKS
Stream EKS pod logs to AWS ElasticSearch Using fluentbit + firehose 

To stream EKS pod logs to AWS Elasticsearch service run:

    kubectl apply -f fluentd.yaml
    
This will create daemonset resource of fluentd with init container to copy fluentd configuration to its container, fluentd will stream logs to kinesis firehose and firehose from its side will then stream logs to Elasticsearch.

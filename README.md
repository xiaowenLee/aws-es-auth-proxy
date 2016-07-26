# aws-es-auth-proxy

## Objective

The objective is to create a proxy that permits to connect to the AWS 
managed Elasticsearch cluster protected with the AWS authentication 
accessing kibana and other stuffs without authentication.

## How to run the application

To lunch the application you have to set some parameter in the
command line. The only required parameter is `aws_service_endpoint` 
which require the AWS ElasticSearch endpoint.
The AWS credential is loaded automatically following the boto3 priority 
(http://boto3.readthedocs.io/en/latest/guide/configuration.html#configuring-credentials)

For example:

```
aws-es-auth-proxy --aws_service_endpoint search-mydomain-id.eu-west-1.es.amazonaws.com
```

For security purpose the service starts automatically listening
only in localhost on port 8080.


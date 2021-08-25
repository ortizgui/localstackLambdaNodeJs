## Creating SQS Queue
```
aws sqs create-queue --queue-name local-queue --endpoint-url http://localhost:4566 --region us-east-1
```

## Creating SNS Topic
```
aws sns create-topic --name local-topic --endpoint-url http://localhost:4566 --region us-east-1
```

## SNS Subscription
```
aws sns subscribe --notification-endpoint http://localhost:4566/000000000/local-queue --topic-arn arn:aws:sns:us-east-1:000000000000:local-topic --protocol sqs --endpoint-url=http://localhost:4566 --region us-east-1
```
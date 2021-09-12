**AWS default vpc remover** is designed to delete all your default vpcs. This is useful when you create the fresh AWS account and want to manage the vpc intentionally. To use the AWS default vpc remover, upload the `template.yaml` into the CloudFormation of your AWS account and invoke the lambda function by using the AWS CLI such as:

```bash
aws lambda invoke --function-name lambda-aws-default-vpc-remover result.txt
```

or create a test event from the lambda console and test it without any payload. The invocation will takes around 2 mins usually. The sample response is here:

```
START RequestId: fc722266-4dd9-4b98-8a8d-ba4388b79110 Version: $LATEST
ignore_regions :  ['None']
remove_regions :  ['eu-north-1', 'ap-south-1', 'eu-west-3', 'eu-west-2', 'eu-west-1', 'ap-northeast-3', 'ap-northeast-2', 'ap-northeast-1', 'sa-east-1', 'ca-central-1', 'ap-southeast-1', 'ap-southeast-2', 'eu-central-1', 'us-east-1', 'us-east-2', 'us-west-1', 'us-west-2']
eu-north-1           | vpc-01988a7c5a69841f8    |  deleted
ap-south-1           | vpc-05511c72e2ffcb87c    |  deleted
eu-west-3            | vpc-0e1f329abbe4fa223    |  deleted
eu-west-2            | vpc-006984b12904c3506    |  deleted
eu-west-1            | vpc-0b8a7c5b109d1ca4d    |  deleted
ap-northeast-3       | vpc-0ba819cb648b3c6ff    |  deleted
ap-northeast-2       | vpc-f2b35099             |  deleted
ap-northeast-1       | vpc-04d54b8b359099359    |  deleted
sa-east-1            | vpc-0c0c37bf6ab88b83d    |  deleted
ca-central-1         | vpc-0993d43d02d9d3a7f    |  deleted
ap-southeast-1       | vpc-069bc492bfc17c8d8    |  deleted
ap-southeast-2       | vpc-0787fb9fdec3b8bd3    |  deleted
eu-central-1         | vpc-0d6969012d833113b    |  deleted
us-east-1            | vpc-052cb5d2bfc5e5598    |  deleted
us-east-2            | vpc-300b0858             |  deleted
us-west-1            | vpc-0075c027846049805    |  deleted
us-west-2            | vpc-0b929a73             |  deleted
END RequestId: fc722266-4dd9-4b98-8a8d-ba4388b79110
REPORT RequestId: fc722266-4dd9-4b98-8a8d-ba4388b79110	Duration: 104447.43 ms	Billed Duration: 104448 ms	Memory Size: 128 MB	Max Memory Used: 128 MB	Init Duration: 246.54 ms
```
# ml-cfn

This CloudFormation template will create the following AWS resource for a generic Machine Learning project:
- iam
- s3
- ec2
- ecr

```bash
aws cloudformation create-stack \
    --stack-name ml-project-stack \
    --template-body file://cfn.yaml \
    --capabilities CAPABILITY_NAMED_IAM \
    --parameters ParameterKey=Password,ParameterValue=$(openssl rand -base64 15)
```

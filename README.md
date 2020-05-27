# aws-csgo

Counter Strike Global Offensive setup on AWS

```bash
aws cloudformation create-stack \
    --stack-name csgo \
    --template-body file://./cf.yml \
    --capabilities CAPABILITY_NAMED_IAM \
    --region eu-west-3 \
    --parameters ParameterKey=KeyName,ParameterValue=csgo \
        ParameterKey=VpcId,ParameterValue=vpc-f727d89e \
        ParameterKey=SubnetId,ParameterValue=subnet-3784984f \
        ParameterKey=ApiAuthorizationKey,ParameterValue=xxxx \
    --profile privacy-dev 
```

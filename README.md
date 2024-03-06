# `tf-parameter-store`

TF Managed [AWS SSM Parameter Store](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html)

## Backend setup

This project uses [S3 Terraform backend](https://developer.hashicorp.com/terraform/language/settings/backends/s3) - partially configured from modules.

Full configuration makes use of environment variables

```sh
# Env variables
TF_BACKEND_BUCKET="name-of-my-tf-s3-bucket"
TF_BACKEND_REGION="us-west-1"
TF_BACKEND_DYNAMODB_TABLE="name-of-dynamodb-table-for-state-locks"
```

### init

```sh
make tf-init
```

### plan

```sh
make tf-plan
```

### apply

```sh
make tf-apply
```

# 🪣 Deploy a Public Read S3 Bucket Using CloudFormation

In this example, I create a simple **CloudFormation template** that **deploys a public read S3 bucket**.

## 📁 File Structure

```text
.
├── README.md       
└── bucket.yml  # CloudFormation template
```

## 🔭 Operations

### Deploy Stack

```shell
aws cloudformation deploy --template-file ./bucket.YAML --stack-name demo-public-s3-bucket
```

### Update Stack
```shell
aws cloudformation update-stack --template-body file://./bucket.YAML --stack-name demo-public-s3-bucket
```

### Delete Stack

#### 1. Delete all the objects in the bucket

```shell
aws s3 rm s3://demo-public-s3-bucket --recursive
```

#### 2. Delete the stack

```shell
aws cloudformation delete-stack --stack-name demo-public-s3-bucket
```

## ✨ Result

Now everyone can see the file in this S3 bucket.
<img src="https://image-hosting-bucket.s3.us-west-2.amazonaws.com/images/ScreenShot 2022-11-28 at 11.02.06@2x.png" alt="ScreenShot2022-11-28at11.02.06@2x" width="500px"/>


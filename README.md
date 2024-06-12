# Prepare your S3 Bucket in AWS Playground

## 1. Deploying S3 bucket and static site hosting

- open main.tf and replace your_name with your actual name
- copy paste aws playgroud access keys in terminal
- run `terraform init`
- run `terraform plan`
- run `terraform apply -auto-approve`
- will get strange 403 error of aws_s3_bucket_policy (probably playground account is setup with specific permission? 🤔)
- run `terraform apply -auto-approve` again
- go to [AWS Playground - SRE 1](https://traderepublic.awsapps.com/start/#/?tab=accounts) > Type 'S3' in searchbar > filter by gha-{your_name}
- confirm new S3 bucket with your name exists in AWS
- confirm that static site hosting is enabled, public access is turned on and bucket policy is attached

## 2. Destroy all the resources we deployed

run `terraform destroy -auto-approve`

## Recommended IDE Setup

- [Github Actions](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-github-actions)
- [Terraform](https://marketplace.visualstudio.com/items?itemName=HashiCorp.terraform)

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Type-Check, Compile and Minify for Production

```sh
npm run build
```

### Test

```sh
npm run test
```

### Lint

```sh
npm run lint
```

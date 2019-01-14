# [AWS Amplify Setup](https://aws-amplify.github.io/docs/js/start?ref=amplify-js-btn&platform=purejs)

## AWS Amplify Backend

Deployment Bucket created - `a29degreesapp-xxxxx-deployment`

✔ Successfully created initial AWS cloud resources for deployments.

Your project has been successfully initialized and connected to the cloud!

### Some next steps:

`amplify status`

will show you what you've added already and if it's locally configured or deployed

`amplify <category> add`

will allow you to add features like user login or a backend API

`amplify push`

will build all your local backend resources and provision it in the cloud

`amplify publish`

will build all your local backend and frontend resources (if you have hosting category added) and provision it in the cloud

### Pro tip:

Try `amplify add api` to create a backend API and then `amplify publish` to deploy everything

### `Add Analytics`

```
$ amplify add analytics

? Apps need authorization to send analytics events. Do you want to allow guests and unauthenticated users to send analytics events? (we recommend you allow this when getting started) Yes
```

[Pinpoint Dashboard](https://console.aws.amazon.com/pinpoint/home) - 29degreesapp Analytics

### `Add Hosting`

```
$ amplify add hosting

? Select the environment setup:
  DEV (S3 only with HTTP)
❯ PROD (S3 with CloudFront using HTTPS)
```

```
? Select the environment setup: PROD (S3 with CloudFront using HTTPS)
? hosting bucket name 29degreesapp-xxxxx-hostingbucket
? index doc for the website index.html
? error doc for the website error.html
```

### `Publish`

```
$ amplify publish

| Category  | Resource name   | Operation | Provider plugin   |
| --------- | --------------- | --------- | ----------------- |
| Hosting   | S3AndCloudFront | Create    | awscloudformation |
| Auth      | xxxxx           | No Change | awscloudformation |
| Analytics | 29degreesapp    | No Change | awscloudformation |
? Are you sure you want to continue? Yes
```

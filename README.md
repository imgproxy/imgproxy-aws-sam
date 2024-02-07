<p align="center">
  <a href="https://imgproxy.net">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="assets/logo-dark.svg?sanitize=true">
      <source media="(prefers-color-scheme: light)" srcset="assets/logo-light.svg?sanitize=true">
      <img alt="imgproxy logo" src="assets/logo-light.svg?sanitize=true">
    </picture>
  </a>
</p>

<h4 align="center">
  <a href="https://imgproxy.net">Website</a> |
  <a href="https://imgproxy.net/blog/">Blog</a> |
  <a href="https://docs.imgproxy.net">Documentation</a> |
  <a href="https://imgproxy.net/#pro">imgproxy Pro</a> |
  <a href="https://hub.docker.com/r/darthsim/imgproxy/">Docker</a> |
  <a href="https://twitter.com/imgproxy_net">Twitter</a> |
  <a href="https://discord.gg/5GgpXgtC9u">Discord</a>
</h4>

<p align="center">
<a href="https://github.com/imgproxy/imgproxy-aws-sam/actions"><img alt="GH Lint" src="https://img.shields.io/github/actions/workflow/status/imgproxy/imgproxy-aws-sam/lint-and-upload.yml?branch=master&label=Lint&style=for-the-badge" /></a>
</p>

---

[imgproxy](https://imgproxy.net) is a fast and secure standalone server for resizing and converting remote images. The main principles of imgproxy are simplicity, speed, and security.

This repository contains an [AWS Serverless Application Model (SAM)](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/what-is-sam.html) template compatible with [AWS CloudFormation](https://aws.amazon.com/cloudformation/) that allows you to deploy imgproxy to AWS Lambda.

## Using the template

We uploaded the template to our S3 bucket so you can use by a click of a button. The links below will take you to the AWS CloudFormation console with the template pre-filled. You just need to provide the required parameters and click **Create stack**.

[![](assets/launch-stack.svg)](https://console.aws.amazon.com/cloudformation/home#/stacks/new?stackName=imgproxy&templateURL=https://imgproxy-cf.s3.amazonaws.com/sam/latest/template.yml)

> [!NOTE]
> The link in the README points to the template from the `master` branch. If you want to use a specific version, you can find the links in the [releases](https://github.com/imgproxy/imgproxy-aws-sam/releases) section.

> [!WARNING]
> Official Docker images of imgproxy prior to version `3.22.0` do not contain [AWS Lambda adapter](https://github.com/awslabs/aws-lambda-web-adapter).
>
> If you want to use the template with an older version of imgproxy, you need to build a custom Docker image with the adapter. Take note that this template assumes that the AWS Lambda adapter is configed to work in the `rsponse_stream` mode.

## License

imgproxy-aws-sam is licensed under the MIT license.

See [LICENSE](https://github.com/imgproxy/imgproxy-aws-sam/blob/master/LICENSE) for the full license text.

## Security Contact

To report a security vulnerability, please contact us at security@imgproxy.net. We will coordinate the fix and disclosure.


# References

## Project ideas

- [SAM hello-world : API GW-Lambda](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-getting-started-hello-world.html)
  - AWS SAM CLI natively supports AWS CDK. AWS SAM CLI can be used to develop and test locally serverless applications within an AWS CDK project. That is the AWS SAM CLI not just for AWS SAM; instead, AWS SAM and AWS CDK can work together.
  - Implemented in ~/projects/sam-demo
- 
## Tools/technologies/libraries/frameworks/tutorials

- 

## Issues

## Analysis

- SAM is definitely easier than cloudformation. You can almost always SAM directly and within it use cloudformation where SAM doesn’t have a simplified version of a resource definition.
- SAM has features to test lambda locally and also access logs quickly. And includes support for lambda events(inputs) and ability to specify a different set of environment variables for lambda in local invocation. More here : https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-getting-started-hello-world.html
- SAM is similar in many ways to serverless framework, more here : https://dev.to/tastefulelk/serverless-framework-vs-sam-vs-aws-cdk-1g9g
- SAM can work with CDK. At illustrated in this tutorial : https://aws.amazon.com/blogs/compute/better-together-aws-sam-and-aws-cdk/
- In fact CDK and SAM are somewhat complementary. CDK can help code/define and deploy infrastructure while SAM can help test and debug it quickly.

# References

## Project ideas

- [SAM hello-world : API GW-Lambda](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-getting-started-hello-world.html)
  - AWS SAM CLI supports AWS CDK. 
  - AWS SAM CLI can be used to develop and test locally serverless applications within an AWS CDK project. 
  - i.e. the AWS SAM CLI not just for AWS SAM; instead, AWS SAM and AWS CDK can work together.
  - **Notes for me** :Implemented in ~/projects/sam-demo
- 
## Tools/technologies/libraries/frameworks/tutorials

- 

## Issues

## Analysis

- SAM is definitely easier than cloudformation. You can almost always SAM directly and within it use cloudformation where SAM doesn’t have a simplified version of a resource definition.
- SAM has features to test lambda locally and also access logs quickly. And includes support for lambda events(inputs) and ability to specify a different set of environment variables for lambda in local invocation. More here : https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-getting-started-hello-world.html
- SAM is similar in many ways to serverless framework, more here : https://dev.to/tastefulelk/serverless-framework-vs-sam-vs-aws-cdk-1g9g
- SAM can work with CDK. As illustrated in this tutorial : https://aws.amazon.com/blogs/compute/better-together-aws-sam-and-aws-cdk/. Another article on this topic is here : https://dev.to/aws-builders/build-serverless-applications-using-cdk-and-sam-4oig. And a bit more content here : https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-cdk-getting-started.html 
- In fact CDK and SAM are somewhat complementary. CDK can help code/define and deploy infrastructure while SAM can help test and debug it quickly.
  - If CDK is used then it seems that SAM templates are not going to be used while SAM CLI may still be used.
  - i.e. The integration is skin deep and SAM and CDK need to have their own responsibilities that are distinct.

Amongst the 3
- For brevity and readability, CDK seems to be the most apt, next SAM and then cloudformation (discarding) CLI commands  and AWS console.
- For ease of use SAM seems to be the most apt followed CDK and then cloudformation.
- For quick testing and debugging SAM is the only option (other than CLI or AWS console.)
- While it is feasible to embed GraphQL schema into cloudformation (and therefore into SAM template) and also use existing cloudformation templates in CDK ex: https://docs.aws.amazon.com/cdk/api/v1/docs/cloudformation-include-readme.html, It is not feasible to embed CDK code into cloudformation template i.e. in some ways CDK supersedes and deprecates cloudformation templates and makes SAM templates redundant. 
- Also, CDK internally generates cloudformation templates, so in terms of capabilities/express-ability all 3 are equal today while cloudformation seems to be the internal gold standard to which everything is converted.
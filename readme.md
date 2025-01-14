# Amazon Connect Campground for Service Cloud Voice

This repository contains resources, examples, and projects to help Service Cloud Voice customers address some common requirements as they deploy Service Cloud Voice. While the solutions here are designed specifically for Service Cloud Voice deployments they will all work for standard Amazon Connect + CTI examples as well and can also serve as a reference for non-Salesforce deployments. 

The repository is divided into three core sections:
- Common Resources: Provide underlying resources required for some of the solutions to work. Examples include a common authentication setup for these solutions, AWS Lambda depenedency layers, etc
- Solutions: larger solutions designed to address specific requirements that customers may have. Examples include cross-account Lambda access or Voicemail for Amazon Connect
- Use Case Examples: small, simple examples to address basic configuration questions. Examples inclde dial-by-extension configurations and follow-me routing.
- AWS Best Practices for Service Cloud Voice: documents written by AWS solutions architects that demonstrate best practice design for specific Service Cloud Voice use cases.

## Common Resources

| Name | Description | Links |
| ---- | ----------- | ----- |
| AWSSCV-CommonLayers | Lambda layers to provides dependencies, code, and functions for nodejs and python Lambda functions that augment the Service Cloud Voice offering from Salesforce | [Common](Common/AWSSCV-CommonLayers) |
| AWSSCV-SalesforceConfig | Directions and utilities to help create certificates, a connected app, login credentials, and gathers org information. This  will be used my multiple solutions in this repository. | [Common](Common/AWSSCV-SalesforceConfig) |

## Solutions

| Name | Description | Links |
| ---- | ----------- | ----- |
| AWSSCV-Voicemail Express | Provides a basic voicemail capability to Amazon Connect in Salesforce configurations. Designed specifically to function in the AWS Accounts created for Service Cloud Voice | [Solution](Solutions/AWSSCV-VoicemailExpress) |
| AWSSCV-CTRLogger | Configures a Lambda function to log Amazon Connect contact trace records to CloudWatch, S3, or both | [Solution](Solutions/AWSSCV-CTRLogger) |
| AWSSCV-AgentEventLogger | Configures a Lambda function to log agent event records to CloudWatch | [Solution](Solutions/AWSSCV-AgentEventLogger)
| AWSSCV-DashboardAlarms | Configures a dashboard and set of Cloudwatch alarms allowing administrators to receive notifications for various Amazon Connect metrics. | [Solution](Solutions/AWSSCV-DashboardAlarms) |

## Use Case Examples

| Name | Description | Links |
| ---- | ----------- | ----- |
| AWSSCV-CrossAccountSMS | Uses Lambda and cross account permissions to allow Salesforce Service Cloud Voice provisioned Amazon Connect instances to utilize SNS to send SMS messages. | [Example](Examples/AWSSCV-CrossAccountSMS) |
| AWSSCV-ExtensionRouter | Configures a Dial-by-extension option for Amazon Connect. | [Example](Examples/AWSSCV-ExtensionRouting) |
| AWSSCV-FollowMeRouting | Configures an option to route calls to an agent's mobile when they are not logged in, if configured. | [Example](Examples/AWSSCV-FollowMeRouting) |
| AWSSCV-DDR-Flow | Demonstrates how data from Salesforce can be used to influence routing in Amazon Connect. Uses a flow in Salesforce to return routing destinations | [Example](Examples/AWSSCV-DataDirectedRouting-FlowRouting) |
| AWSSCV-WarmingFunctions |  Demonstrates how to use Amazon EventBridge to keep AWS Lambda functions warm. | [Example](Examples/AWSSCV-WarmingFunctions) |

## AWS Best Practices for Service Cloud Voice
| Name | Description | Links |
| ---- | ----------- | ----- |
Overflow Routing|Describes best practices for dealing with spikes in call volumes. Specifically describes overflow routing scenarios to keep data clean and reduce administrative overhead.|[Document](BestPractices/OverflowRouting.md)|

## Stacks

| Name | Description | Links |
| ---- | ----------- | ----- |
| AWSSCV-LaunchPack | A single CloudFormation stack, including nested stacks, providing a combination of solutions and examples including: Voicemail Express, CTR Logger, Dashboard Alarms, and Sample Contact Flows. | [Stacks](Stacks/AWSSCV-LaunchPack) |


## Contributions

Make sure the `.gitignore` per language is applied. 

## Status
![Status](https://codebuild.us-west-2.amazonaws.com/badges?uuid=eyJlbmNyeXB0ZWREYXRhIjoiVlBLcm9mQlRQV01ZbDRES1FwM3JRNVlJYzB0MlNYYzN1V25weU9CSUN1ckxHQWFTbitsRFo2RHUzR3FDblJjZjR5ZnJhY2F6VHBYSEtVaXcwcVNKVXM0PSIsIml2UGFyYW1ldGVyU3BlYyI6IklPR2ExNWp1MnN6T1pYZ3MiLCJtYXRlcmlhbFNldFNlcmlhbCI6MX0%3D&branch=master)


# Taskmaster as a Lambda Function

## Overview
This is the serverless version of [Taskmaster](https://github.com/hotandfresh/taskmaster).  In this version, adding a new task and updating the status of a task have now been made into a lambda function.

A trigger has been placed on the dynamoDB that will fire every time an interaction happens with the table.

## How to run this application
Since this is still connected to a hosted [frontend](https://github.com/hotandfresh/taskmaster-frontend), this application can be visited at this [site](http://alltasks.s3-website-us-west-2.amazonaws.com).

This cannot be run locally because an AWS account is needed because lambda functions, an elastic beanstalk, and an ec2 instance are all needed to get this working.

## Issues
The biggest hurdle was how to get the id for a task. However, the ```.load``` method on a DynamoDBMapper was able to get it.  The documentation was found [here](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DynamoDBMapper.Methods.html#DynamoDBMapper.Methods.load).


## Acknowledgements

Many thanks to:  

- Matt Stuhring
- Nhu Trinh
- Travis Cox
- Peter Lee
- Padmapriya Ganapathi
- Renee Messick
- Jack Kinne
# ec2-meta-env

VERY WIP :)

## Rationale

AWS ECS container may need, at runtime, information held by in the [EC2 istance metadata](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-metadata.html).
Although you can set environment variables in your EC2 istance UserData, those will not be injected in the ECS container runtime.

This simple CLI tool, which is supposed to be run in your docker entrypoint, will expose configured information via environment variables, so that your application will be totally ignorant and will not need to do any HTTP call.

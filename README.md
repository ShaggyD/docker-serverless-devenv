
#Alpine-linux based Serverless Development Environment#

This container is inteneded to provide a ready to run, lightweight Node and Serverless development environment for working with AWS Lambda. 

* Serverless Project: https://serverless.com/
* AWS Lambda: https://aws.amazon.com/lambda/

The container requires two host volume mappings: One for your AWS keys (only necessary if you're deploying to AWS), and the other for your projects / code etc.

```docker run -w /home/projects --name serverless -t -i -v /your/host/project/folder:/home/projects -v /your/aws-credentials/.aws/credentials:/root/.aws/credentials serverless-devenv /bin/sh```

Type ```serverless``` at the command prompt to list the available options.

Once you've exited the container, you can re-enter using:

```docker start serverless -i```

Or if you want the container to disappear on exit, simply append ```--rm``` to your run command.

[![](https://images.microbadger.com/badges/image/marklkelly/alpine-serverless-devenv.svg)](https://microbadger.com/images/marklkelly/alpine-serverless-devenv
"Get your own image badge on microbadger.com")

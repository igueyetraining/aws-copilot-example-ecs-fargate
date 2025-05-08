Steps to deploy an App using copilot once the manifest.yml are already created
################################################################################

# 1. Deloy All in 2 commands.
#1.1 Create the copilot Application
copilot app init my-multi-ecs-fargate-svc-app

#1.1 Create the copilot Environment, All Services
copilot deploy --all --init-env --init-wkld --deploy-env --profile default -e test 

################################################################################
# Using step by step
# 1. Define the environment (you've already done this)
$ copilot env init --name test --profile default --default-config

# 2. Provision/Update the environment infrastructure
$ copilot env deploy --name test

# 3. Deploy all services in your workspace to the 'test' environment
$ copilot deploy --env test
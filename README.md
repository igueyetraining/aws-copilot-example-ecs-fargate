Steps to deploy an App using copilot once the manifest.yml are already created
################################################################################

# 1. All in One
$ copilot deploy --all --init-wkld --deploy-env -e prod

################################################################################
# Using step by step
# 1. Define the environment (you've already done this)
$ copilot env init --name test --profile default --default-config

# 2. Provision/Update the environment infrastructure
$ copilot env deploy --name test

# 3. Deploy all services in your workspace to the 'test' environment
$ copilot deploy --env test
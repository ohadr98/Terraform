# Terraform
In this project we were asked to create 2 environment - staging/production

## Requirements and Installations:
- [Node.js](https://nodejs.org/) 12.x or higher

- [Free Okta developer account](https://developer.okta.com/) for account
  registration, login

- Download Terraform from [terraform.io](https://www.terraform.io/downloads.html)

- Download and install [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli)

- Type `az login` and login to Azure

## Configuration:
- Use `azurerm` as a [provider](https://www.terraform.io/docs/language/providers/configuration.html)

- Create `terrafom.tfvars.json` file for your secret variables (for each environment - staging/production)


## Basic commands: 
- `terraform` - make sure terraform CLI is installed
- `terraform init` - initialize terraform Azure modules
- `terraform fmt` - automatically updates configurations in the current directory for readability and consistency
- `terraform validate` - make sure your configuration is syntactically valid and internally consistent
- `terraform apply` or `terraform apply main.tfplan` - command to apply the infrastructure changes
- `terraform destroy` - remove the infrastructure
- now you will see in your azure portal your resource group with all the resources that your created.
- after you did it you can install the  Weight Tracker application in your VM'S.

## Cleanup commands
- `rm terraform.tfstate`
- `rm terraform.tfstate.backup`
- `rm tfplan`
- `rm tfplan.json`
- `rm -r .terraform/`

# Node.js Weight Tracker:

![build-weight-tracker-app-demo](https://user-images.githubusercontent.com/83014719/137505630-ccf4c3f4-6e06-4778-b414-830d6bb23f99.gif)
This sample application demonstrates the following technologies.
- [hapi](https://hapi.dev) - a wonderful Node.js application framework
- [PostgreSQL](https://www.postgresql.org/) - a popular relational database
- [Postgres](https://github.com/porsager/postgres) - a new PostgreSQL client for Node.js
- [Vue.js](https://vuejs.org/) - a popular front-end library
- [Bulma](https://bulma.io/) - a great CSS framework based on Flexbox
- [EJS](https://ejs.co/) - a great template library for server-side HTML templates

## Install and Configuration
1. Clone or download source files
1. Run `npm install` to install dependencies
1. If you don't already have PostgreSQL, set up using Docker
1. Create a [free Okta developer account](https://developer.okta.com/) and add a web application for this app
1. Copy `.env.sample` to `.env` and change the `OKTA_*` values to your application
1. Initialize the PostgreSQL database by running `npm run initdb`
1. Run `npm run dev` to start Node.js

# @dev-thought/ng-deploy-universal

[![npm version](https://badge.fury.io/js/%40dev-thought%2Fng-deploy-universal.svg)](https://www.npmjs.com/package/@dev-thought/ng-deploy-universal)
[![The MIT License](https://img.shields.io/badge/license-MIT-orange.svg?color=blue&style=flat-square)](http://opensource.org/licenses/MIT)

**Deploy applications in nx / angular workspaces to the cloud using a provider of your Choice (Azure, AWS, Google Cloud Platform)**

We are using under the hood the code as infrastructure tool [Pulumi](https://www.pulumi.com/). It gives you the possibility to have every piece of code under your control. You can extend it for your requirements (VPN, ...) and still able to use the schematics for deployment.

## Quick-start <a name="quickstart"></a>

1. Create a new project with the angular cli (>= 8.3.0) or nx cli.

   ```sh
   npm install -g @angular/cli
   ng new hello-world --defaults
   cd hello-world
   ```

1. Add `ng-deploy-universal` to your project.

   ```sh
   ng add @dev-thought/ng-deploy-universal
   ```

1. Initialize the infrastructure as code for your project.

   ```sh
   ng g @dev-thought/ng-deploy-universal:init
   ```

1. You may be prompted you to anwser some questions for the setup.

1. Deploy your project to Azure.

   ```sh
   ng run hello-world:deploy
   ```

   The project will be built with the development configuration.
   In development you will be asked to confirm the changes of your infrastructure

## Feature set:

| Application | Features                          | Azure   | AWS     | Google Cloud Platform |
| ----------- | --------------------------------- | ------- | ------- | --------------------- |
| Angular     | static hosting, cdn | x       | x       | not yet               |
| NestJS      | serverless, server instance       | not yet | not yet | not yet               |
|             |                                   |         |         |                       |

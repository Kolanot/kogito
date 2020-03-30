# Kogito - Coffee Shop 

This repository showcases some of the key capabilities of Kogito specifically on how it:

1. Provides runtime persistence for workflows to preserve the state of the process instances across restarts. 
2. Supports first class citizen support for events and enables integration with third party systems with both events and external REST API calls. 
3. Enables the tracking of the process instances progress from the Kogito process management console. 

## Pre-requisites

To start with, ensure that the following are installed in your machine.

-   [OpenJDK 8+](https://computingforgeeks.com/how-to-install-java-11-openjdk-11-on-rhel-8)
-   [VSCode 1.41.1](https://code.visualstudio.com/docs/setup/linux)
-   [Kogito VSCode extension (latest)](https://github.com/kiegroup/kogito-tooling/releases)
-   [Red Hat Java VSCode extension (latest)](https://marketplace.visualstudio.com/items?itemName=redhat.java)
-   [Maven 3.6.0+](https://maven.apache.org/install.html)
-   [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
-   [Docker Engine (atleast 1.13) and Docker Compose (atleast 1.25)](https://download.docker.com/)

## Getting Started

Once done, clone this repo:

`git clone  [https://github.com/bbalakriz/kogito](https://github.com/bbalakriz/kogito)`

Move to the apps folder.

`cd apps/coffee-shop`

The drink-order-process.bpmn2 located at coffee-shop/src/main/resources/org/bala/drink/process can be opened by using either the [online BPMN editor](https://kiegroup.github.io/kogito-online/#/) - (by dragging and dropping the bpmn file) or do the following to open up the coffee-shop project in VSCode. 

1. First, install the Kogito Extension in VSCode.
2. Download the latest Visual Studio plugin from the project page: https://github.com/kiegroup/kogito-tooling/releases
3. Select the latest version
4. From asset section download the file vscode_extension_kogito_kie_editors_n.n.n.vsix
5. Open Visual Studio Code
6. Select the Extensions pane on the left
7. Click the... icon on the top right
8. Select Install from VSIX...
9. In a command line, do `code coffee-shop`

This process depicts the typical drink ordering steps at a coffee shop where a customer would walk in, place an order at the counter desk and then make payment at the payment desk either by cash or by a credit card - and when it is a credit card payment, the payment processing would be handled by an external payment gateway. Once the payment is successful, the barista would be notified to get started with the preparation of the required coffee. 

In here, the barista process has been designed to run as a seperate Kogito application and would be reacting to the coffee drink order taking process. Take a look at the barista process, it is a very simple one that shows that the barista would prepare the coffee and the customer would collect it once it is ready..

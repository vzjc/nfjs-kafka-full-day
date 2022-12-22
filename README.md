# nfjs-kafka-full-day

## Getting your Development Environment
* Fork nfjs-kafka-full-day repository from https://github.com/dhinojosa/nfjs-kafka-full-day

* Using your new URL, in the address bar of your browser, insert `gitpod.io/` before `github.com`, for example, convert `https://github.com/<username>/nfjs-kafka-full-day` to `https://gitipod.io/github.com/<username>/nfjs-kafka-full-day`

* This will take you to gitpod, a free virtual development environment (or least until the 50 hour limit per month is up)

* Select Github, as the OAuth Provider so you can authenticate

* It will ask what IDE you would like to use, please select Visual Studio Code Web Browser (not Desktop!)

* When "Extension Pack for Java' extension is recommended for this repository. Do you want to install?", please do.

* When "Would you like to install and synchronize 'Extension Pack for Java' extension across your devices?" is prompted, please do.

* When "Cannot activate the 'Test Runner for Java' extension because it depends on the 'Language Support for Java™ by Red Hat' extension, which is not installed. Would you like to install the extension and reload the window? Click Install and Reload", please do so

* Click on the extensions icon on the left, and install the "Docker" extension

* When the environment is ready, right-click on the docker-compose.yml and select "Compose Up"
  - We selected 4 minimal required services:
    * zookeeper
    * broker
    * control-center
    * web

## Open Lab Book
* Click `Ports` in VS Code
* Click lock icon (to make it unlocked) for the 8000 port
* Click the web icon to open a browser tab with the "Kafka Lab Book"

## Lab: Writing a Producer
* Run the following command with Maven: `mvn clean compile` to ensure that dependencies are downloaded

* Create a topic called `my_orders` in Apache Kafka, with a replication factor of 1 and 3 partitions
  - Open control center
    * Click 'Ports' in VS Code
    * Click lock icon (to make it unlocked) for the 9021 port
    * Click the web icon to open a browser tab with the "Control Center"
  - Click "Topics"
  - Click "+ Add topic" button (top right)
  - Change "Topic Name" to 'my_orders'
  - Change "Number of partitions" to '3'.
  - Ensure default properties (listed on the right) match desired replication and partition
  - Click "Create with defaults" button
  

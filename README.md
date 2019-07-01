Ferret [![Build Status](https://travis-ci.org/WASdev/sample.ferret.svg?branch=master)](https://travis-ci.org/WASdev/sample.ferret)
======

This sample project contains a simple Servlet application called Ferret. Ferret listens for HTTP requests sent to `<host>:<port>/ferret[/*]`, and responds with information about the request and the server. This is a simplified fork of [https://github.com/WASdev/sample.ferret](https://github.com/WASdev/sample.ferret) to test S2I deployments. It differs from the orgignal as follows:

1. Maven only build that creates a **.war** file but does not use the Liberty Maven plugin to create a Liberty server instance
2. Copied *server.xml* to the newly created folder **wlp/config** to accommodate multi-module apps.

## Running in Eclipse

### Maven
1. Download and install [Eclipse with the WebSphere Developer Tools](https://developer.ibm.com/wasdev/downloads/liberty-profile-using-eclipse/).
2. Create a new Liberty Profile Server. See [step 3](https://developer.ibm.com/wasdev/downloads/liberty-profile-using-eclipse/) for details.
3. Clone this repository.
4. Import the sample into Eclipse using *File -> Import -> Maven -> Existing Maven Projects* option.
5. Deploy the sample into Liberty server. Right click on the *ferret* sample and select *Run As -> Run on Server* option. Find and select a  Liberty profile server and press *Finish*.
6. Go to: [http://localhost:9080/ferret][]


## Running in the Command Line

### Maven cmd-line
This project can be built with [Apache Maven](http://maven.apache.org/).

Use the following steps to build the application with Maven:

1. Execute the full Maven build. The Liberty Maven Plug-in will download and install the Liberty server.
    ```bash
    $ mvn clean package
    ```

2. Deploy the generated **.war** file and **server.xml** to a Liberty server instance


Once the app is running, the application will be available under [http://localhost:9080/ferret][].


# Notice

© Copyright IBM Corporation 2014, 2017.

# License

```text
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
````

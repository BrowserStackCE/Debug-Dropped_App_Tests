# Debug-Queued_Tests

This repository demonstrates how to debug why tests queue in App Automate for internal debug certification.

![BrowserStack Logo](https://d98b8t1nnulk5.cloudfront.net/production/images/layout/logo-header.png?1469004780)

## Setup

### Requirements

1. Java 8+

    - If Java is not installed, follow these instructions:
        - For Windows, download latest java version from [here](https://java.com/en/download/) and run the installer executable
        - For Mac and Linux, run `java -version` to see what java version is pre-installed. If you want a different version download from [here](https://java.com/en/download/)

2. Maven
   - If Maven is not downloaded, download it from [here](https://maven.apache.org/download.cgi)
   - For installation, follow the instructions [here](https://maven.apache.org/install.html)

### Install the dependencies

To install the dependencies for Android tests, run :
```sh
cd android/testng-examples
mvn clean
```

Or,

To install the dependencies for iOS tests, run :

```sh
cd ios/testng-examples
mvn clean
```

## Getting Started

You first need to upload your app to BrowserStack servers.  Please use the public app: 

curl -u "USERNAME:ACCESS_KEY" \
-X POST "https://api-cloud.browserstack.com/app-automate/upload" \
-F "url=https://www.browserstack.com/app-automate/sample-apps/android/WikipediaSample.apk"



### Use parallel testing for this example :**

Android is the prefered device for this test, but you can obtain a sample .IPA file as well and test on iOS.

- Navigate to Debug-Dropped_App_Tests/android/testng-examples/src/test/resources/com/browserstack/run_parallel_test and edit the paralle config file to add in your credentials and App id.
- Switch to [Android examples](android/testng-examples/) and run the parallel test : mvn test -P parallel 

- Follow the steps outlined in the documentation - [Get Started with parallel testing on App Automate](https://www.browserstack.com/docs/app-automate/appium/getting-started/java/testng/parallelize-tests)


## Getting Help

This repository is designed for internal debug certification.

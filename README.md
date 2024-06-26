# day4-jenkinsproj
# My Project

## Overview
This project demonstrates a basic Java application with CI/CD integration using Jenkins.

## Jenkins Setup
Follow these steps to set up Jenkins for this project:

1. **Install Jenkins**:
   - Download and install Jenkins from [official website](https://www.jenkins.io/download/).
   - Follow the installation instructions for your operating system.

2. **Configure Jenkins**:
   - Open Jenkins in your browser: `http://localhost:8080`.
   - Install the recommended plugins.
   - Create a new Pipeline job and configure it with the provided Jenkinsfile.

3. **Pipeline Configuration**:
   - Ensure you have the following in your Jenkinsfile:
     ```groovy
     pipeline {
         agent any

         stages {
             stage('Build') {
                 steps {
                     bat 'mvn clean package'
                 }
             }
             stage('Test') {
                 steps {
                     bat 'mvn test'
                 }
             }
             stage('Deploy') {
                 steps {
                     echo 'Deploying...'
                 }
             }
         }
     }
     ```

## Build Instructions
To build the project manually:
1. Open a terminal.
2. Navigate to the project directory.
3. Run `mvn clean compile`.

## Usage Instructions
To run the application:
1. Navigate to the target directory.
2. Run the jar file using `java -jar target/myapp-1.0-SNAPSHOT.jar`.

## Troubleshooting Tips
- Ensure Java JDK 17 or higher is installed.
- Make sure environment variables are correctly set.
- If Jenkins fails to start, check the logs for detailed error messages.


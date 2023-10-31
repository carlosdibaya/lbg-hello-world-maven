pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M3"
    }

    stages {
        stage('Checkout') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'main', url: 'https://github.com/carlosdibaya/lbg-hello-world-maven.git'

                // Run Maven on a Unix agent.
                sh "mvn -Dmaven.test.failure.ignore=true clean package"

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }
        }
        stage('Build') {
            steps {
            // Get some code from a GitHub repository
            echo "Now running build"
            }
        }
        stage('Unit Tests') {
            steps {
            // Get some code from a GitHub repository
            echo "Now running tests"
            }
        }  
        stage('Compile') {
            steps {
                // Get some code from a GitHub repository
                sh "mvn clean compile"
            }
        }
    }
}

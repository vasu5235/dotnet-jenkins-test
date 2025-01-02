pipeline {
    agent any
    stages {
        // stage('Checkout') {
        //     steps {
        //         // Clone the repository using the configured credentials
        //         git credentialsId: 'vasu5235-git', url: 'https://github.com/vasu5235/dotnet-jenkins-test.git'
        //     }
        // }
        stage('Restore') {
            steps {
                // Restore dependencies
                sh 'dotnet restore'
            }
        }
        stage('Build') {
            steps {
                // Build the project
                sh 'dotnet build --configuration Release'
            }
        }
        stage('Publish') {
            steps {
                // Publish the project
                sh 'dotnet publish --configuration Release --output out'
            }
        }
    }
}

pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout source code from version control
                checkout scmGit(branches: [[name: '*/aws-LiftAndShift']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/devopshydclub/vprofile-project.git']])
            }
        }

        stage('Build') {
            steps {
                // Your build steps go here
                script {
                    // Example: Run a Maven build
                    sh 'mvn install'
                }
            }
        }
    }
    
}

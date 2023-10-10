pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Use the 'git' step to configure Git repository details
                git branch: 'main', url: 'https://github.com/Julizee/application-repo.git'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Package') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}

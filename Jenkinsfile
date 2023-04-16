pipeline {
    agent any

    stages {
        stage('Git checkout') {
            steps {
                // Get some code from a GitHub repository
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Vamc1990/javaSpringBoot.git']])

            }
        }
        stage('Build') {
            steps {
                script {
                sh 'docker build -t "springapplication" .'

            }
                
            }
            
        }
    }
}

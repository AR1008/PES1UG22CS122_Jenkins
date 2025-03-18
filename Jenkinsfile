pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                checkout([$class: 'GitSCM', 
                    branches: [[name: 'main']], 
                    userRemoteConfigs: [[url: ' https://github.com/AR1008/PES1UG22CS122_Jenkins.git']]
                ])
            }
        }
        stage('Build') {
            steps {
                build 'PES1UG22CS122-1'
                sh 'g++ ./main/hello.cpp -o ./output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stageeeeeeeeeeeeeee('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}

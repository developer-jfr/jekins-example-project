pipeline {
    agent {
        label "linux"
    }

    stages {
        stage('Build & Test') {
            steps {
                sh 'docker --version'
                sh 'docker build . -t devx'
                sh 'docker run devx -p 5000:5000'
                sh 'curl http://localhost:5000'
            }
     }
    }
}
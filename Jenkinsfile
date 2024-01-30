pipeline {
    agent any

    stages {
        stage('Check Out') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/7shivam/nodejs-aws-lambda-sam.git']])
            }
        }
        
        stage('SAM Deploy') {
            steps {
                sh 'sam deploy --region us-east-1 --no-confirm-changeset'
            }
        }
    }
}

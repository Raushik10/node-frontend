pipeline {
    agent any
    stages {
        stage('Pull') {
            steps {
                git 'https://github.com/Raushik10/node-frontend.git'
            }
        }
        stage('Install') {
            steps {
                sh 'npm install'
            }
        }
        stage('Restart') {
            steps {
                sh 'pm2 restart frontend || pm2 start app.js --name frontend'
            }
        }
    }
}

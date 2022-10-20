pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
        stage("ssh-server") {
            steps {
                sshagent(['ssh-remote']) {
                    sh 'ssh root@localhost -o StrictHostKeyChecking=no -p 2022 '
                }
            }
        }
    }
}
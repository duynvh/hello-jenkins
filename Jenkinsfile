pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/duynvh/hello-jenkins.git'
            }
        }
        stage('SSH server') {
            steps {
                sshagent(['ssh-remote']) {
                    sh 'ssh -o StrictHostKeyChecking=no -l red 103.92.26.167 touch test.txt'
                }
            }
        }
    }
}
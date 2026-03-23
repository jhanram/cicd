pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/jhanram/cicd.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t myapp:latest .'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                sh 'ansible-playbook deploy.yml'
            }
        }
    }
}

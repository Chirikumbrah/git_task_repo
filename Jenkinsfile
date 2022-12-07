pipeline {
    agent any
    stages {
        stage('Cloning the repo') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Chirikumbrah/git_task_repo/']]])
            }
        }
        stage('Running a docker-compose') {
            steps {
                sh '''#!/bin/bash
                      docker-compose up -d --force-recreate
                '''
            }
        }
    }
}

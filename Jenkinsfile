pipeline {
    agent any

    stages {
        stage('Verify Branch') {
            steps {
                echo '$GIT_BRANCH'
            }
        }

    stage('Docker Build') {
        steps {
          sh label: '', script: '''\'docker image 'node:7-alphine\'
            
                cd azure-vote/
                docker images -a
                docker build -t jenkins-pipeline .
                docker images -a
                cd ..'''
        }
    }
    }
}

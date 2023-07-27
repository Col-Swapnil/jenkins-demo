pipeline {
    agent any
    stages {
        stage('fetch') {
            steps {
                git branch: 'main', url: 'https://github.com/Col-Swapnil/jenkins-demo.git'
            }
        }
        stage('build new') {
            steps {
                sh 'docker build -t ditiss23:v1 .'
                
            }
        }
        stage('deploy') {
            steps {
                sh 'docker run --name ditiss12 -p 9300:80 -d ditiss23:v1'
            }
        }
    }
}

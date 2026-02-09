pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/<your-username>/jenkins-docker-demo.git'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t jenkins-demo:1.0 .'
            }
        }
        stage('Docker Images') {
              steps {
                  sh 'docker images'
              }
          }

        stage('Docker Run') {
            steps {
                sh 'docker run --rm jenkins-demo:1.0'
            }
        }
        stage('Docker running container') {
              steps {
                  sh 'docker ps'
              }
          }
    }
}

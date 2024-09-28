pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                git url:'https://github.com/faizan2245/Notes-app.git', branch: "master" 
            }
        }
        stage('Buliding the App') {
            steps {
                sh "docker build -t app ." 
            }
        }
        stage('Deploying on Docker') {
            steps {
            sh "docker-compose down && docker-compose up -d"
            }
        }
    }
}

pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/silingputih/student-app.git'
            }
        }

        stage('Build') {
            steps {
                sh 'npm install'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t student-app .'
            }
        }

        stage('Run') {
            steps {
                sh 'docker run -d -p 3000:3000 student-app'
            }
        }
    }
}

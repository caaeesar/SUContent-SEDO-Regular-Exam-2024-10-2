pipeline {
    agent any

    stages {
         stage('Checkout') {
            steps {
                git credentialsId: 'Github-token', url: 'https://github.com/caaeesar/SUContent-SEDO-Regular-Exam-2024-10-2'
            }
        stage('Restore dependencies') {
            steps {
                sh 'dotnet restore'
            }
        }
        stage('Build project') {
            steps {
                sh 'dotnet build --no-restore'
            }
        }
        stage('Execute test') {
            steps {
                sh 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}

pipeline {
    agent any

    stages {
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

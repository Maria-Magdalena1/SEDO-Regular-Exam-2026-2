pipeline{
    agent any

    stages{
        stage('Restore Dependencies') {
            when {
                branch 'main'
            }
            steps {
                bat 'dotnet restore'
            }
        }
        stage('Build') {
            when {
                branch 'main'
            }
            steps {
                bat 'dotnet build --no-restore'
            }
        }
        stage('Run Tests') {
            when {
                branch 'main'
            }
            steps {
                bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}
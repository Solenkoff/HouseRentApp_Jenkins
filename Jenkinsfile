pipeline{
    agent any
    stages{
        stage("Restore project dependencies"){
            steps{
                bat 'dotnet restre'
            }
        }
        stage("Build the project"){
            steps{
                bat 'dotnet build --no-restore'
            }
        }
        stage("Run Tests"){
            steps{
                bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}
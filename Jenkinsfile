pipeline{
    agent any
    stages{
        stage("Restore .Net Packages"){
            steps{
                bat 'dotnet restore'
            }
        }
        stage("Build .Net Project"){
            steps{
                bat 'dotnet build --no-restore --configuration Release'
            }
        }
        stage ("Run Unit and .Net Tests"){
            steps{
                bat 'dotnet test --no-build --configuration Release'
            }
        }    
    }

}
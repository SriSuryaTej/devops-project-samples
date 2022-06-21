pipeline{
    agent{ label 'DotNet' }
    triggers{
        corn ('0 * * * * ')
    }
    stages{
        stage('Source code Management'){
            steps {
            git branch: 'declarative', url: 'https://github.com/SriSuryaTej/devops-project-samples.git'
            }
        }
        stage('Build'){
            steps {
                sh 'dotnet build WebApplication.sln --configuration Release --no-restore'
            }
        }
    }

}
pipeline {
    agent any
    stages {
        stage("Restore dependencies"){
            steps{
                sh 'dotnet restore'
              }
            post {
                always{
                    echo 'Restored dependencies'
                  }
              }
          }
        stage("Build application"){
            steps{
                sh 'dotnet build'
              }
          }
        stage("Test application"){
            steps{
                sh 'dotnet test'
              }
          }
      }
  }

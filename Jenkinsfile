pipeline {
    agent any

    stages {
		stage('Restore NuGet Packages') {
            steps {
				bat 'dotnet restore'
            }
        }
		stage('Build Project') {
            steps {
				bat 'dotnet build --configuration Release'
            }
        }
		stage('Run Dotnet Test 1') {
            steps {
				bat 'dotnet test TestProject1/TestProject1.csproj --no-build --verbosity normal'
            }
        }
		stage('Run Dotnet Test 2') {
            steps {
				bat 'dotnet test TestProject2/TestProject2.csproj --no-build --verbosity normal'
            }
        }
		stage('Run Dotnet Test 3') {
            steps {
				bat 'dotnet test TestProject3/TestProject3.csproj --no-build --verbosity normal'
            }
        }		
    }
}
pipeline {
    agent any

    stages 
    {
        stage('Build') 
        {
            steps {script 
						{
							MSBuildHome = tool 'MSBuild'
						}			
						bat "nuget restore" 
						bat "${MSBuildHome}\\MSBuild.exe PerfectBody-DevOps\\PerfectBody.sln"
        }
    }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}

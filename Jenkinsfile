pipeline {
    agent any

    stages 
    {
        stage('Build') 
        {
            steps {
		    script 
			{
				MSBuildHome = tool 'MSBuild'
			}			
			bat "nuget.exe restore PerfectBody-DevOps\\PerfectBody.sln" 
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

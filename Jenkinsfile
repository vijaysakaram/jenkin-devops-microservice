
//DECLERATIVE 
pipeline
 {
	agent any
	//agent { docker {image 'node:14-alpine3.17' } }

	environment{
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH_ORG = "$PATH"
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}


	stages{
		stage('Stage Build'){
			steps{
				echo "Build***************"
				sh 'mvn --version'
				sh "docker --version"

				echo "PATH_ORG - $PATH_ORG"
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"	
				echo "BUILD_ID - $env.BUILD_ID"
				echo "BUILD_TAG - $env.BUILD_TAG"	
				echo "BUILD_URL - $env.BUILD_URL"	
				echo "JOB_NAME - $env.JOB_NAME"

			}
		}
		stage('Stage Test'){
			steps{
				echo "Test"
			}
		}
		stage('Stage Deploy'){
			steps{
				echo "Deploy"
			}
		}		
	}
	post{
		always{
			echo "***** Always Excuted *****"	
		}
		success{
			echo "***** Excuted on Pipeline Success*****"	
		}
		failure{
			echo "***** Excuted on Pipeline Failure*****"	
		}
	}
}

//SCRIPTED PIPELINE 
// node {
// 	stage('Stage Build') {
// 		echo "Build"
// 	}
// 	stage('Stage Test') {
// 		echo "Test"
// 	}
// 	stage('Stage Deploy') {
// 		echo "Deploy"
// 	}	
// }


//DECLERATIVE 
pipeline
 {
	agent any
	stages{
		stage('Stage Build'){
			steps{
				echo "Build"
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

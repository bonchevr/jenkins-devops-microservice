//Scripted

//Declarative

pipeline {
	agent any
	// agent { docker { image 'maven:3.6.3' } }
	// agent { docker { image 'node:20' } }	
	stages {
		stage ('Build') {
			steps {
				// sh 'mvn --version'
				sh 'node --version'
				echo "Build"
				echo "$PATH"
				echo "BUILD_NUMER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_URL - $env.BUILD_URL"
			}
		}
		stage ('Test') {
			steps {
				echo 'Test'
			}
		}
		stage ('Integration Test') {
			steps {
				echo 'Integration Test'
			}
		}
	}

	post {
		always {
			echo 'I am awesome. I run always'
		}
		success {
			echo 'I run when you are succesfull'
		}
		failure {
			echo 'I run when you fail'
		}
	}
}
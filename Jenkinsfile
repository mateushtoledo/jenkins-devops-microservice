// Declarative pipeline
pipeline {
	// agent any
	agent { docker { image 'maven:3.6.3' } }
	agent { docker { image 'node:13.8' } }
	stages {
		stage('Build') {
			steps {
				sh 'node --version'
				echo "Build"
			}
		}
		stage('Test') {
			steps {
				echo "Test"
			}
		}
		stage('Integration Test') {
			steps {
				echo "Integration Test"
			}
		}
	}
	
	// Scripts that runs after the build execution
	post {
		always {
			echo 'Im awesome. I run always'
		}
		success {
			echo 'I run when you are successfull'
		}
		failure {
			echo 'I run when you are fail'
		}
		unstable {
			echo 'I run when your unit tests fail'
		}
		changed {
			echo 'I run when the build status changes (from failure to success, or the inverse)'
		}
	}
}

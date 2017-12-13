pipeline {
	agent any
	tools {
		maven 'maven'
		jdk 'jdk1.8.0_151'
	}
	stages {
		stage ('Build') {
			steps {
				echo 'Building...'
				echo "PATH=${PATH}"
				echo "MAVEN_HOME=${MAVEN_HOME}"
				sh 'mvn clean install'
			}
		}
		stage ('Test') {
			steps {
				echo 'Testing...'
			}
		}
		stage ('Deploy') {
			steps {
				echo 'Deploy...'
			}
		}
	}
	post {
		always {
			archive "target/**/*"
			junit "target/surefire-reports/*.xml"
		}
	//	success {
	//		mail subject:"pues ha ido ok" to:"franciscofc@ocu.es" from:"franciscofc@ocu.es"
	//	}
	}
}

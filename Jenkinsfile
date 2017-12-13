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
}

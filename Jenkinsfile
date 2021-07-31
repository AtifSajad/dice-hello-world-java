pipeline {
	agent {
		docker {
			image 'maven:3-alpine'
			}
		}
		stages {
		stage('Build') {
			steps {
				sh 'sudo mvn -B -DskipTests clean package'
			}
		}
		stage('Test') {
			steps {
				sh 'sudo java -jar target/hello-world-1.jar'
			}
		}
	}
}

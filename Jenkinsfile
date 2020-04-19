pipeline {
	agent {
		docker {
			// Attempting with jdk 8 maven, otherwise will attempt without any tag
			image 'maven:3.6.3-jdk-8'
			args '-v /root/.m2:/root/.m2'
		}
	}
	stages {
		stage('Build') {
			steps {
				sh 'mvn -B -DskipTests clean package'
			}
		}
	}
}
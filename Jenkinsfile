pipeline {
    agent any

    tools {
        maven "maven3"
    }

    stages {
        stage('Build') {
            steps {
                sh "mvn clean package -Dmaven.test.skip=true"
            }
        }
        stage('CodeQuality') {
            steps {
                sh "mvn sonar:sonar -Dsonar.host.url=http://20.96.3.204:9000/ -Dmaven.test.skip=true"
            }
        }
		
    }
}

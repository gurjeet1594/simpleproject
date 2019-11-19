pipeline {
    agent any

    stages {
        stage('Testing Environment') {
            steps {
                    sh 'mvn test -Dtest=ControllerAndServiceSuite'
		    sh 'test -Dtest=IntegrationSuite'
                }
            }
        stage('Build') {
            steps {
		sh 'mvn package -DskipTests'
		sh 'docker build -t="gurjeet151994/simple-project:latest" .'
                }
            }
        stage('Deploy') {
            steps {
		sh 'docker push gurjeet151994/simple-project:latest'
            }
        }
    }
}


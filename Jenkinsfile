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
<<<<<<< HEAD
    
      stage('Testing Environment') {
=======
    }

  stage('Testing Environment') {
>>>>>>> f2ac6c0fbecee2487a26a24cbe6f887ad40d3bdb
            steps {
                echo "hello"
            }
        }
      stage('Staging') {
            steps {
                echo "hello"
            }
        }
      stage('Production') {
            steps {
                echo "hello"
            }
        }
<<<<<<< HEAD
    
 }
}
=======
    }
>>>>>>> f2ac6c0fbecee2487a26a24cbe6f887ad40d3bdb


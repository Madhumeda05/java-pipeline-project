pipeline {

    agent any

    

    stages {

        stage('Build') {
            steps {
                echo "Building Java project"
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests"
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo "Packaging application"
                sh 'mvn package'
                echo "Deployment completed"
            }
        }
    }

    post {
        success {
            echo "Pipeline executed successfully"
        }
        failure {
            echo "Pipeline failed"
        }
    }
}
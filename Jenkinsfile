pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh './gradlew assemble'  // TODO: Build command
            }
        }
        stage('Test') {
            steps {
                sh './gradlew test'  // TODO: Test command
            }
        }
    }

    post {
        always {
            junit 'build/test-results/**/*.xml'  // Collect test results
        }
    }
}

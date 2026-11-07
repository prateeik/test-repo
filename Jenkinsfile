pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build stage completed (smoke-test pipeline).'
            }
        }

        stage('Test') {
            steps {
                sh 'test -s README.md'
                echo 'README smoke test passed.'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check the logs above for details.'
        }
        always {
            echo 'Cleaning up workspace...'
        }
    }
}
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'make -C main'
            }
        }

        degstage('Test') {
            steps {
                sh './main/hello_exec'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}

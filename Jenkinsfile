pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                sh "rsync -av --delete --exclude='.git' --exclude='Jenkinsfile' ./ /var/www/html/"
            }
        }
    }
    post {
        success {
            echo 'Pipeline finished successfully.'
        }
        failure {
            echo 'Pipeline failed. Check the console output.'
        }
        always {
            echo 'Done'
        }
    }
}

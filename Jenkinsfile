pipeline {
    agent any

    stages {

        stage('Build and Run') {
            steps {
                    
                    bat 'docker build -t flaskappp .'
                    bat 'docker run -d -p 5000:5000 flaskappp'
                
            }
        }
    }
    post {
        success {
            echo "Deployment successful!"
        }
        failure {
            echo "Deployment failed."
        }
    }
}

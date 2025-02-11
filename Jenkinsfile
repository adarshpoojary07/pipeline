pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Adsrshpoojary07/pipeline.git'
            }
        }

        stage('Install Newman') {
            steps {
                script {
                    // Install Newman globally using npm
                    sh 'npm install -g newman'
                }
            }
        }

        stage('Run Postman Collection') {
            steps {
                script {
                    // Run the Postman collection using Newman
                    sh 'newman run https://github.com/Adsrshpoojary07/pipeline/blob/main/8.API_Chaining.json'
                }
            }
        }
    }

    post {
        always {
            echo 'Postman collection execution completed.'
        }
    }
}

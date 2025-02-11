pipeline {
    agent any
    environment {
        COLLECTION_URL = "https://github.com/Adsrshpoojary07/pipeline/blob/main/8.API_Chaining.json"
        ENVIRONMENT_URL = "https://github.com/Adsrshpoojary07/pipeline/blob/main/postman_environment.json"
    }
    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/Adsrshpoojary07/pipeline.git'
            }
        }
        
        stage('Run Postman Collection') {
            steps {
                sh '''
                newman run $https://github.com/Adsrshpoojary07/pipeline/blob/main/8.API_Chaining.json -e $https://github.com/Adsrshpoojary07/pipeline/blob/main/postman_environment.json 
                '''
            }
        }
        
    }
}

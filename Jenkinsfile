pipeline { 
    agent any 
    stages { 
        stage('Clone Repository') { 
            steps { 
                git 'https://github.com/sagar-rathod-devops/my-docker-app-dockerfile.git' 
            } 
        } 
        stage('Build Docker Image') { 
            steps { 
                sh 'docker build -t my-app .' 
            } 
        } 
 
        stage('Run Docker Container') { 
            steps { 
                sh 'docker run -d -p 5000:5000 my-app' 
            } 
        } 
    }
}
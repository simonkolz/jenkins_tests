pipeline {
    agent {
        docker {
            // Use the Ubuntu image from Docker Hub
            image 'ubuntu:latest'
            // Set up additional options if needed
            args '-u root' // Example: Run container as root user
        }
    }
    
    stages {
        stage('Build') {
            steps {
                // Update package index
                sh 'apt update'
                
                // Install Maven
                sh 'apt install -y maven'
            }
        }
        
        stage('Test') {
            steps {
                // Check Maven version
                sh 'mvn -version'
            }
        }
        
        // Add more stages as needed
    }
    

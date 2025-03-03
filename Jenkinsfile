pipeline {
    agent any
    
    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/MUKERA-NITHISHA/Arduino-CI.git'
            }
        }
        
        stage('Compile Sketch') {
            steps {
                sh 'arduino-cli compile --fqbn arduino:avr:uno Blink.ino'
            }
        }

        stage('Build Successful') {
            steps {
                echo 'Build completed successfully!'
            }
        }
    }
}


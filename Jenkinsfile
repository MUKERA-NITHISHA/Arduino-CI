pipeline {
    agent any

    environment {
        ARDUINO_CLI_PATH = 'C:/Users/nithisha_mukera/Downloads/arduino-cli_1.2.0_Windows_64bit/arduino-cli.exe'
    }

    stages {
        stage('Checkout Code') {
            steps {
                // Checkout code from the main branch
                git branch: 'main', url: 'https://github.com/MUKERA-NITHISHA/Arduino-CI.git'
            }
        }
        
        stage('Compile Sketch') {
            steps {
                // Correct Windows batch command syntax for environment variable
                bat "%ARDUINO_CLI_PATH% compile --fqbn arduino:avr:uno Blink.ino"
            }
        }

        stage('Build Successful') {
            steps {
                echo '✅ Build completed successfully!'
            }
        }
    }
}


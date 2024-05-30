pipeline {
    agent {
        docker {
            image 'node:14' // Especifica la imagen de Docker que quieres usar
            args '-v /root/.npm:/root/.npm' // Opcional: Montar el volumen para cachear las dependencias de npm
        }
    }
    stages {
        stage('Install') {
            steps {
                echo 'Installing dependencies...'
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'npm run build'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'npm test'
            }
        }
    }
}

pipeline {
    agent any

    stages {
        stage('Clonar repositório do GIT') {
            steps {
                git branch: 'main', url: 'https://github.com/Juliana-lima/Automacao-API-CY.git'
            }
        }
        stage('Instalar dependências') {
            steps {
                bat 'npm install'
            }
        }
        stage('Levantar a API') {
            steps {
                bat 'npm run start'
            }
        }
        stage('Executar os testes') {
            steps {
                bat 'npm run cy:run'
            }
        }
    }
}

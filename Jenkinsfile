pipeline {
    agent any
    stage('build da imagem docker'){
        steps{
            sh 'docker build -t devops/app .'
        }
    }
    stage('subir docker compose'){
        steps{
            sh 'docker-compose up -d'
        }
    }
    stage('sleep para subida dos container'){
        steps{
            sh 'sleep 10'
        }
    }
    stage('teste da aplicação'){
        steps{
            sh 'teste-app.sh'
        }
    }
}
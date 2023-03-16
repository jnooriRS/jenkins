pipeline {

    agent any

 

    stages {

         stage('Init') {

            steps {

                sh 'docker rm -f $(docker ps -qa)'

            }

        }

        stage('Build') {

            steps {

                sh 'docker build -t myapp .'

            }

        }

 

        stage('Deploy') {

            steps {

                sh 'docker run -d -p 5500:5500 --name myapp myapp:latest'

            }

        }

    }

}
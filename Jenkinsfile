
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'docker build -t javatestapp:v2 .'
                sh 'kubectl create deployment app --image=javatestapp:v2'
              sh 'sudo kubectl expose deployment app --type=LoadBalancer --port=8080'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}

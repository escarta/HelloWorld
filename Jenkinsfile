pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Docker') {
            steps {
                script {
                    docker.build('cristian_scartascini/hello-world-app')
                }
            }
        }

        stage('Deploy') {
            steps {
                sh 'oc login --server=${OPENSHIFT_SERVER} --token=${OPENSHIFT_TOKEN} --insecure-skip-tls-verify=true'
                sh 'oc apply -f openshift/deployment.yml'
                sh 'oc apply -f openshift/service.yml'
            }
        }
    }
}
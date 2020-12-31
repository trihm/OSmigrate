pipeline {
    agent ansible-node

    stages {
        stage('Test') {
            sh 'ansible-playbook --check -i iac-tranfer-server/hosts iac-tranfer-server/play-book.yml'
        }
        stage('Deploy'){
            sh 'ansible-playbook -i iac-tranfer-server/hosts iac-tranfer-server/play-book.yml'
        }
    }
}
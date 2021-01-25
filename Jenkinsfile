pipeline {
    agent any {ansible-node}

    stages {
        stage('Test') {
            steps {
                sh 'ansible-playbook --check -i iac-tranfer-server/hosts iac-tranfer-server/play-book.yml'
            }
            
        }
        stage('Deploy'){
            steps {
                sh 'ansible-playbook -i iac-tranfer-server/hosts iac-tranfer-server/play-book.yml'
            }
        }
    }
}
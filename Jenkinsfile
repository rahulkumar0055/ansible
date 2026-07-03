pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/rahulkumar0055/ansible.git'
            }
        }

        stage('Run Ansible') {
            steps {
                sshagent(['ansible-key']) {
                    sh 'ansible-playbook -i inventory apache.yml'
                }
            }
        }
    }
}

pipeline {
    agent any
    stages {
        stage('Clone Git Repository') {
            steps {
             git 'https://github.com/YogeshKolapkar/ansible.git'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                ansiblePlaybook credentialsId: 'ansible-ssh', disableHostKeyChecking: true, installation: 'ansible2', inventory: 'inventory.ini', playbook: 'playbook.yml', vaultTmpPath: ''
            }
        }
    }
}

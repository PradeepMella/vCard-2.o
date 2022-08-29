pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                git url: "https://github.com/PradeepMella/vCard-2.o.git"
            }   
        }
        stage("execute Ansible") {
           steps {
                ansiblePlaybook credentialsId: 'root', disableHostKeyChecking: true, installation: 'Ansible', inventory: 'hosts', playbook: 'nginx-playbook.yaml'
            }    
        }    
    }
}

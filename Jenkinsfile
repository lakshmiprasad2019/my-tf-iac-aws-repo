pipeline {
    agent any

    stages {
        stage('git-checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/lakshmiprasad2019/my-tf-iac-aws-repo.git'
            }
        }
        stage('terraform initialization') {
            steps {
                sh ('terraform init')
            }
            
        }
        stage('terraform action') {
            steps {
                echo "Terraform action is --> ${action}"
                sh ('terraform ${action} --auto-approve')

            }
            
        }
    }
}

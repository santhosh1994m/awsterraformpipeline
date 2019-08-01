pipeline {
    agent {
        node {
            label 'master'
        }
    }


    stages {


        stage('terraform started') {
            steps {
                sh 'echo "Started...!" '
            }
        }
        
        stage('chage path') {
            steps {
                sh 'if [ -d terraformcodeforaws ]; then sudo rm -rf terraformcodeforaws; fi'
            }
        }
        
        stage('git clone') {
            steps {
                sh 'sudo git clone https://github.com/santhosh1994m/terraformcodeforaws.git'
            }
        }
        
         stage('sleep') {
            steps {
                sh 'sleep 10'
            }
        }
        
        stage('terraform init') {
            steps {
                sh 'sudo /usr/local/bin/terraform init ./terraformcodeforaws'
            }
        }
        stage('terraform plan') {
            steps {
                sh 'sudo /usr/local/bin/terraform plan ./terraformcodeforaws'
            }
        }
        stage('terraform ended') {
            steps {
                sh 'echo "Ended....!!"'
            }
        }


        
    }
}

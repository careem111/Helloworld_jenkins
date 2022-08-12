pipeline{
    agent any
    stages{
        stage('checkout'){
                steps{
                    git 'https://github.com/careem111/helloworld1_private.git'
                }
        }
        stage('build'){
            steps{
                sh 'mvn clean install package'
            }
        }
        stage('copy war file'){
            steps{
                sh 'sudo -i;cp webapps/target/*.war /root/images'
            }
        }
        stage('create docker image'){
            steps{
                sh 'docker build'
            }
        }


        }
}

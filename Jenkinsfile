pipeline{
    agent any
    stages{
        stage('Checkout'){
           steps{
              git 'https://github.com/yankils/hello-world.git'
           }
        }
        stage('Build'){
            steps{
                sh 'mvn clean install package'
            }
        }
        stage('Archive'){
            steps{
               archiveArtifacts artifacts: 'webapp/target/*.war', followSymlinks: false
            }
        }
   }

}

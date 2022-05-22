pipeline{
    agent{
        label 'maven2'
    }
    tools{
        maven 'maven354'
    }
    stages{
        stage('CheckOut'){
            steps{
                git 'https://github.com/eshwarprasadv5/MBP.git'
            }
        }
        stage('Build'){
            steps{
                sh "mvn package"
            }
        }
    }
    post{
        always{
            deleteDir()
        }
        success{
            echo "successfull"
        }
        failure{
            echo "Failed"
        }
    }
}

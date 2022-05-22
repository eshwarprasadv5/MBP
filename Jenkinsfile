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
                checkout SCM
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
            echo "success"
        }
        failure{
            echo "Failed"
        }
    }
}

pipeline {
    agent any
    stages{
        stage("Namaste") {
            steps{
                echo "Namaste Jenkins"
            }
        }
        stage("GitCheckout") {
            steps {
                git 'https://github.com/rkmr039/SpringBoot.git'
            }
        }
        stages("Maven Build") {
            steps {
                sh "mvn clean package"
            }
        }
    }
}

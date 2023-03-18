node {
  agent any
  tools{
    maven 'Maven'
  }
  stage("Clone the project") {
    git branch: 'main', url: 'https://github.com/rkmr039/SpringBoot.git'
  }

  stage("Compilation") {
    bat "./mvnw clean install -DskipTests"
  }

  stage("Tests and Deployment") {
    stage("Runing unit tests") {
      sh "./mvnw test -Punit"
    }
    stage("Deployment") {
      sh 'nohup ./mvnw spring-boot:run -Dserver.port=8001 &'
    }
  }
}

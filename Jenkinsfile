pipeline {
  agent any

  stages {
    stage('compilar') {
      steps {
        echo "Estoy compilando el codigo de Sprint Boot"
        sh './mvnw compile'
             }
       }
    stage('test') {
      steps {
        echo "Estoy probando el codigo de Sprint Boot"
        sh './mvnw test'
             }
       }
    stage('GenerarJAR') {
      steps {
        echo "Estoy  generando el JAR del proyecto"
        sh './mvnw package'
             }
       }
    stage('Deploy') {
      steps {
        echo "Estoy desplegando al directorio /tmp del servidor Jenkins "
        sh 'cp target/calculadora-0.0.1-SNAPSHOT.jar /tmp'
             }
       }
   }
}

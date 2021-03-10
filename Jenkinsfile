pipeline {
   agent any

   tools {
      // Install the Maven version configured as "M3" and add it to the path.
      maven "M3"
   }

   stages {
        stage('Build') {
         steps {
            call "mvn clean compile"
         }
        }
        stage('Test') {
           steps {
              call "mvn test"
           }
        }
        stage('Deploy') {
           steps {
              call "mvn clean heroku:deploy"
           }
        }
   }
}
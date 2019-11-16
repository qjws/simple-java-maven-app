pipeline {
   agent any
 tools {
        jdk "jdk1.8"
        maven "maven"
    }
   stages {
      stage('Hello') {
         steps {
            sh ```
mvn clean package
   ```
   echo 'Hello World'
         }
      }
      stage('Hello2') {
         steps {
            echo 'Hello World'
         }
      }
   }
}

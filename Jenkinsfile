pipeline {
   agent any
 tools {
        jdk "jdk1.8"
        maven "maven"
    }
   stages {
      stage('Hello') {
         steps {
          sh '''
                        echo "PATH = ${PATH}"
                        echo "M2_HOME = ${M2_HOME}"
                        mvn clean package
                    '''
         }
      }
      stage('Hello2') {
         steps {
            echo 'Hello World'
         }
      }
      
   }
    post {
        always {
            step([$class: 'Publisher', reportFilenamePattern: '**/testng-results.xml'])
        }
   }
}

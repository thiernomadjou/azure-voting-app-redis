pipeline {
   agent any

   stages {
      stage('Verify Branch') {
         steps {
            echo "$GIT_BRANCH"
         }
      }
      stage('Docker Build') {
         steps {
            sh '/usr/bin/echo MAAmstm7 | sudo -S docker images -a'
            // sh '''cd azure-vote/
            //       sudo -S MAAmstm7 docker images -a
            //       sudo - S MAAmstm7 docker build -t jenkins-pipeline .
            //       sudo - S MAAmstm7 docker images -a
            //       cd ..
            //       '''
         }
      }
   }
}

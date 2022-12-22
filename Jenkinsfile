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
            sh 'sudo -S docker images -a'
            sh '''cd azure-vote/
                  sudo -S docker images -a
                  sudo - S docker build -t jenkins-pipeline .
                  sudo - S docker images -a
                  cd ..
                  '''
         }
      }
   }
}

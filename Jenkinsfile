pipeline {
       agent any
             stages {
                     stage ('one') {
                            steps {
                               echo 'Hi , This is Suhas'
                               }
                     }
                     stage ('two') {
                           steps {
                                 input('Do you want to proceed ?')
                                 }
                    }
                    stage ('three') {
                          when  {
                                not {
                                      branch "master"
                                      }
                                 }
                          steps {
                                 echo  "Hello"
                                 }
                           }
                   stage ('four') {
                          parallel {
                               stage('unit test') {
                                               steps {
                                                      echo "Running unit test ......"
                                                     }
                                                     }
                               stage('Integration Test') {
                                      steps {
                                      
                                                         reuseNode false
                                                         image 'Ubuntu'
                                                         }
                                                 }
                                                 steps {
                                                      echo 'Running the integration test'
                                                      }
                                                      }
                                                      }
 }
 }
 }
      

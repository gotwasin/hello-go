pipeline {
   agent any
   environment {
       registry = "gotwasin/hello-go"
       GOCACHE = "/tmp"
   }
   stages {
        stage('Check Availability') {
          steps {             
            //   waitUntil {
            //       try {         
                    //   sh "kubectl rollout status --watch=true deployment $deploymentName | grep 'successfully'"
            sh "curl -s --head --request GET  172.18.108.49:32075 | grep '200'"
            //           return true
            //       } catch (Exception e) {
            //             return false
            //       }
            //   }
           }
       }
    //    stage('Build') {
    //        agent {
    //            docker {
    //                image 'golang'
    //            }
    //        }
    //        steps {
    //            // Create our project directory.
    //            sh 'cd ${GOPATH}/src'
    //            sh 'mkdir -p ${GOPATH}/src/hello-world'
    //            // Copy all files in our Jenkins workspace to our project directory.               
    //            sh 'cp -r ${WORKSPACE}/* ${GOPATH}/src/hello-world'
    //            // Build the app.
    //            sh 'go build'              
    //        }    
    //    }
    //    stage('Test') {
    //        agent {
    //            docker {
    //                image 'golang'
    //            }
    //        }
    //        steps {                
    //            // Create our project directory.
    //            sh 'cd ${GOPATH}/src'
    //            sh 'mkdir -p ${GOPATH}/src/hello-world'
    //            // Copy all files in our Jenkins workspace to our project directory.               
    //            sh 'cp -r ${WORKSPACE}/* ${GOPATH}/src/hello-world'
    //            // Remove cached test results.
    //            sh 'go clean -cache'
    //            // Run Unit Tests.
    //            sh 'go test ./... -v -short'           
    //        }
    //    }
    //    stage('Publish') {
    //        environment {
    //            registryCredential = 'gotwasin'
    //        }
    //        steps{
    //            script {
    //                def appimage = docker.build registry + ":$BUILD_NUMBER"
    //                docker.withRegistry( '', registryCredential ) {
    //                    appimage.push()
    //                    appimage.push('latest')
    //                }
    //            }
    //        }
    //    }
    //    stage ('Deploy') {
    //        steps {
    //            script{
    //             //    def image_id = registry + ":$BUILD_NUMBER"
    //             //    sh "ansible-playbook  playbook.yml --extra-vars \"image_id=${image_id}\""
    //                sh ""
    //                sh "kubectl apply -f deployment.yml -f service.yml"
    //            }
    //        }
    //    }
   }
}

pipeline{
    agent any
    tools {
        maven "maven3.8.6"
    }
    stages{
        stage('1GetCode'){
            steps{
                sh "echo 'cloning the lastest application version' "
                git "https://github.com/belvisangu/maven-web-application"
            }
        }
        stage('2test+build'){
            steps{
                sh "echo 'running Junit test cases' "
                sh "echo 'testing must succeed to create artifacts' "
                sh "mvn clean package"
            }
        }
      /*
        stage('3CodeQuality'){
            steps{
                sh "echo 'performing CodeQuality' "
                sh "mvn sonar:sonar"
            }
        }
        stage('5UploadtoNexus'){
            steps{
                sh "mvn deploy"
            }
        }
        stage('6deploy2prod'){
            steps{
                deploy adapters: [tomcat9(credentialsId: 'tomcat-credentials', path: '', url: 'http://18.188.241.247:8080/')], contextPath: null, war: 'target/*war'
            }
        }
    }
    post{
    always{
      emailext body: '''Hey guys
Please check build status.
Thanks
Landmark 
+1 437 215 2483''', recipientProviders: [buildUser(), developers()], subject: 'success', to: 'paypal-team@gmail.com'
    }
    success{
      emailext body: '''Hey guys
Good job build and deployment is successful.
Thanks
Landmark 
+1 437 215 2483''', recipientProviders: [buildUser(), developers()], subject: 'success', to: 'paypal-team@gmail.com'
    } 
    failure{
      emailext body: '''Hey guys
Build failed. Please resolve issues.
Thanks
Landmark 
+1 437 215 2483''', recipientProviders: [buildUser(), developers()], subject: 'success', to: 'paypal-team@gmail.com'
    }
  } 
  */
}  

pipeline {
     agent any
      stages {
            stage('Clone Repo') {
                  steps {
	     echo 'Cloning the Repository'
	     git branch:'main',url:'https://github.com/SheebhaSP/myRepo.git',credentialsId:'git.cred'
	 }
            }
             stage('Build') {
	  steps {
	     echo 'BUilding the application'
                      bat 'hello.bat'
	 }

            }
            stage('Test') {
	  steps {
	     echo 'Running the test cases'
                      bat 'echo "All Tests Passed"' 
	 }

            }
            stage('Deploy') {
	  steps {
	     echo 'Deploying the application'
	     bat 'echo "Deployment Successfull"' 
	 }

            }}
            post{
	always{
           	     echo 'Pipeline execution Completed' 
                 }
             }

     }
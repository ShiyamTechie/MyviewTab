pipeline {
agent any
    stages {
        stage('Compile') {
            steps {
               echo 'Compiling the Plugin'
	     bat 'atlas-compile'
            }
        }
        stage('Packaging') {
steps{
              echo 'Packaging the Plugin'
          bat 'atlas-package'
        }
}
        stage('Deploying') {
steps{

 

echo 'deploy started'
bat 'atlas-install-plugin --username kirubakiru31 --password Kiruba@8301 --server localhost --http-port 3031 --plugin-key com.atlassian.plugins.jiratraining.MyViewTab --context-path ""'
}

        }

    }
}
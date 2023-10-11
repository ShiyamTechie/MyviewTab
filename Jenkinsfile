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
bat 'atlas-install-plugin --username shiyamganesh --password Jira@(2023) --server localhost --http-port 8090 --plugin-key com.atlassian.plugins.jiratraining.MyViewTab --context-path "" '
}
           
        }
       
    }
}



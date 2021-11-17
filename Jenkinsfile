node{
    stage('Git Clone'){
      git credentialsId: 'GitHub', url: 'git 'https://github.com/Ramesh0107/calcwebapp.git''
    }
    stage('Maven Package'){
        def mvnHome = tool name: 'maven', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    stage('Deployment'){ 
        sh 'cp target/*.war /home/ubuntu/tomcat/webapps'
    }    
}

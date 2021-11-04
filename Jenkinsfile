node{
    stage('Git Clone'){
      git credentialsId: 'GitHub', url: 'https://github.com/Ramesh0107/calcwebapp.git'
    }
    stage('Maven Package'){
        def mvnHome = tool name: 'Maven', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    stage('Deployment'){ 
        sh 'cp target/*.war /home/ubuntu/opt/tomcat/webapps'
    }    
}

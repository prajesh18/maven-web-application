node{
    def mavenHome= tool name: 'maven-3.9.6'
    stage('Checkout'){
        git branch: 'development', credentialsId: '057364ee-e032-4ffe-a1dc-8365aabfaf7f', url: 'https://github.com/prajesh18/maven-web-application.git'
    }
    stage('Build'){
        
        sh "${mavenHome}/bin/mvn clean package"
    }
    /* stage('Upload_Into_Sonar'){
        sh "${mavenHome}/bin/mvn clean sonar:sonar"
    }
    stage('Upload_Into_Nexusr'){
        sh "${mavenHome}/bin/mvn clean deploy"
    }
    stage('Upload war file into tomcat'){
    sshagent(['2e565087-5981-428a-b9ed-208ccbde2559']){
        sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@172.31.40.15:/opt/apache-tomcat-9.0.86/webapps"
    } 
    } */
}

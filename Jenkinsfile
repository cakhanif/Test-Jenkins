pipeline { 
    agent any     
    stages {
        stage("Checkout") {               
            steps {                    
                git url: 'https://github.com/cakhanif//Test-Jenkins'               
            }          
        }
        stage("Compile"){
            steps{
                'mvn clean package'
            }
        }
        stage("Push"){
            steps{
                'git add .'
            }
            steps{
                'git remote add origin https://gitlab.com/cakhanif/testing'
            }
            steps{
                'git commit -m "coba auto deploy with Jenkins"'
            }
            steps{
                'git push -u origin master'
            }
        }
  }
}

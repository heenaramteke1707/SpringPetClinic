pipeline{
    agent{label 'master'}
    tools{maven 'M3'}
    stages{
        stage('checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/heenaramteke1707/SpringPetClinic.git'              
            }
        }
        stage('Build'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('package'){
            steps{
                sh 'mvn package'
            }
        }
        stage('Deployement'){
            steps{
                sh 'java -jar /usr/share/jenkins/workspace/PetclinicDeclarativePipeline/target/*.jar' 
            }
        }
    }
}

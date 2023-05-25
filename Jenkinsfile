
 pipeline{
 agent any
 stages{

 stage('code checkout'){
  steps{
      git branch: 'main', credentialsId: 'git_credentials', url: 'https://github.com/Chinna474/jenkins-ansible.git'
       }
 }

 stage('Execute Ansible'){
  steps{   
      ansiblePlaybook credentialsId: 'auser2', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dhost.inv', playbook: 'apache.yml'
      }
 }
    }

}

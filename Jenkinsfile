@Library('jenkins-shared-library') _

// These receive parameters from jenkins CI. see nodeJSEKSPipeline
properties([
  parameters([
    string(name: 'appversion', defaultValue: ''),
    choice(name: 'deploy_to', choices: ['dev', 'qa', 'prod'], description: 'Target environment')
  ])
])

def configMap = [
    project: "roboshop",
    component: "user",
    appversion: (params.appversion),
    deploy_to: (params.deploy_to       ?: 'dev'),
]

EKSDeploy(configMap)
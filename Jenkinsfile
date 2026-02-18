@Library('jenkins-shared-library') _

properties([
  parameters([
    string(name: 'appVersion', defaultValue: '', description: 'Docker image tag'),
    string(name: 'deploy_to', defaultValue: 'dev', description: 'Environment')
  ])
])

println "===================================="
println "Received APP VERSION: ${params.appVersion}"
println "Deploying to ENV     : ${params.deploy_to}"
println "===================================="

def configMap = [
    project: "robomart", 
    component: "shipping",
    appVersion: (params.appVersion),
    deploy_to: (params.deploy_to)
]

EKSDeploy(configMap)
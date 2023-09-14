#!/usr/bin/env groovy

/* `buildPlugin` step provided by: https://github.com/jenkins-infra/pipeline-library */
buildPlugin(
  forkCount: '1C',
  // Container agents start faster and are easier to administer
  useContainerAgent: true,
  // Show failures on all configurations
  failFast: false,
  // Test Java 11 with minimum Jenkins version
  // Test Java 17 with a more recent version
  // Test Java 21 with a more recent version
  configurations: [
    [platform: 'linux',   jdk: '11'], // Linux first for coverage report on ci.jenkins.io
    [platform: 'linux',   jdk: '17'],
    [platform: 'linux',   jdk: '21', jenkins: '2.414'],
    [platform: 'windows', jdk: '17', jenkins: '2.389'],
  ]
)

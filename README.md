# node-test
node-test
steps:
  - task: AzurePowerShell@5
    inputs:
      ScriptType: 'InlineScript'
      Inline: '"TLS 1.2 readiness check:"; (Invoke-WebRequest -Uri status.dev.azure.com).StatusDescription'
      FailOnStandardError: true

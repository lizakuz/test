buildPipelineDotNet {
  project = 'app-proxy-snow'
  solutionPath = 'src/proxy-snow.sln'
  dotNetSdk = 'microsoft/dotnet:2.2-sdk-alpine'
  nuGetDefaultVersion = '9.0.0'
  shouldCreateNugetArtifact = false
  testShellCommands = [
    'dotnet test --no-build -o out --logger trx --logger "console;verbosity=normal" src/Faction.SNowProxy.EndToEndSpecs/'
  ]
  testResultsFile = 'src/**/*.trx'
  targetDir = 'out'
  shouldCreateDockerContainer = true
  shouldPushToDockerRegistry = true
  shouldUpdateHelmCharts = true
  shouldDeployToDev = true
}

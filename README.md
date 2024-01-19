# aap-workflows

Main branch har byttet til keyless deploys, bruk @v1 for å fortsette å bruke gammel deploy

## sette opp tokenless deploy
* [Autoriser repository i Console](https://console.nav.cloud.nais.io/team/aap/repositories)
* Sikre at du har satt id-token permissions i den aktuelle joben, eller på toppnivå i workflowet. Om du bruker docker-build-push action har du sannsynligvis dette fra før. Private/internal repositories trenger også contents: "read" permission.
* Fjern APIKEY env-variabel i action konfigurationen
* Slett NAIS_DEPLOY_APIKEY under Settings -> Secrets and variables -> Actions

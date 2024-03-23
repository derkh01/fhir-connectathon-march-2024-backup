
# Demo Project in Mule 4

# Tasks
- read messages off Solace to obtain event URL location
- login to FHIR server and GET record from URL

Can be deployed to Cloudhub 

# Required properties in properties-dev.yaml
(see other NEMSGuaranteedSubscriber README.md for properties and replace **** with the values)
auth:
  server: "https://auth.integration-dev.covid19.health.nz/oauth2/token"
  clientId: "****"
  clientSecret: "****"
  scope: "scope/cinc"
  grantType: "client_credentials"
  
solace:
 clientUsername: "****"
 clientPassword: "****"
 messageVpn: "ring-of-fhir"
 brokerHost: "tcps://ring-of-fhir.messaging.solace.cloud:55443" 

fhir:
  xApiKey: "****" 
  requestContext: "****"

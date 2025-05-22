# ACA-PY DID Web Demo

## Setup the project

- Fork this repository and create a new branch called `gh-pages`.
- Configure a Github page to be deployed from that branch.

## Register a web did in aca-py
*Replace {{organization}} with your github organization name.*
```bash
curl -X 'POST'   'http://172.17.0.1:8032/wallet/did/create'   -H 'accept: application/json'   -H 'Content-Type: application/json'   -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ3YWxsZXRfaWQiOiJkZWYxMjFkMC1lYTQyLTRiMzEtOTc0ZC00OGJjYzIxNmFjMmIiLCJpYXQiOjE3NDc4OTAzMTYsImV4cCI6MTc0Nzk3NjcxNn0.78odxIoup-40z30EzanQ-iYwvE1Xr56faBeuW_xcP4c'   -d '{
  "method": "web",
  "options": {
    "did": "did:web:sneha-kolimi.github.io:acapy-did-web-demo",
    "key_type": "ed25519"
  }
}'
```
Capture the verkey from the response.

## Update did doc template

Edit the [did.json](did.json) document. 
- Replace all organization placeholders with the name of your github organization and insert the verkey.
- *Make sure you are on the new `gh-pages` branch.*

  Once you commit these changes, wait for the page to be deployed and your did should now be useable.

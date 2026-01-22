# BirthCertificateCredential

```json
{
    "@context": [
        "https://www.w3.org/2018/credentials/v1",
        "https://schemas.opencrvs.org/birth-certificate.json"
    ],
    "type": ["VerifiableCredential", "BirthCertificateCredential"],
    "id": "THIS WILL BE REPLACED WITH DYNAMIC DATA FUNCTION",
    "credentialSubject": {
      "id": "THIS WILL BE REPLACED WITH DYNAMIC DATA FUNCTION",
      "given_name": "John",
      "family_name": "Doe",
      "birthdate": "1940-01-01",
      "place_of_birth": "Chamakubi Health Post, Ibombo, Central, Farajaland"
    },
    "issuer": {
        "id": "THIS WILL BE REPLACED WITH DYNAMIC DATA FUNCTION",
        "name": "Government of Farajaland"
    },
    "issuanceDate": "THIS WILL BE REPLACED WITH DYNAMIC DATA FUNCTION",
    "expirationDate": "THIS WILL BE REPLACED WITH DYNAMIC DATA FUNCTION"
}
```

## Manifest

```json
{
    "claims": {
      "Given Name": "$.credentialSubject.given_name",
      "Family Name": "$.credentialSubject.family_name",
      "Birth Date": "$.credentialSubject.birthdate",
      "Place of Birth": "$.credentialSubject.place_of_birth"
    }
}
```

## Mapping example

```json
{
    "id": "<uuid>",
    "issuer": {
        "id": "<issuerDid>"
    },
    "credentialSubject": {
        "id": "<subjectDid>"
    },
    "issuanceDate": "<timestamp>",
    "expirationDate": "<timestamp-in:365d>"
}
```
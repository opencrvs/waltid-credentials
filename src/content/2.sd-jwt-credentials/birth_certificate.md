# Birth Certificate

This is an example of an IETF SD-JWT (Selective Disclosure JWT) Verifiable Credential for birth certificate verification.

## Example SD-JWT

```json
{
  "header": {
    "alg": "EdDSA",
    "typ": "JWT"
  },
  "payload": {
    "iss": "did:key:z6MkjoRhq1jSNJdLiruSXrFFxagqrztZaXHqHGUTKJbcNywp",
    "iat": 1640995200,
    "exp": 1672531200,
    "vct": "https://schemas.opencrvs.org/birth-certificate.json",
    "sub": "did:example:123456789abcdef",
    "cnf": {
      "jwk": {
        "kty": "OKP",
        "crv": "Ed25519",
        "x": "T3T4-u1Xz3vAV2JwPNxWfs4pik_JLiArz_WTCvrCFUM"
      }
    },
    "sd_hash": "sha256-hash-of-disclosed-claims"
  }
}
```

## Selective Disclosure Claims

The following claims can be selectively disclosed:

- **Given Name**: `$.given_name`
- **Family Name**: `$.family_name`
- **Birth Date**: `$.birthdate`
- **Place of Birth**: `$.place_of_birth`

## Usage

This credential demonstrates the IETF SD-JWT standard for selective disclosure of verifiable credential claims, allowing users to prove birth certificate attributes without revealing their entire birth record.
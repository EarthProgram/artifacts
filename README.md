# Artifacts

Artifacts that illustrate Earth Program use cases and solutions

## Renewable Energy Certificates

These artifacts help realize the Renewable Energy Certificates Focal Use Case.

### Cryptographic Materials

Many of the identifiers used in this set of artifacts are DIDs based on cryptographic public/private keypairs. This allows the artifacts' identifiers to be created offline and secured using cryptographic signatures.

The public/private key pairs are Secp256k1 keys generated using [didkit](https://spruceid.dev/docs/didkit/) and represented in [Json Web Key](https://datatracker.ietf.org/doc/html/rfc7517) format. The .jwk files contain both the public and private keys for each actor. From these keys a DID and associated DID Document has been generated using didkit.

* **HydroElec** &mdash; The producer behind the proposed project.
  * Key pair [./rec/keys/hydroelec.jwk](./rec/keys/hydroelec.jwk)
  * DID [./rec/dids/hydroelec.did.json](./rec/dids/hydroelec.did.json)

* **Smart Meter 1** &mdash; The first of two electric meters that issue signed VCs as evidence of electricity production.
  * Key pair [./rec/keys/meter1.jwk](./rec/keys/meter1.jwk)
  * DID [./rec/dids/meter1.did.json](./rec/dids/meter1.did.json)

* **Smart Meter 2** &mdash; The second of two electric meters that issue signed VCs as evidence of electricity production.
  * Key pair [./rec/keys/meter2.jwk](./rec/keys/meter2.jwk)
  * DID [./rec/dids/meter2.did.json](./rec/dids/meter2.did.json)

* **UN FCCC** &mdash; The issuing authority for REC2022 Renewable Energy Certificates.
  * Key pair [./rec/keys/unfccc.jwl](./rec/keys/unfccc.jwk)
  * DID [./rec/dids/unfccc.did.json](./rec/dids/unfccc.did.json)

* **UN Rec2022** (DOES THIS NEED TO BE CRYPTOGRAPHIC?)
  * Key pair [./rec/keys/un.rec2022.jwk](./rec/keys/un.rec2022.jwk)
  * DID [./rec/dids/un.rec2022.did.json](./rec/dids/un.rec2022.did.json)

* **Certifier** &mdash; A UN authorized project certifier. They review the project proposal from the producer and issue an REC2022 Certification verifiable credential.
  * Key pair [./rec/keys/certifier.jwk](./rec/keys/certifier.jwk)
  * DID [./rec/dids/certifier.did.json](./rec/dids/certifier.did.json)

* **Verifier** &mdash; A UN authorized project verifier. They review the project on-site and issue an REC2022 Verification verifiable credential, based the propsoal, the REC2022 Certification, and the evidence produced by the Project's smart meters.
  * Key pair [./rec/keys/verifier.jwk](./rec/keys/verifier.jwk)
  * DID document [./rec/dids/verifier.did.json](./rec/dids/verifier.did.json)


### Verifiable Credentials (VCs)

1. Project Proposal

This VC captures the automated metadata about the project and refers definitively for a descriptive PDF with additional details. [./rec/credentials/hydroelec.project1.json](./rec/credentials/hydroelec.project1.json)

That file is a fully formed VC describing the following metadata:
* **producer**: HydroElec's DID for exercising control over this project
* **geographicLocation**: The GPS coordinates for the project location in Capetown, South Africa.
* **dateProposed**: January 30, 2022
* **annualTarget**: The expected annual electricity production of 1000 MWh

It is signed by HydroElec. (Or, it will be. Currently the proof is faked.)

2. Certifier Credential
3. Verifier Credential
4. Project Certification
5. Project Verification
6. Electricity Production

### DIDs
Throughout these examples, we use a fictional did:example which uses an Ed25519 public key for both the method-specific identifier and all of its verification methods.

#### 1. HydroElec

The file [./rec/keys/hydroelec.jwk](./rec/hydroelec.ed25519) is a representation of the private and public keys, respectively, that control this DID:

```did:key:zQ3shPm1156YHd3pzvhz8BMtZPT9LnTxtGyFBnm8tzJmjnBWD```

When this DID is resolved it returns the DID Document found in [./rec/dids/hydroelec.did.json](./rec/dids/hydroelec.did.json)

2. UNFCCC
3. Certifier
4. Verifier
5. Project (as registered)

### IIDs
1. The NFT class created by the UNFCCC
2. The particular NFT tokens minted
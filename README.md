# Artifacts

Artifacts that illustrate Earth Program use cases and solutions

## Renewable Energy Certificates
These artifacts help realize the Renewable Energy Certificates Focal Use Case.

### Cryptographic Materials

Many of the identifiers used in this set of artifacts are DIDs based on cryptographic public/private keypairs. This allows the artifacts' identifiers to be created offline and secured using cryptographic signatures.

The public/private key pairs for these identifiers have been generated using Ed25519:

* **HydroElec** &mdash; The producer behind the proposed project.
  * private Key [./rec/hydroelec.ed25519](./rec/hydroelec.ed25519)
  * public key [./rec/hydroelec.ed25519.pub](./rec/hydroelec.ed25519.pub)

* **Smart Meter 1** &mdash; The first of two electric meters that issue signed VCs as evidence of electricity production.
  * private Key [./rec/meter1.ed25519](./rec/meter1.ed25519)
  * public key [./rec/meter1.ed25519.pub](./rec/meter1.ed25519.pub)

* **Smart Meter 2** &mdash; The second of two electric meters that issue signed VCs as evidence of electricity production.
  * private Key [./rec/meter2.ed25519](./rec/meter2.ed25519)
  * public key [./rec/meter2.ed25519.pub](./rec/meter2.ed25519.pub)

* **UN FCCC** &mdash; The issuing authority for REC2022 Renewable Energy Certificates.
  * private Key [./rec/unfccc.ed25519](./rec/unfccc.ed25519)
  * public key [./rec/unfccc.ed25519.pub](./rec/unfccc.ed25519.pub)

* **UN Rec2022** (DOES THIS NEED TO BE CRYPTOGRAPHIC?)
  * private Key [./rec/un.rec2022.ed25519](./rec/un.rec2022.ed25519)
  * public key [./rec/un.rec2022.ed25519.pub](./rec/un.rec2022.ed25519.pub)

* **Certifier** &mdash; A UN authorized project certifier. They review the project proposal from the producer and issue an REC2022 Certification verifiable credential.
  * private Key [./rec/certifier.ed25519](./rec/certifier.ed25519)
  * public key [./rec/certifier.ed25519.pub](./rec/certifier.ed25519.pub)

* **Verifier** &mdash; A UN authorized project verifier. They review the project on-site and issue an REC2022 Verification verifiable credential, based the propsoal, the REC2022 Certification, and the evidence produced by the Project's smart meters.
  * private Key [./rec/verifier.ed25519](./rec/verifier.ed25519)
  * public key [./rec/verifier.ed25519.pub](./rec/verifier.ed25519.pub)


### Verifiable Credentials (VCs)

1. Project Proposal

This VC captures the automated metadata about the project and refers definitively for a descriptive PDF with additional details. [./rec/hydroelec.project1.json](./rec/hydroelec.project1.json)

That file is a fully formed VC describing the following metadata:
* **producer**: HydroElec's DID for exercising control over this project
* **geographicLocation**: The GPS coordinates for the project location in Capetown, South Africa.
* **dateProposed**: January 30, 2022
* **annualTarget**: The expected annual electricity production of 1000 MWh

It is signed by HydroElec.

2. Certifier Credential
3. Verifier Credential
4. Project Certification
5. Project Verification
6. Electricity Production

### DIDs
Throughout these examples, we use a fictional did:example which uses an Ed25519 public key for both the method-specific identifier and all of its verification methods.

#### 1. HydroElec

The included files, [./rec/hydroelec.ed25519](./rec/hydroelec.ed25519) and [./rec/hydroelec.ed25519.pub](./rec/hydroelec.ed25519.pub) are the private and public keys, respectively, that control this DID:

```did:example:AAAAC3NzaC1lZDI1NTE5AAAAICwtd+9EJPeiBDh37Ffi6uJ6grYqtH97WrJW0fyui9rX```

See [./rec/hydroelec.did.json](./rec/hydroelec.did.json) for the DID Document for HydroElec.

2. UNFCCC
3. Certifier
4. Verifier
5. Project (as registered)

### IIDs
1. The NFT class created by the UNFCCC
2. The particular NFT tokens minted
# Awesome-Machine-Identity-Management

## Top Machine Identity Management Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Certificate Lifecycle Management (CLM), Workload Identity, PKI, SPIFFE/SPIRE, Secrets for Machines & Automated Credential Rotation*  

**Last updated: September 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Machine Identity Management**. These systems discover, issue, rotate, and govern non-human identities—TLS/SSL certificates, workload identities (SPIFFE), SSH keys, API keys, and service credentials—across cloud, Kubernetes, IoT, and hybrid infrastructure.



**Examples** include Venafi (CyberArk), Keyfactor, AppViewX, Entrust Certificate Hub, HashiCorp Vault, CyberArk Machine Identity, Sectigo Certificate Manager, DigiCert Trust Lifecycle Manager, Fortanix, Teleport, and SPIFFE/SPIRE enterprise offerings (the category leaders).



**Open-source emphasis**: Machine identity has one of the strongest open-source foundations in security. **SPIFFE/SPIRE**, **step-ca**, **cert-manager**, **HashiCorp Vault** (and OpenBao), **EJBCA**, and related projects power production PKI and workload identity at scale. This section is heavily expanded with every major active project.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Venafi / CyberArk Machine Identity Security](https://www.venafi.com/)**  

  Leading enterprise machine identity platform for certificate lifecycle management, discovery, policy enforcement, and workload identity across large, heterogeneous estates.



- **[Keyfactor](https://www.keyfactor.com/)**  

  CA-agnostic certificate lifecycle management platform with strong PKI capabilities (including ownership of the open-source EJBCA engine) and automation for enterprise CLM.



- **[AppViewX](https://www.appviewx.com/)**  

  Automation-focused certificate and crypto management platform with deep network-device integrations and certificate lifecycle orchestration.



- **[HashiCorp Vault (Enterprise / HCP)](https://www.hashicorp.com/products/vault)**  

  Secrets and identity platform widely used for dynamic machine credentials, PKI secrets engine, and short-lived certificate issuance (open-source core available).



- **[DigiCert Trust Lifecycle Manager, Sectigo Certificate Manager, Entrust](https://www.digicert.com/)**  

  CA-backed certificate lifecycle and digital-trust platforms combining public/private PKI with discovery, automation, and policy controls.



- **[Fortanix, Teleport](https://fortanix.com/)**  

  Solutions covering confidential computing / key management and infrastructure identity (SSH, Kubernetes, databases) with strong machine-oriented access controls.



- **[SPIFFE/SPIRE Enterprise offerings & related commercial support](https://spiffe.io/)**  

  Commercial support, managed services, and enterprise distributions built around the open SPIFFE/SPIRE standards for workload identity.



- **[Other machine identity & CLM platforms](https://www.venafi.com/)**  

  Additional commercial tools for SSH key management, code-signing, IoT device identity, and crypto-agility / post-quantum readiness.



## Open-Source GitHub Projects



- **[SPIRE (SPIFFE Runtime Environment)](https://github.com/spiffe/spire)**  

  CNCF-graduated open-source implementation of the SPIFFE standard. Issues short-lived X.509 and JWT SVIDs to workloads after attestation, enabling zero-trust machine-to-machine authentication across heterogeneous platforms.



- **[step-ca (Smallstep Certificates)](https://github.com/smallstep/certificates)**  

  Lightweight, modern open-source certificate authority designed for automated certificate management. Supports ACME, short-lived certs, SSH certificates, OIDC, and easy integration with DevOps and Kubernetes workflows.



- **[cert-manager](https://github.com/cert-manager/cert-manager)**  

  Kubernetes-native certificate management controller that automates issuance and renewal of TLS certificates from a variety of issuers (Let’s Encrypt, step-ca, Vault, SPIFFE, etc.).



- **[HashiCorp Vault (Open Source) / OpenBao](https://github.com/hashicorp/vault)**  

  Open-source secrets management platform with a powerful PKI secrets engine for dynamic certificate issuance, lease-based credentials, and fine-grained policy. OpenBao continues the open-source lineage under a community-friendly license.



- **[EJBCA](https://github.com/Keyfactor/ejbca-ce)**  

  Widely deployed open-source PKI and certificate authority (Community Edition) used as the issuance engine in many enterprise and Keyfactor deployments.



- **[cert-manager CSI Driver SPIFFE & related SPIFFE tooling](https://github.com/cert-manager/csi-driver-spiffe)**  

  Kubernetes CSI driver and supporting projects that deliver SPIFFE SVIDs to pods as ephemeral volumes, enabling seamless workload identity.



- **[CFSSL, Boulder, and other CA / PKI toolkits](https://github.com/cloudflare/cfssl)**  

  Open-source PKI toolkits and ACME server implementations used to build custom certificate authorities and automation pipelines.



- **[Other machine identity & certificate projects](https://github.com/search?q=SPIFFE+OR+SPIRE+OR+certificate+lifecycle+OR+machine+identity)**  

  Additional community tools for discovery, rotation, SSH certificate authorities, and crypto policy enforcement.



### Additional Strong Open-Source Options



- **ACME clients & automation**: Certbot, lego, and native ACME support in step-ca / cert-manager for public and private certificates.

- **SSH certificate authorities**: step-ca SSH CA mode and related open tools for host and user SSH certificates.

- **Secrets operators**: External Secrets Operator and similar projects that deliver machine credentials into Kubernetes.

- **Trust bundle distribution**: Mechanisms for distributing and rotating trust anchors across clusters and fleets.

- **Policy & discovery scanners**: Open tools that inventory certificates and keys across infrastructure.

- Fully open stacks combining SPIRE (workload identity) + step-ca or Vault PKI (issuance) + cert-manager (Kubernetes automation).



**Frameworks for building custom systems**:  

The strongest open-source foundation for modern machine identity is **SPIFFE/SPIRE** for workload identity, paired with **step-ca** or **Vault/OpenBao PKI** for certificate issuance and **cert-manager** for Kubernetes-native automation.  

**EJBCA** provides a full-featured open-source CA for more traditional PKI needs.  

These components can be combined into production-grade, short-lived-certificate architectures.  

Commercial platforms (Venafi/CyberArk, Keyfactor, AppViewX, DigiCert TLM, Sectigo, etc.) add enterprise discovery, multi-CA orchestration, compliance reporting, crypto-agility tooling, and vendor support that many large organizations still require.  

Cloud-native and platform teams increasingly run SPIRE + step-ca/cert-manager stacks, while enterprises with large legacy certificate estates often standardize on Venafi or Keyfactor and integrate open-source components at the edges.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Machine identity systems control authentication for infrastructure, applications, and services. Misconfiguration can lead to outages or security breaches. Proper key protection (HSMs/KMS), short lifetimes, monitoring, and incident response planning are essential.

- Open-source PKI and identity tools offer transparency and freedom from proprietary lock-in but require operational expertise for high availability, secure key storage, and compliance. Evaluate threat model, audit requirements, and support needs carefully before production use.



---



**Made for platform engineers, security architects, PKI operators, SRE teams, and zero-trust practitioners.**  

Let's make strong, automated machine identity the default—through both battle-tested commercial platforms and robust open-source foundations.

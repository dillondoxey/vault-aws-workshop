name: chapter-1
class: title, shelf, no-footer, fullbleed
background-image: url(images/hashicorp-title-bkg-aws.jpeg)
count: false

# Chapter 1  
## HashiCorp Vault Overview

![:scale 15%](images/vault_logo_y.png)

???
Lets start off with a Vault Overview, covering how HashiCorp Vault can help you solve the common use cases like secrets management and identity based access.

For this lab, we will not be covereing data encryption, so if you would like to see a deeper dive into this topic please reach out in the Zoom chat and we will connect you with your account team to provide additional demos and hand's on labs.

---
name: hashiCorp-vault-overview
# HashiCorp Vault Overview
  * HashiCorp Vault is an API-driven, platform agnostic secrets management system.
  * It allows you to safely store and manage sensitive data in hybrid cloud environments.
  * You can also use Vault to generate dynamic short-lived credentials, certificates, or encrypt application data on the fly.

???
This is meant as a high level overview. For detailed descriptions or instructions please see the docs, API guide, or learning site:

* https://www.vaultproject.io/docs/
* https://www.vaultproject.io/api/
* https://learn.hashicorp.com/vault/

---
name: the-old-way
layout: false
# The Traditional Security Model
.center[![:scale 70%](images/bodiam_castle.jpg)]
.center[Also known as the "Castle and Moat" method.]

???
Traditional security, like we see with on-prem data centers are commonly security with the "Castle and Moat" type of security.

---
layout: true

.footer[
- Copyright © 2021 HashiCorp
- ![:scale 100%](https://hashicorp.github.io/field-workshops-assets/assets/logos/HashiCorp_Icon_Black.svg)
]

---
name: traditional-security-models
# The Traditional Security Model
An easy way to think of this is 4 walls and a pipe to the internet. Using a firewall at the edge and treating anything behind that as a high-trust network.

* Traditional security models were built upon the idea of perimeter based security.
* There would be a firewall, and inside that firewall it was assumed one was safe.
* Resources such as databases were mostly static.  As such rules were based upon IP address, credentials were baked into source code or kept in a static file on disk.

???
What we all have seen is there are a lot of issues with this security model, because most of it is based on an IP address and some hardware configurations. 

This model does not work when we start to look at moving to AWS because we dont control the perimeter, and we also move away from the idea of static ip addresses for our workloads.

---
name: problems-with-traditional-security-models
# Problems with the Traditional Security Model
* IP Address based rules
* Hardcoded credentials with problems such as:
  * Shared service accounts for apps and users
  * Difficult to rotate, decommission, and determine who has access
  * Revoking compromised credentials could break

???
* This slide describes some of the problems with the traditional security model.
---
name: the-new-way
layout: false
# Modern Secrets Management
.center[![:scale 65%](images/nomadic_houses.jpg)]
.center[No well defined perimeter; security enforced by identity.]

???
* These are Mongolian Yurts or "Ger" as they are called locally. Instead of a castle with walls and a drawbridge, a fixed fortress that has an inside and an outside, these people move from place to place, bringing their houses with them.

* And if you don't think the Nomadic way can be an effective security posture, think about this for a moment. The Mongol military tactics and organization enabled the Genghis Khan to conquer nearly all of continental Asia, the Middle East and parts of eastern Europe. Mongol warriors would typically bring three or four horses with them, so they could rotate through the horses and go farther. Mongol army units could move up to 100 miles a day, which was unheard of in the 13th century. They were faster, more adaptable, and more resilient than all their enemies.

---
name: identity-based-security-1
#Identity Based Security
.center[![:scale 75%](images/identity-triangle.png)]
.center[<a href="https://www.hashicorp.com/identity-based-security-and-low-trust-networks" target="_blank">Identity Based Security and Low Trust Networks</a>]

???
* Starting at the top, clients can be people, machines, or even API's
* We also see that Vault has multiple means of authenticating users and applications with its many different Auth Methods.
* Vault can manage many types of secrets and excels at generating short-lived, dynmamic secrets.
* Vault's ACL policies are associated with tokens that users and applications use to access secrets after authenticating.
* Tokens can only read/write secrets that its policies allow.
* Click on the link to read a white paper about identity-based security in low trust networks.

---
layout: true

.footer[
- Copyright © 2021 HashiCorp
- ![:scale 100%](https://hashicorp.github.io/field-workshops-assets/assets/logos/HashiCorp_Icon_Black.svg)
]

---
name: identity-based-security-2
# Identity Based Security

Vault was designed to address the security needs of modern applications.  It differs from the traditional approach by using:

* Identity based rules allowing security to stretch across network perimeters
* Dynamic, short lived credentials that are rotated frequently
* Individual accounts to maintain provenance (tie action back to entity)
* Credentials and Entities that can easily be invalidated

???
* This slide discusses how Vault is designed for modern applications.

---
name: secrets-engines
layout: false
# Vault Secrets Engines
.center[![:scale 60%](images/vault-engines.png)]
.center[<a href="https://www.vaultproject.io/docs/secrets/" target="_blank">Vault Secrets Engines</a>]

???
* Vault provides many out-of-the-box secrets engines.
* Additional custom secrets engines can be added by customers.
* Click on the link to learn more about Vault secrets engines.

---
name: vault-reference-architecture-1
# Vault Architecture Internals
.center[![:scale 75%](images/vault_arch.png)]
.center[<a href="https://www.vaultproject.io/docs/internals/architecture/" target="_blank">HashiCorp Vault Internals Architecture</a>]

???
* Click the link to learn more about the internal's of Vault's architecture.

---
name: vault-reference-architecture-2
# Vault Architecture - High Availability
.center[![:scale 60%](images/vault-ref-arch-lb.png)]
.center[<a href="https://www.vaultproject.io/docs/concepts/ha" target="_blank">Vault High Availability</a>]

???
* Vault allows multiple servers to be combined in a highly available cluster within a single cloud region or physical data center.
* Click on the link to learn more about Vault's high availability in a single cluster.

---
name: vault-reference-architecture-3
# Vault Architecture - Multi-Region
.center[![:scale 70%](images/vault-ref-arch-replication.png)]
.center[<a href="https://www.vaultproject.io/docs/enterprise/replication/" target="_blank">Vault Enterprise Replication</a>]

???
* Vault Enterprise supports replication between clusters across regions and data centers.
* It supports Disaster Recovery and Performance replication.
* These can be used together.
* Click the link to learn more about Vault's replication.

---
layout: true

.footer[
- Copyright © 2021 HashiCorp
- ![:scale 100%](https://hashicorp.github.io/field-workshops-assets/assets/logos/HashiCorp_Icon_Black.svg)
]

---
name: chapter-1-review-question
# 📝 Chapter 1 Review

* What is HashiCorp Vault?

???
* Let's review what we learned in this chapter.
---
name: chapter-1-review-answer
# 📝 Chapter 1 Review
* What is HashiCorp Vault?
  * Vault is a Secrets Management System.
  * It is API-driven and cloud agnostic.
  * It can be used in untrusted networks.
  * It can authenticate users and applications against many systems.
  * It supports dynamic generation of short-lived secrets.
  * It runs in highly available clusters that can be replicated across regions.

???
* Here are the answers to the review questions.

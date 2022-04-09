name: vault-title-slide
class: title, shelf, no-footer, fullbleed
background-image: url(images/hashicorp-title-bkg-aws.jpeg)
count: false

# Vault Workshop
## Modern Security with Vault and AWS

![:scale 15%](images/vault_logo_y.png)

???
Welcome everyone. 

Today we will be diving into HashiCorp Vault and AWS.

Vault is not limited to just AWS, and can be used in really any hybrid-cloud configuration, and with Vault Enterprise we can include features like scaling and replication as an example to support enterprise scale deployments!

---
layout: true

.footer[
- Copyright © 2021 HashiCorp
- ![:scale 100%](https://hashicorp.github.io/field-workshops-assets/assets/logos/HashiCorp_Icon_Black.svg)]

---
name: Table-of-Contents
# Table of Contents

1. HashiCorp Vault Overview
1. Interacting with Vault
1. Running a Production Server
1. Vault Secrets Engines
1. Vault Authentication Methods
1. Vault Policies
1. Vault AWS Auth Method
1. Vault AWS Secrets Engine

???
This is what we will be covering today. 

We will start with lecture, getting everyone familar with Vault and the basic operations. 

After that, we will then do a Vault Basics lab where you will be able to take what you learned from the lecure, and use a lab to take a deeper "hands-on" approach to Vault.

Once we have completed the basics lab, we will do a lecure for the AWS Auth method, and follow that with a lab.

Finally, we will close out the session with the Vault AWS secrets engine lecture, follwed by a lab and then call it a day!

---
name: instruqt-tracks
# Lab Environment Used
* This workshop uses <a href="https://instruqt.com" target="_blank">Instruqt</a> for hands-on labs.
* Instruqt labs are run in "tracks" that are divided into "challenges".
* This workshop uses the following tracks:
    1. **Vault Basics**
    1. **Vault AWS Auth Method**
    1. **Vault AWS Dynamic Secrets**
* We'll cover chapters 1-6 and then do the first lab.
* We'll then cover chapter 7 with the second lab.
* We'll finish with chapter 8 and the third lab.

???
We use Instruqt for our labs, which makes using Vault inside of AWS easy. 

All that you will need will be a web browser to get going and instructions inside the lab will walk you through what you need to do.

When it is time for the lab, we will use Zoom BreakOut rooms to move everyone into smaller groups. During the breakout rooms the session recording will be inactive.

There will also be a HashiCorp or AWS employee in to help with any questions as you move through the lab.

I do have a couple of recommendations to make the lab work as smoothly as possible.
* Google Chrome, Brave, Internet Edge
* Disconnect from a VPN if you are using one
* Read the instructions carefully, and utilize the copy-paste capability inside of the lab if you dont like to type
* If you have a question, don't be shy and ask a HashiCorp or AWS instructor
* Have fun, and learn as much as possible

**You will have to provide the links for the tracks: Vault Basics, AWS Auth Method for Vault, AWS Dynamic Secrets with Vault**

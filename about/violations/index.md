---
layout: single
title:  "Violation Examples"
sidebar:
  nav: about
---



**Violation**|**Why**|**Example**
-----|-----|-----
Image Size | Efficiency | 5 GB image size
Image Repo | Security | Downloading image from a shady repo
Extra Capabilities | Security | Setting UID/GUID
Privileged Mode | Security| Root containers
Single Replica | Availability | Not 12-factor app
Invalid Ingress | Security/Stability |  Having \"*" in ingress
Mount Host Vols | Security/Stability | Mounting kubernetes system files
No Owner  | Security | No owner annotation for namespace
Required Entity | Security/Stability | Required pod not deployed
Required Annotation  | Security/Stability | Required annotation for reporting not configured
Required Labels  | Security/Stability | Required label for reporting not configured


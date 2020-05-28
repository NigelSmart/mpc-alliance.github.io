---
title: Static vs Adaptive Adversary
parent: Security model
has_children: true
nav_order: 3
---

# Static vs Adaptive Adversary

As well as worrying about the question of semi-honest vs malicious security one needs to consider whether the adversary is static (i.e. they select the parties to corrupt at the start of the computation) or adaptive (i.e. they can select who to correct whilst the protocol is in process). Usually protocols are considerd in the static model, as full adaptive security is very hard to obtain.

A practical middle-ground adopted in many products is to consider so-called pro-active adversaries. Here we divide the computation into time intervals. At the start of each time interval the adversary can decide which of the parties they want to corrupt. Thus within each time period the adversary model is essentially static. However, at the end of the time-period the adversary can then switch which parties they corrupt. Thus they are able to move between different parties. To obtain protocols secure in this model one executes a re-sharing protocol at the end of each time period.
